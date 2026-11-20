# Free Providers audit (batch A): 20 entries, checked 2026-11-20

Two entries no longer offer anything free and should be removed: Hugging Face (free users now get no monthly credits) and Mistral (the Free plan lost its $10/month API credit in October). Vertex AI also changed materially: since Nov 16, 2026, the $300 trial credit no longer pays for the platform itself. Four entries are KEEP and the other 14 need updates, mostly to their free model lineups.

## Verdict

| Entry | Status | One-line reason |
|---|---|---|
| TokenRouter | UPDATE | The free Nemotron model is still $0. The catalog grew from 145 to 155 models. No new free promo is live. |
| OrcaRouter | UPDATE | All three dated offers ended. Two new deposit matches replaced them (DeepSeek V4.1 Flash and Fable 5.2), and `deepseek-v4.1-flash-free` joined the $0 models. |
| OpenRouter | UPDATE | Limits are unchanged (20 RPM, 50 or 1,000 RPD). The `:free` lineup turned over: Qwen3.8-27B, Laguna, Inkling and North Mini Code are gone. |
| NVIDIA NIM | UPDATE | `/v1/models` fell from 81 to 33 entries. Kimi K3, DeepSeek, GLM 5.3 and GPT-OSS-20B are gone (Kimi K3 is marked deprecated as of Oct 15, 2026). |
| OpenCode Zen | UPDATE | Renamed "OpenCode Console", with new `/inference/...` endpoints. Free chat models now work only from the OpenCode client. The free lineup changed. |
| Google AI Studio | UPDATE | Gemini 4 Hydrogen is new and free. 3.7 Flash and 3.5 Flash are deprecated. 2.5 Pro and 2.5 Flash re-route on Dec 1, 2026. Gemini 4 Carbon, Argon and Neon are paid-only. |
| Kilo Code — Gateway | UPDATE | The docs give a new base URL, `ai-gateway.kilo.ai/api/v1`. The free model lineup changed. The 200 req/hour per IP limit is unchanged. |
| Cloudflare Workers AI | UPDATE | Still 10k Neurons/day. The paid-only list now names GLM 5.3 Flash, DeepSeek V4.1 Flash / V4 Pro and Inkling 2 Small. |
| DeepSeek Platform | KEEP | Prices, base URLs and peak hours match the official page. The 5M signup-token claim is still unverified and stays hedged. |
| Groq | KEEP | The Free Plan table is identical to the README's. |
| Mistral Studio | **STALE** | The Free plan lost its $10/month API credit in October 2026. Mistral's pages now state no free API allowance. |
| Google Cloud Vertex AI | UPDATE | Now branded "Gemini platform". The $300 credit cannot pay for it for signups on or after Nov 16, 2026, so express mode is the only free path left. |
| Hugging Face Inference Providers | **STALE** | Free users now get "None" in monthly credits, so there is no free path. Routing now runs through OpenRouter. |
| Cerebras Cloud | UPDATE | The Qwen 3.8 27B free-trial limits rose to 300 RPM and 150K uncached TPM, with no daily cap. GPT-OSS-120B is unchanged. |
| Fireworks AI | UPDATE | The $1 credit and the 10 / 6,000 RPM limits are unchanged. Models: DeepSeek V4 Flash is now V4.1 Flash, and Kimi K3.1 Pro was added. |
| Scaleway Generative APIs | UPDATE | Renamed "Generative APIs - Serverless". The free tier (1M tokens + 60 min audio) is unchanged. GLM-5.3 and DeepSeek V4.1 Flash were added. |
| SambaNova Cloud | UPDATE | The free models are down to two (gpt-oss-120b, Gemma 4 31B). Developer tier is now 60 RPM / 12K RPD. |
| Cohere | KEEP | Trial limits, models and the compatibility URL are unchanged. |
| Vercel AI Gateway | UPDATE | The free tier and the payment-method requirement are unchanged. Add the $0 promo models now listed. BYOK needs purchased credits. |
| Requesty | KEEP | 200 req/day, no card, 600+ models, +5% fee and the router URL are all confirmed. |

## KEEP entries: what was confirmed

Each of these can have its Checked date bumped to Nov 20, 2026 with no text change. Claims marked "carried over" were not re-checked against a primary source this session.

