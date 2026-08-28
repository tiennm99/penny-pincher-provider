# Research Report: Stable Ruby Version for 1–2 Year Horizon

Conducted 2026-08-28. Context: local rbenv install + Cloudflare Workers build for this Jekyll site.

## Executive Summary

**Install Ruby 3.4.4.** Not 4.0, not 3.3, and not the 3.2.2 recommended earlier in this session
(3.2 hit EOL 2026-04-01).

Two constraints decide it, both external:

1. **Jekyll has no Ruby 4.0 support.** Jekyll 4.4.1 (Jan 2025, still latest) declares `>= 2.7.0`
   and recommends 3.2+. Theme gems constrained to `~> 3.1` fail version solving under 4.0.
2. **Cloudflare's build image defaults to Ruby 3.4.4.** Pinning anything else risks a build
   image that cannot supply it — and there is conflicting evidence that recent 3.4.x patches
   are unavailable (see Conflict below).

3.4 is the only branch in normal (non-security-only) maintenance that Jekyll actually supports.
Picking the exact patch Cloudflare defaults to gives local/CI parity for free.

## Methodology

- Sources: 5 (ruby-lang.org branches page, Cloudflare Workers build-image docs, 3 web searches)
- Date range: 2024-12 (Ruby 3.4.0) → 2026-07 (Ruby 4.0.6)
- Terms: ruby maintenance branches EOL, ruby 3.5/4.0 stable, jekyll ruby 4.0 compatibility,
  cloudflare workers build image RUBY_VERSION

## Key Findings

### 1. Ruby 3.5 does not exist — it shipped as 4.0

The version after 3.4 was renumbered. Ruby 4.0.0 released 2025-12-25; latest patch 4.0.6
(2026-07-14). Anyone searching for "Ruby 3.5 stable" finds only the April 2025 preview.

### 2. Branch status as of 2026-08-28

| Branch | Status | Released | EOL | Verdict |
| --- | --- | --- | --- | --- |
| 4.0 | Normal maintenance | 2025-12-25 | TBD (~2029-03) | Too early — Jekyll unsupported |
| 3.4 | Normal maintenance | 2024-12-25 | TBD (~2028-03) | **Pick this** |
| 3.3 | Security maintenance only | 2023-12-25 | 2027-03-31 | <1 yr left, no bug fixes |
| 3.2 | **EOL** | 2022-12-25 | 2026-04-01 | Dead — no security patches |

EOL dates for 3.4/4.0 are unpublished. Ruby's historical cadence is ~2 yrs normal + ~1 yr
security, so 3.4 EOL lands ~March 2028 — comfortably past a 2-year horizon. Treat as
convention, not commitment.

### 3. Jekyll compatibility

Jekyll 4.4.0 (Jan 2025) added Ruby 3.4 support; 4.4.1 is current. No Jekyll release has
declared Ruby 4.0 support. Community reports (chirpy theme issue #2640, Jan 2026) show
dependency resolution failing on 4.0. Ruby 3.4 moved `csv`, `base64`, `bigdecimal` to bundled
gems — this repo's `Gemfile` already declares them explicitly, so it is 3.4-ready as written.

### 4. Cloudflare build image

- Default Ruby **3.4.4**; OS Ubuntu 24.04; x86_64; Node 24.18.0.
- Override via `RUBY_VERSION` env var or `.ruby-version` file.
- Policy: minor versions may auto-update without notice; pin to avoid drift.

**Conflict:** the docs claim "all versions are available for override," but open issue
cloudflare-docs#27779 ("Recent Ruby versions aren't yet supported") reports 3.4.5–3.4.8
unavailable. Unresolved. Pinning 3.4.4 sidesteps it entirely — it is the default, so it is
guaranteed present.

### 5. Security

3.2 is EOL: no further CVE patches. Anything still on it should move. 3.3 gets security fixes
only until 2027-03-31 — inside the requested horizon, so it fails the 1–2 year test. 3.4 is the
oldest branch still receiving ordinary bug fixes.

## Recommendation

```sh
rbenv install 3.4.4
cd /config/workspace/tiennm99/penny-pincher-provider
rbenv local 3.4.4        # writes .ruby-version; Cloudflare reads the same file
```

Requires `libyaml-dev` present first (psych failure seen earlier this session).

Horizon: safe to ~March 2028 on 3.4. Revisit when Jekyll declares Ruby 4.0 support, or by
early 2028, whichever is first.

### Correction required in existing docs

`docs/cloudflare-deployment.md` (written earlier this session) states the build image ships
Ruby 3.2 and suggests `RUBY_VERSION=3.2.2`. Both wrong — default is 3.4.4. With a committed
`.ruby-version` the env-var fallback becomes unnecessary.

### Pitfalls

- Don't pin a 3.4.x newer than 3.4.4 until #27779 resolves.
- Don't rely on Cloudflare's default staying 3.4.4 — minors update without notice; the
  `.ruby-version` file is the pin.
- Ruby 4.0 local + Jekyll = dependency resolution failure, not a runtime error. Looks confusing.

## Sources

- [Ruby maintenance branches](https://www.ruby-lang.org/en/downloads/branches/)
- [Cloudflare Workers build image](https://developers.cloudflare.com/workers/ci-cd/builds/build-image/)
- [cloudflare-docs#27779 — recent Ruby versions unsupported](https://github.com/cloudflare/cloudflare-docs/issues/27779)
- [Jekyll 4.4.0 release notes](https://jekyllrb.com/news/2025/01/27/jekyll-4-4-0-released/)
- [chirpy#2640 — Add Ruby 4 support](https://github.com/cotes2020/jekyll-theme-chirpy/issues/2640)

## Unresolved

1. Exact EOL dates for 3.4 and 4.0 — unpublished; ~2028-03 / ~2029-03 inferred from cadence.
2. Whether Cloudflare actually rejects 3.4.5+ (docs vs. issue conflict). Untested.
3. Jekyll's Ruby 4.0 timeline — no roadmap statement found.
