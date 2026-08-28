# Deployment

The site is a Jekyll build of `README.md` (via `index.md`), published to two hosts
from the same source. Each host builds it independently on every push to `main`.

| Target | URL | Deployed by |
| --- | --- | --- |
| GitHub Pages | <https://tiennm99.github.io/penny-pincher-provider> | `.github/workflows/github-pages.yml` |
| Cloudflare Pages | <https://penny-pincher-provider.pages.dev> | Cloudflare's Git integration |

Both build with this repo's `Gemfile`, so both run Jekyll 4.4.1 regardless of the
host's own defaults. Only the Ruby patch differs (Actions tracks 3.4.x, Cloudflare's
image is 3.4.4), which does not affect output.

## Config layering

The only difference between the targets is where the site sits on its domain.

| File | Role |
| --- | --- |
| `_config.yml` | Base config **plus GitHub Pages values** — `url: https://tiennm99.github.io`, `baseurl: /penny-pincher-provider`. |
| `_config.cloudflare.yml` | Overrides for the pages.dev root — `baseurl: ""`. Layered on top, never used alone. |

```sh
bundle exec jekyll build                                        # GitHub Pages
bundle exec jekyll build --config _config.yml,_config.cloudflare.yml   # Cloudflare
```

Order matters: later files win. `_config.cloudflare.yml` is excluded from the site
output.

## GitHub Pages setup

One repo setting, once: **Settings → Pages → Source → GitHub Actions**. Without it
the workflow's deploy step fails.

The workflow deliberately does not use `actions/configure-pages` — that action
rewrites `baseurl` with its own guess, which would fight the explicit value in
`_config.yml`.

## Cloudflare Pages setup

The Pages project is connected to this repository through Cloudflare's Git
integration, so Cloudflare builds and deploys on its own. There is deliberately no
Actions workflow for Cloudflare — that would deploy a second time on every push and
race the Git integration.

Dashboard settings, under the project's **Settings → Build**:

| Setting | Value |
| --- | --- |
| Build command | `bundle exec jekyll build --config _config.yml,_config.cloudflare.yml` |
| Build system version | **v3** — v2 ships Ruby 3.2.2, which is end-of-life. |

The build command must carry the `--config` flag. Cloudflare's Jekyll preset runs a
plain `jekyll build`, which uses `_config.yml` alone and bakes in the GitHub Pages
`baseurl` — every asset URL on pages.dev would then 404 and the page would render
unstyled.

The build output directory needs no dashboard entry: `pages_build_output_dir` in
`wrangler.jsonc` supplies it, and the wrangler file takes precedence for
Git-integrated builds.

No API token or account ID is needed anywhere — Cloudflare pulls the repository
itself.

## Building locally

Requires Ruby 3.4.x with Bundler (3.4.8 is what this project was developed
against). Jekyll does not yet support Ruby 4.0 — do not upgrade past the 3.4 branch.

```sh
bundle config set --local path .bundle/gems   # first time only
bundle install
JEKYLL_ENV=production bundle exec jekyll build
```

Gems install into the gitignored `.bundle/` inside the repo rather than the shared
rbenv gem home, keeping the project self-contained.

To preview what Cloudflare will publish, add the config flag:

```sh
JEKYLL_ENV=production bundle exec jekyll build --config _config.yml,_config.cloudflare.yml
```

Deploying by hand is not possible: `wrangler pages deploy` performs a direct upload,
which a Git-connected project rejects. Push to `main` instead.

## Notes

- `Gemfile.lock` is committed. It was generated on aarch64 but its `PLATFORMS` list
  includes `x86_64-linux-gnu`, which is what GitHub runners use — without that entry
  CI installs would fail. Re-check it after any `bundle update`.
- `_config.yml` excludes `README.md` from the output. It is still the site's
  content, pulled into `index.md` by `include_relative`, which reads excluded files
  fine — the exclusion only stops the raw markdown shipping as a duplicate page.
- `404.html` is served automatically by both hosts for unmatched routes.
- Ruby is pinned to the `3.4` series in both workflows rather than an exact patch.
  Cloudflare's own build image is irrelevant here, since Actions does the building.