- **DeepSeek Platform:** Both base URLs and the model names (`deepseek-flash` is now served by DeepSeek-V4.1-Flash-1017) are confirmed. So are all four prices ($0.15/$0.30 in and $0.60/$1.20 out for Flash; $0.66/$1.32 in and $1.98/$3.96 out for Pro), the half-price off-peak rule, the peak windows (01:00–04:00 and 06:00–10:00 UTC on weekdays) and the 1M context. The official page also makes Chinese public holidays off-peak, which is an optional addition. Carried over: the 5M signup tokens. The official page still mentions only an unspecified "granted balance".
- **Groq:** The Free Plan Limits tab (the default tab on `console.groq.com/docs/rate-limits`) matches the README row for row: gpt-oss-120b / 20b and qwen3.8-27b at 30 RPM, 1K RPD, 8K TPM and 200K TPD; whisper at 20 RPM, 2K RPD and 7.2K ASH. The models page still lists Llama 3.1 8B and 3.3 70B as "Enterprise / Contact Sales". Carried over: the "no card" claim, already hedged.
- **Cohere:** 1,000 calls/month on trial keys and 20 RPM per chat model are confirmed. So are Rerank at 10 RPM, Embed at 2,000 inputs/min, the note that prod keys get trial limits on newer variants, the model list and the compatibility URL (the docs show both `api.cohere.ai` and `api.cohere.com`). Carried over: "no credit card" and the exact "not permitted for production or commercial use" wording. The docs now say trial keys are "free but limited" and meant for proofs of concept.
- **Requesty:** 200 requests/day on free models, "No credit card required", 600+ models, the 5% markup and `https://router.requesty.ai/v1` are confirmed. Carried over: the Claude Code `ANTHROPIC_BASE_URL` line.

---

## TokenRouter — UPDATE

```markdown
### [TokenRouter](https://www.tokenrouter.com/)

Unified AI gateway (155 models listed) exposing OpenAI-, Anthropic- and Gemini-format APIs behind one key.

- **Free model:** `nvidia/nemotron-3-nano-omni-30b-a3b-reasoning:free` at $0/M input and output.
- **Launch promos:** TokenRouter runs short free windows on self-hosted launches (e.g. GLM 5.3 was free for all accounts, no card, until Sep 4, 2026). Watch the [blog](https://www.tokenrouter.com/blog).
- **API:** OpenAI Chat Completions at `https://api.tokenrouter.com/v1` with a TokenRouter API key.

