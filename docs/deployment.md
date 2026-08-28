# Deployment

The site is a Jekyll build of `README.md` (via `index.md`), published to two hosts
from the same source. Both deploy from GitHub Actions on every push to `main`.

| Target | URL | Workflow |
| --- | --- | --- |
| GitHub Pages | <https://tiennm99.github.io/penny-pincher-provider> | `.github/workflows/github-pages.yml` |
| Cloudflare Pages | <https://penny-pincher-provider.pages.dev> | `.github/workflows/cloudflare-pages.yml` |

Both workflows build with this repo's `Gemfile` (Jekyll 4.4.1 on Ruby 3.4), so the
two sites cannot drift apart on toolchain.

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

The project must be **Direct Upload**, not Git-connected. A Git-connected project
would build on every push as well, deploying twice and racing the workflow.

1. Create the project once, either in the dashboard (**Workers & Pages → Create →
   Pages → Upload assets**, named `penny-pincher-provider`) or locally:

   ```sh
   npx wrangler pages project create penny-pincher-provider --production-branch main
   ```

2. Add two repository secrets under **Settings → Secrets and variables → Actions**:

   | Secret | Where to get it |
   | --- | --- |
   | `CLOUDFLARE_API_TOKEN` | My Profile → API Tokens → Create Token, with the **Cloudflare Pages: Edit** permission. |
   | `CLOUDFLARE_ACCOUNT_ID` | Workers & Pages overview sidebar, or `npx wrangler whoami`. |

`wrangler.jsonc` supplies the project name and `pages_build_output_dir`, so the
workflow's `pages deploy` command needs no arguments.

## Building locally

Requires Ruby 3.4.x with Bundler (3.4.8 is what this project was developed
against). Jekyll does not yet support Ruby 4.0 — do not upgrade past the 3.4 branch.

```sh
bundle config set --local path .bundle/gems   # first time only
bundle install
JEKYLL_ENV=production bundle exec jekyll build
```

Gems install into the gitignored `.bundle/` inside the repo rather than the shared
rbenv gem home, keeping the project self-contained. To deploy to Cloudflare by hand,
build with the Cloudflare config and run `npx wrangler pages deploy` after
`npx wrangler login`.

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