Source: [TokenRouter models](https://www.tokenrouter.com/models)

*Checked Nov 20, 2026.*
```

What changed:
- The models page now says 155 models (it said 145).
- The free model page still shows $0.0000/M for both input and output.
- No new free promo is on the blog; GLM 5.3 is still the latest one.
- The base URL still answers (an unauthenticated call returns 401).

Sources: https://www.tokenrouter.com/models, https://www.tokenrouter.com/models/nvidia/nemotron-3-nano-omni-30b-a3b-reasoning%3Afree/, https://www.tokenrouter.com/blog

## OrcaRouter — UPDATE

The referral blockquote is unchanged and kept verbatim.

```markdown
### [OrcaRouter](https://www.orcarouter.ai/)

OpenAI-compatible gateway with access to 200+ models, automatic routing, and failover (also accepts Anthropic and Gemini formats).

> Referral: <https://www.orcarouter.ai/ref/ref_3976ba42abf37dc55c1d> (code: `ref_3976ba42abf37dc55c1d`).

- **Always-free models ($0):** `deepseek/deepseek-v4.1-flash-free`, `deepseek/deepseek-v4-flash-free`, `z-ai/glm-5.3-flash-free`, `tencent/hy4-preview-free`, `tencent/hy3-free`, plus the `orcarouter/free` router. Requires a linked GitHub account with some history, or any paid purchase.
- **DeepSeek V4.1 Flash "Unlimited" Deposit Match:** 100% match on top-ups for `deepseek/deepseek-v4.1-flash` (min $20 top-up, no cap listed), enroll by **Dec 18, 2026**; match credit expires Jan 17, 2027.
- **Fable 5.2 Deposit Match:** 100% match for `anthropic/claude-fable-5.2` (min $10 top-up, cap ≈$200 derived from API quota units), enroll by **Dec 11, 2026**; match credit expires Jan 10, 2027.
- **API:** `https://api.orcarouter.ai/v1`.

Offers can change quickly; check the [live offers page](https://www.orcarouter.ai/offers) before claiming.

*Checked Nov 20, 2026.*
```

What changed:
- All three previous offers ended: Hy4 (Oct 28), DeepSeek V4.1 Flash 30% (Oct 2) and GPT-6 Astra.
- The K3 + GLM 5.3 50% match (new users only, card required) came and went, ending Nov 15. It is omitted.
- There are two DeepSeek "Unlimited" campaigns. Only the newer one (ref c18) has `joinable: true`. The older one (c17, ending Dec 13) shows only a waitlist of 184, so I left it out.
- Caveat: every card reports `remaining: 0` to logged-out callers, and the meaning of that field is not documented. Readers should confirm on the live page.
- The Fable cap is my derivation: `reward_cap_quota` 100M ÷ `quota_per_unit` 500k = $200.
- New $0 model: `deepseek/deepseek-v4.1-flash-free`. `/v1/models` now lists 217 models.
- The FAQ wording about the GitHub-history requirement is unchanged.

Sources: https://www.orcarouter.ai/api/offers (JSON, server_time 2026-11-20), https://api.orcarouter.ai/v1/models, https://www.orcarouter.ai/offers, https://www.orcarouter.ai/llms.txt

## OpenRouter — UPDATE

```markdown
### [OpenRouter](https://openrouter.ai)

Free models (`:free` suffix): 20 RPM, 50 req/day; 1,000 req/day once you have bought at least $10 in credits (all time). BYOK requests are not gated by the free-model cap.

Current free lineup includes NVIDIA Nemotron 3 Ultra / 3.5 Super VL / 3.5 Lightning / 3 Nano Omni, Google Gemma 4 (26B-A4B, 31B), inclusionAI Ling 3.2 Flash, Baidu ERNIE 5.5 Flash Preview, Recursive Flint, Particle-1, LiquidAI LFM3-1.7B, Dots3-Note Preview, plus the `openrouter/free` auto-router. OpenAI-compatible at `https://openrouter.ai/api/v1`.

*Checked Nov 20, 2026.*
```

What changed:
- The limits table is unchanged.
- The free tier now shows as a `free_model_daily_requests` counter on `GET /api/v1/key`.
- The models API returns 15 zero-priced entries out of 477. This count includes two Lyria 3 music previews, which I omitted.
- Gone from the free list: Nemotron 3 Super 120B, Qwen3.8-27B, Laguna S/XS 2.1, Inkling / Inkling Small and North Mini Code.

Sources: https://openrouter.ai/docs/api/reference/limits.md, https://openrouter.ai/api/v1/models

## NVIDIA NIM — UPDATE

```markdown
### [NVIDIA NIM](https://build.nvidia.com)

Free prototyping endpoints for NVIDIA Developer Program members, no credit card. Rate-limited per model (commonly ~40 RPM per community reports); NVIDIA does not publish a fixed quota and does not raise free-tier limits on request.

Models: Kimi K3.1 Pro, MiniMax M3.1 Flash, Mistral Large 4, GLM 5.3 Flash, Step 5 Preview, Nemotron 3 Ultra / 3.5 Super VL / 3.5 Lightning / 3 Nano Omni, Gemma 4 31B, Laguna XS 2.1, Muse Glimmer 30B. OpenAI-compatible at `https://integrate.api.nvidia.com/v1`.

**Warning:** trial terms say use is logged and may be used to improve NVIDIA products — do not send personal or confidential data.

*Checked Nov 20, 2026.*
```

What changed:
- `/v1/models` returned 33 models on two fetches. I checked that this is not a partial response: Kimi K3's model page carries `isDeprecated: true` and says "no longer be supported after 10/15/2026". The GPT-OSS-20B page is also marked deprecated.
- GLM 5.3 (non-Flash) and DeepSeek V4.1 Flash return only the generic catalog page.
- Credits: an NVIDIA forum moderator wrote "We no longer use a credit-based system for build.nvidia.com", replaced by per-model rate limits that "we do not publish" (Sep 10, 2025; an earlier post dated Jun 24, 2025 says the same). This confirms the README's wording.
- The ~40 RPM figure is still community-sourced.
- Carried over: "no credit card".
- The old quickstart URL (`docs.api.nvidia.com/nim/docs/api-catalog-quickstart-guide`) now returns 404, so I no longer cite it.

Sources: https://integrate.api.nvidia.com/v1/models, https://build.nvidia.com/moonshotai/kimi-k3, https://forums.developer.nvidia.com/t/request-more-4-000-credits-option-on-build-nvidia-com/344567, https://forums.developer.nvidia.com/t/cannot-find-the-amount-of-credits-left-on-nim-api/337051, https://opencode.ai/docs/console/models/ (NVIDIA trial-endpoint privacy text)

## OpenCode Zen — UPDATE

The product is now called "OpenCode Console" (`/docs/zen` 301-redirects to `/docs/console/models/`). The block below renames the heading. Keep the old title if you prefer.

```markdown
### [OpenCode Console (formerly Zen)](https://opencode.ai/docs/console/models/)

Hand-picked free models that change periodically (each is "free for a limited time"). Optimized for coding agents. **Free-tier chat models only work from the OpenCode client**; other clients need paid models or Go.

| Model | Model ID | Notes |
|---|---|---|
| Big Pickle | `big-pickle` | Stealth model; data may be used to improve it |
| Iceman Free | `iceman-free` | Stealth model; data retained and used to improve it |
| DeepSeek V4.1 Flash Free | `deepseek-v4.1-flash-free` | Zero-retention provider |
| Hy4 flash Free | `hy4-flash-free` | Zero-retention provider |
| LongCat 2.5 Free | `longcat-2.5-free` | 100 req/day; zero retention; hosted in China |
| MiMo-V2.6-Flash Free | `mimo-v2.6-flash-free` | Feedback-collection period |
| Flint 40B Free | `flint-40b-free` | Data may be used to improve it; retained 30 days |
| Beam Free | `beam-free` | Not used for training; retained 30 days; region-restricted |
| Inkling 2 Small Free | `inkling-2-small-free` | Retained, may be used for training; not available in the EU |
| Nemotron 3.5 Lightning Free | `nemotron-3.5-lightning-free` | NVIDIA trial endpoint; logged |
| Nemotron 3.5 Super VL Free | `nemotron-3.5-super-vl-free` | NVIDIA trial endpoint; logged |

OpenAI-compatible at `https://opencode.ai/inference/openai/v1` (`/chat/completions`, `/responses`); Anthropic-format models use `https://opencode.ai/inference/anthropic/v1/messages`. Model format in opencode: `opencode/<model-id>`.

*Checked Nov 20, 2026.*
```

What changed:
- The endpoints moved from `/zen/v1/...` to `/inference/...`.
- New docs line: "Free-tier chat models require OpenCode; use paid models or Go from other clients."
- Gone from the free list: Space Bunny, LongCat 2.5 Preview (replaced by LongCat 2.5), MiMo-V2.5, Ling 3.0 Flash Fin, Nemotron 3 Ultra and Muse Spark 1.3 Contributor.
- The deprecation table shows GLM-5.3-Flash Free (Nov 18) and MiniMax M3.1 Flash Free (Nov 17).
- New: Iceman, DeepSeek V4.1 Flash, Hy4 flash, Flint 40B, Beam, Inkling 2 Small and Nemotron 3.5 Super VL.
- The docs and the API disagree in two places:
  - `inkling-2-small-free` is in the docs but not in `/models`.
  - `tidepool-alpha-free` ("Stealth reasoning model, free for a limited time") is in `/models` but not in the docs, so I left it out.
- I still exclude `jev-1.13-free`, because it uses the systemone classification API.

Sources: https://opencode.ai/docs/console/models/, https://opencode.ai/zen/v1/models

## Google AI Studio — UPDATE

```markdown
### [Google AI Studio](https://aistudio.google.com/)

Google's developer platform for Gemini models. Free tier (no billing) with pay-as-you-go available.

Free-tier models: Gemini 4 Hydrogen, Gemini 3.8 / 3.6 Flash, Gemini 3.5 / 3.1 Flash-Lite, Gemini 3 Flash Preview, plus TTS / Live / Transcribe variants, embeddings and Gemma 4. **Gemini 4 Carbon / Argon / Neon and Gemini 3.1 Pro Preview are paid-only.** Gemini 3.7 Flash and 3.5 Flash are deprecated (requests re-route to 3.8 / 3.6 Flash); Gemini 2.5 Pro and 2.5 Flash re-route to 3.8 Flash and 3.5 Flash-Lite on Dec 1, 2026.

Google no longer publishes a free-tier rate-limit table — limits are per project and shown in AI Studio. RPD resets at midnight Pacific. Some free projects need verification.

OpenAI-compatible endpoint: `https://generativelanguage.googleapis.com/v1beta/openai/`.

**Warning:** In the Free tier, Google may use your prompts and responses to improve their products. Use the Paid tier or Vertex AI for privacy.

*Checked Nov 20, 2026.*
```

What changed:
- From the pricing page (Free Tier column, "Free of charge"):
  - Free: Gemini 4 Hydrogen, 3.8 Flash, 3.6 Flash, 3.5 Flash-Lite, 3.1 Flash-Lite, 3 Flash Preview, Gemma 4, and the 2.5 models (for existing users).
  - Not available on free: 4 Carbon, 4 Argon, 4 Neon and 3.1 Pro Preview.
- From the changelog:
  - Nov 12, 2026: Gemini 4 Hydrogen GA, "Available on the free tier".
  - Oct 8, 2026: 3.7 Flash and 3.5 Flash deprecated.
  - Nov 2, 2026: 2.5 Pro and 2.5 Flash deprecated, with routing from Dec 1, 2026.
- I removed the third-party "~20 / ~500 RPD" figures. They dated from Sep 2026, predate Hydrogen and are not official. The rate-limits page publishes free-tier numbers only for Gemini Decision 1 (200 RPM / 10,000 RPD), a classification API.
- The privacy row ("Used to improve our products: Yes" on free) is unchanged.

Sources: https://ai.google.dev/gemini-api/docs/pricing, https://ai.google.dev/gemini-api/docs/rate-limits, https://ai.google.dev/gemini-api/docs/changelog

## Kilo Code — Gateway — UPDATE

```markdown
### [Kilo Code — Gateway](https://kilo.ai/gateway)

VS Code + JetBrains coding extension (and CLI) with a built-in OpenAI-compatible gateway at `https://ai-gateway.kilo.ai/api/v1`. Kilo was acquired by Anaconda.

Free: `:free` models and the `kilo-auto/free` router, 200 req/hour per IP (anonymous or signed in). Current free models include Nemotron 3 Ultra / 3.5 Super VL / 3.5 Lightning / 3 Nano Omni, Ling 3.2 Flash, ERNIE 5.5 Flash Preview, Flint, Beam 1.0, Particle-1, LFM3-1.7B and Dots3-Note Preview.
BYOK supported with no Kilo markup (5% processing fee on credit purchases). Kilo Pass ($19/$49/$199 per month) adds up to 50% bonus credits.

**Warning:** Auto Free may route to providers that log prompts and use them for training (including NVIDIA trial endpoints).

*Checked Nov 20, 2026.*
```

What changed:
- The gateway docs now give `https://ai-gateway.kilo.ai/api/v1` as the base URL. The old `api.kilo.ai/api/gateway` still returns 200 for `/models`.
- The free list was refreshed from 18 zero-priced entries in the models API. I omitted the Lyria music previews and two stealth or collaborator models (Glyph Cluster, Ampersand).
- Gone: Nemotron 3 Super, Qwen3.8-27B, Laguna, Inkling Small, North Mini Code and Step 3.7 Flash.
- The pricing page shows a "Credit purchase processing fee 5%". The 200/hour per-IP limit, the Kilo Pass tiers and the Auto Free warning are unchanged.

Sources: https://kilo.ai/docs/gateway, https://kilo.ai/docs/gateway/usage-and-billing, https://kilo.ai/docs/gateway/models-and-providers, https://kilo.ai/pricing, https://ai-gateway.kilo.ai/api/v1/models

## Cloudflare Workers AI — UPDATE

```markdown
### [Cloudflare Workers AI](https://developers.cloudflare.com/workers-ai/)

10,000 Neurons/day free on both Workers Free and Paid (resets 00:00 UTC). Roughly ~49K output tokens/day on Llama 3.3 70B or ~147K on GPT-OSS-120B.

Models: GPT-OSS 120B/20B, Kimi K2.5, Llama 3.3 70B, Llama 4 Scout, Gemma 4 26B, Qwen3.8-27B, Nemotron 3 120B, GLM-4.7-Flash, Mistral Small 3.1, BGE embeddings, Whisper. Kimi K2.6/K2.7-Code, GLM 5.2/5.3/5.3-Flash, DeepSeek V4 Flash/V4.1 Flash/V4 Pro and Inkling 2 Small require Workers Paid or AI Gateway credits.

OpenAI-compatible at `https://api.cloudflare.com/client/v4/accounts/<ACCOUNT_ID>/ai/v1`.

*Checked Nov 20, 2026.*
```

What changed:
- Only the paid-only sentence changed, now matching the docs' list exactly (Inkling 2 Small is new).
- The allocation, the reset time, every listed free model, the neuron rates behind the token estimates (204,805 and 68,182 neurons per M output) and the base URL are all confirmed.

Sources: https://developers.cloudflare.com/workers-ai/platform/pricing/, https://developers.cloudflare.com/workers-ai/configuration/open-ai-compatibility/

## Mistral Studio — STALE (recommend removal)

The Free plan no longer includes any free API allowance that Mistral documents.

What changed:
- The pricing page lists API credits only for paid plans: "$25.5 /mo in API credits" for Pro and "$15 /mo" for Education. I confirmed which is which from the page's `data-educational` toggle.
- The Free column has no credit line. The FAQ says only "On the Free plan, you also get access to Mistral Studio."
- The docs say "Paid plans add seats, features, and included monthly usage".
- PricingSaaS diffs (third-party corroboration only) record the change on Oct 5 → Oct 12, 2026: "Free plan loses $10/mo API credits and Studio model testing", and Pro credits went from $30 to $25.50.
- Mistral's two "try the API for free with the Experiment plan" help articles now return 404.

If you want to keep it, use this block. It could also move under Coding Plans, since Pro is a $14.99 Vibe subscription with included API credits.

```markdown
### [Mistral Studio](https://console.mistral.ai)

Formerly "La Plateforme". Free mode (default for new accounts) gives access to Mistral Studio, but no free API credit is advertised since Oct 2026 — check included usage in Admin Panel › Subscription. Pay-as-you-go is prepaid. Pro ($14.99/month) includes $25.50/month in API credits; Education includes $15/month.

Models (indicative): Mistral Medium, Mistral Large, Mistral Small, Devstral, Codestral, Voxtral, OCR, embeddings. OpenAI-compatible.

**Warning:** Model training on your data is opt-out, not opt-in.

*Checked Nov 20, 2026.*
```

Sources: https://mistral.ai/pricing, https://docs.mistral.ai/admin/billing-usage/subscriptions, https://pricingsaas.com/companies/mistral/diffs/2026W42, https://help.mistral.ai/en/articles/455206-how-can-i-try-the-api-for-free-with-the-experiment-plan (404)

## Google Cloud Vertex AI — UPDATE

```markdown
### [Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)

Now branded **Gemini platform** (formerly Gemini Enterprise Agent Platform / Vertex AI).

Express mode: `@gmail.com` accounts new to Google Cloud get a **90-day free tier with no billing info**, within express-mode quotas, on the APIs that support express mode (Gemini models). This is the only no-cost path for new users.

Free Trial: **$300** credit for 90 days (new GCP customers only; card or other payment method required). **For sign-ups or upgrades on or after Nov 16, 2026, the $300 credit cannot pay for Gemini platform services**; it also never covers partner models offered as MaaS (e.g. Claude) or Gemini API in AI Studio.

Partner models (Claude and others) need a paid billing account.

*Checked Nov 20, 2026.*
```

What changed:
- The Free Trial docs (updated 2026-11-13) say: "The $300 credit can't pay for Gemini platform (formerly known as Gemini Enterprise Agent Platform, Vertex AI) services if you sign up for a free trial or upgrade to a paid account on or after November 16, 2026."
- The product page title is now "Gemini platform". The express-mode doc (updated 2026-11-20) still offers the 90-day free tier without billing.
- I dropped the "Gemini 3.x (Pro / Flash / Flash-Lite)" model line. The current lineup is Gemini 4.x, and I did not check which models express mode supports.

Sources: https://cloud.google.com/free/docs/free-cloud-features, https://cloud.google.com/vertex-ai/generative-ai/docs/start/express-mode/overview, https://cloud.google.com/vertex-ai

## Hugging Face Inference Providers — STALE (recommend removal)

Remove the entry; there is no replacement block. The pricing docs' table now reads "Free Users | None | - | yes (credits purchase required)". PRO ($9/month) still includes $2.00/month in credits, but that is a paid subscription. The index page now says "Routing is powered by OpenRouter", and the router's model list spans 59 provider IDs, so the "20 partners" list is also stale. OpenRouter already has its own entry.

Sources: https://huggingface.co/docs/inference-providers/pricing, https://huggingface.co/docs/inference-providers/index, https://huggingface.co/pricing, https://router.huggingface.co/v1/models

## Cerebras Cloud — UPDATE

```markdown
### [Cerebras Cloud](https://cloud.cerebras.ai)

Wafer-scale chip inference. **Free Trial only**: **$5** in credits after adding a **verified payment method**, expiring 30 days after grant. No permanently free tier. OpenAI-compatible at `https://api.cerebras.ai/v1`.

| Model | RPM | Uncached TPM | Total TPM | Token caps | Context (free) |
|---|---|---|---|---|---|
| `gpt-oss-120b` | 5 | 30K | 90K | 1M/hour, 1M/day | 65K |
| `qwen-3.8-27b` | 300 | 150K | 750K (temporary; normally 450K) | none | 64K |

Qwen 3.8 27B has the same per-minute limits on Free Trial and Pay as You Go. Access stops when credits run out or expire until you buy credits.

*Checked Nov 20, 2026.*
```

What changed:
- Qwen 3.8 27B went from 5 RPM / 30K TPM / 1M TPD to 300 RPM / 150K uncached TPM / 750K total TPM, with "no hourly or daily token caps". Free Trial images are limited to 2 per request.
- The $5 credit, the verified-payment requirement, the 30-day expiry, GPT-OSS limits and context sizes are unchanged.

Sources: https://inference-docs.cerebras.ai/support/rate-limits, https://inference-docs.cerebras.ai/models/overview, https://inference-docs.cerebras.ai/models/qwen-3.8-27b

## Fireworks AI — UPDATE

```markdown
### [Fireworks AI](https://fireworks.ai)

**$1** in free starter credits for serverless inference. Without a payment method (or without credits) the account is capped at **10 RPM**; adding a payment method raises it up to 6,000 RPM.

Models: GLM 5.3 / 5.3 Flash, Kimi K3 / K3.1 Pro, DeepSeek V4.1 Flash, Qwen 3.8 27B / 3.8 Max and other open models. Function calling, MCP support.

OpenAI-compatible at `https://api.fireworks.ai/inference/v1`; Anthropic-compatible at `https://api.fireworks.ai/inference` (works with Claude Code).

*Checked Nov 20, 2026.*
```

What changed:
- The pricing page lists DeepSeek V4.1 Flash (1017) in place of V4 Flash, and adds Kimi K3.1 Pro and Qwen 3.8 Max.
- The $1 starter credit (billing FAQ), the 10 / 6,000 RPM limits and the Anthropic base URL are confirmed.
- Not added to the block: "Muse Glimmer 30B SFT is free through November 30". It is a fine-tuning promo, not inference.

Sources: https://docs.fireworks.ai/guides/quotas_usage/rate-limits, https://docs.fireworks.ai/faq-new/billing-pricing/what-happens-when-i-finish-my-1-dollar-credit, https://fireworks.ai/pricing, https://docs.fireworks.ai/tools-sdks/anthropic-compatibility

## Scaleway Generative APIs — UPDATE

```markdown
### [Scaleway Generative APIs](https://www.scaleway.com/en/generative-apis/)

Now "Generative APIs - Serverless". EU/GDPR, Paris. Free tier for new customers: first **1,000,000 tokens** plus **60 minutes** of audio transcription (no time limit advertised; applied to the most expensive tokens first). OpenAI-compatible at `https://api.scaleway.ai/v1`.

Models: GLM-5.3, GLM-5.2, DeepSeek V4.1 Flash, DeepSeek V4 Flash, Qwen3.8-27B, Qwen3.5-397B, Qwen3.6-35B, Qwen3-235B, Qwen3-Coder-30B, Gemma 4 26B, Mistral Medium 3.5, Mistral Small 3.2, gpt-oss-120b, Llama 3.3 70B, Pixtral 12B, Voxtral Small, Whisper.

*Checked Nov 20, 2026.*
```

What changed:
- New name per the FAQ: "Generative APIs - Serverless (formerly known as Scaleway Generative APIs)".
- New serverless models: GLM-5.3, DeepSeek V4.1 Flash and Voxtral Small. Gemma 3 27B is deprecated.
- Verification route: the live site returned 403 (a JavaScript challenge) to both curl and WebFetch. I verified against Scaleway's official docs repo on GitHub instead (`scaleway/docs-content`, FAQ committed 2026-11-06, supported-models committed 2026-11-18).
- Carried over: the "for new customers" eligibility. The FAQ just says "There is a Free Tier available for Serverless", and I could not read the pricing page.

Sources: https://github.com/scaleway/docs-content/blob/main/pages/generative-apis/faq.mdx, https://github.com/scaleway/docs-content/blob/main/pages/generative-apis/reference-content/supported-models.mdx

## SambaNova Cloud — UPDATE

```markdown
### [SambaNova Cloud](https://cloud.sambanova.ai)

RDU (dataflow chip) inference. **Free tier** applies when no payment method is linked: **20 RPM, 20 requests/day, 200K tokens/day** per model. Adding a card moves you to the Developer tier (pay-as-you-go, 60 RPM / 12,000 requests/day per model, 20M tokens/day across models). The $5 signup credit is no longer advertised, and the Plans page says to add a payment method and purchase credits first — the two official pages disagree.

Free-tier models: gpt-oss-120b, Gemma 4 31B. All SambaCloud models are labelled Preview (evaluation only, not for production).

OpenAI-compatible and Anthropic-compatible at `https://api.sambanova.ai/v1`.

Source: <https://docs.sambanova.ai/docs/en/models/rate-limits>

*Checked Nov 20, 2026.*
```

What changed:
- DeepSeek-V3.1, DeepSeek-V3.2 and Llama 3.3 70B are gone from both tier tables.
- Developer tier is now a flat 60 RPM / 12,000 RPD.
- The Plans page still reads "Free ... Add a payment method and purchase credits to run your first requests."
- Carried over: the base URL.

Sources: https://docs.sambanova.ai/docs/en/models/rate-limits, https://cloud.sambanova.ai/plans

## Vercel AI Gateway — UPDATE

```markdown
### [Vercel AI Gateway](https://vercel.com/docs/ai-gateway)

Single endpoint routing to many providers, with failover and BYOK (BYOK needs purchased credits). OpenAI-compatible at `https://ai-gateway.vercel.sh/v1`; also Anthropic Messages, OpenResponses and Cohere-compatible APIs.

Free: a **monthly included credit** (reported as **$5 / 30 days**; does not roll over), starting with your first request. **Requires a valid payment method on the team.** Covers only free-tier-eligible models with lower per-model rate limits. Buying credits moves you to the paid tier permanently and the monthly free credit stops. $0 promo models currently listed: Reflection Beam 1.0, NVIDIA Nemotron 3.5 Lightning, Recursive Flint, Ampersand v0.1 and the stealth Glyph Cluster.

Source: <https://vercel.com/docs/ai-gateway/pricing>

*Checked Nov 20, 2026.*
```

What changed:
- The getting-started page says: "To use free AI Gateway Credits, add a valid payment method to your team."
- The pricing page says: "BYOK is available on the paid tier ... you'll need purchased AI Gateway Credits."
- The models API has 6 zero-priced IDs, five distinct models (`beam` and `beam-free` are the same model). The marketing page lists "28 live" promotions.
- Carried over: the $5 amount. It appears on no Vercel page I fetched.

Sources: https://vercel.com/docs/ai-gateway/pricing, https://vercel.com/docs/ai-gateway/getting-started, https://vercel.com/ai-gateway, https://ai-gateway.vercel.sh/v1/models

---

## Unresolved questions

1. **Mistral:** remove it, keep the fallback block, or move it to Coding Plans as a $14.99 Pro subscription with API credits? Only a logged-in Admin Panel check can show whether Free mode still has any included API usage.
2. **Hugging Face:** remove it outright? Nothing is free for free users now.
3. **OpenCode:** rename the heading to "OpenCode Console (formerly Zen)"? Since free models now work only from the OpenCode client, does the entry still fit a list of free *API* providers?
4. **OrcaRouter:** what does `remaining: 0` mean on every offer card? It needs a logged-in check before readers rely on the two deposit matches.
5. **Vercel:** the $5 / 30-day figure is not stated in any Vercel doc. Keep "reported as", or drop the amount?
6. **DeepSeek, Groq, NVIDIA, Cohere:** the 5M signup tokens and the various "no card" claims remain unverified from primary sources, as in the last audit.
7. **Scaleway:** the live pricing page blocks automated fetches. The "new customers" eligibility needs a manual browser check.

Status: DONE_WITH_CONCERNS
Summary: Re-verified all 20 entries against primary sources: 4 KEEP, 14 UPDATE, 2 STALE (Hugging Face and Mistral lost their free tiers). Vertex AI's $300 credit no longer pays for the platform for signups on or after Nov 16, 2026.
Concerns/Blockers: Scaleway's site returned 403, so it was verified from the official docs repo. Several "no card", signup-grant and Vercel $5 claims stay unverified and carried over. The OrcaRouter offer availability semantics and the Mistral Free-mode API allowance need a logged-in check.
