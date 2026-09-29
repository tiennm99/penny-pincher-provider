# Free Providers audit (batch A): 13 entries, checked 2026-09-29

## Verdict

| Entry | Status | One-line reason |
|---|---|---|
| TokenRouter | UPDATE | Kimi K3 free ended (the model ID now returns 404). GLM 5.3's free week ended Sep 4. One $0 model is left. |
| OrcaRouter | UPDATE | All five dated offers are gone. Three deposit-match campaigns replaced them, and there is now a rotating set of $0 models. |
| OpenRouter | UPDATE | Limits unchanged (20 RPM, 50 or 1,000 RPD). Add the current `:free` lineup. |
| NVIDIA NIM | UPDATE | The model list changed completely. The "1,000 credits" claim cannot be verified. |
| OpenCode Zen | UPDATE | The free lineup changed. DeepSeek V4 Flash Free is gone from the docs. |
| Google AI Studio | UPDATE | The free lineup is now Gemini 3.x Flash and Flash-Lite. Gemini 2.5 is closed to new users. Google no longer publishes the limits. |
| Kilo Code Gateway | UPDATE | Still 200 req/hour per IP. The $20 first-top-up bonus was not found; Kilo Pass replaced it. Kilo was acquired by Anaconda. |
| Cloudflare Workers AI | UPDATE | Still 10k Neurons/day. The model list changed, some models now need a paid plan, and the "~150 responses" figure is wrong. |
| DeepSeek Platform | UPDATE | The model and pricing structure changed. The 5M signup tokens are not confirmed in official docs. |
| Groq | UPDATE | Both Llama models are now Enterprise-only. The free models are GPT-OSS, Qwen3.8-27B and Whisper. |
| GitHub Models | **STALE** | The service was fully retired on Jul 30, 2026. |
| xAI Grok API | UNVERIFIED | Official docs mention no free credits. Third-party sources disagree. Anthropic compatibility is deprecated. |
| Mistral La Plateforme | UPDATE | "Experiment ~1B tokens/month" is replaced by a Free plan with **$10/month in API credits**. |

Formatting note: TokenRouter and OrcaRouter used footnotes (`[^tokenrouter]: Check at ...`). The blocks below switch them to the `*Checked ...*` line that the other entries use, as requested. The CLAUDE.md footnote convention would then no longer be followed for these two entries. Your call.

---

## TokenRouter — UPDATE

```markdown
### [TokenRouter](https://www.tokenrouter.com/)

Unified AI gateway (145 models listed) exposing OpenAI-, Anthropic- and Gemini-format APIs behind one key.

- **Free model:** `nvidia/nemotron-3-nano-omni-30b-a3b-reasoning:free` at $0/M input and output.
- **Launch promos:** TokenRouter runs short free windows on self-hosted launches (e.g. GLM 5.3 was free for all accounts, no card, until Sep 4, 2026). Watch the [blog](https://www.tokenrouter.com/blog).
- **API:** OpenAI Chat Completions at `https://api.tokenrouter.com/v1` with a TokenRouter API key.

Source: [TokenRouter models](https://www.tokenrouter.com/models)

*Checked Sep 29, 2026.*
```

What changed:
- `moonshotai/kimi-k3-free` no longer exists; its model page returns 404. Kimi K3 is now paid at $1.80/M input and $9.00/M output.
- GLM 5.3 was free for one week, ending Sep 4, 2026. That promo has also expired.
- The models page shows 145 models, not "300+".
- The home page now advertises "OpenAI, Claude, and Gemini compatible APIs".

Sources: https://www.tokenrouter.com/models, https://www.tokenrouter.com/models/nvidia/nemotron-3-nano-omni-30b-a3b-reasoning%3Afree/, https://www.tokenrouter.com/models/moonshotai/kimi-k3/, https://www.tokenrouter.com/blog/tokenrouter-announces-day-0-availability-of-self-hosted-glm-5-3, https://www.tokenrouter.com/

## OrcaRouter — UPDATE

```markdown
### [OrcaRouter](https://www.orcarouter.ai/)

OpenAI-compatible gateway with access to 200+ models, automatic routing, and failover (also accepts Anthropic and Gemini formats).

> Referral: <https://www.orcarouter.ai/ref/ref_3976ba42abf37dc55c1d> (code: `ref_3976ba42abf37dc55c1d`).

- **Always-free models ($0):** `deepseek/deepseek-v4-flash-free`, `z-ai/glm-5.3-flash-free`, `tencent/hy4-preview-free`, `tencent/hy3-free`, plus the `orcarouter/free` router. Requires a linked GitHub account with some history, or any paid purchase.
- **Hy4 Deposit Match:** 100% match on top-ups for `tencent/hy4-preview` (min $20 top-up, up to $200), enroll by **Oct 28, 2026**.
- **DeepSeek V4.1 Flash Deposit Match:** 30% match (min $20 top-up, up to $100), enroll by **Oct 2, 2026**.
- **GPT-6 Astra Deposit Match:** 100% match for `openai/gpt-6-astra` (min $20, up to $100), card required, enroll by **Oct 5, 2026**.
- **API:** `https://api.orcarouter.ai/v1`.

Offers can change quickly; check the [live offers page](https://www.orcarouter.ai/offers) before claiming.

*Checked Sep 29, 2026.*
```

What changed:
- All five previous offers are gone from the live offers API. That covers the Kimi K3 $5, Tencent HY3 $5, Claude Opus 5 60% match, DeepSeek 100/30 calls, and the Grok 4.5 waitlist.
- Three deposit-match campaigns replaced them. They have start and end dates, and the match credit expires between Nov 4 and Nov 30, 2026.
- The dollar caps are my derivation. The API reports `reward_cap_quota` together with `quota_per_unit: 500000`: 100M ÷ 500k = $200, and 50M ÷ 500k = $100.
- The FAQ now says the $0 models need account history: "the workspace owner links a GitHub account with some history ... or the workspace makes a paid purchase of any amount".
- `/v1/models` lists 204 models. The `orcarouter/free` router supports the openai, openai-response, anthropic and gemini endpoint types.

Sources: https://www.orcarouter.ai/api/offers (JSON), https://api.orcarouter.ai/v1/models, https://www.orcarouter.ai/offers, https://www.orcarouter.ai/llms.txt

## OpenRouter — UPDATE

```markdown
### [OpenRouter](https://openrouter.ai)

Free models (`:free` suffix): 20 RPM, 50 req/day; 1,000 req/day once you have bought at least $10 in credits (all time). BYOK requests are not gated by the free-model cap.

Current free lineup includes NVIDIA Nemotron 3 Ultra 550B / Super 120B / 3.5 Lightning, Google Gemma 4 (26B-A4B, 31B), Qwen3.8-27B, Poolside Laguna S/XS 2.1, Thinking Machines Inkling / Inkling Small, Cohere North Mini Code, plus the `openrouter/free` auto-router. OpenAI-compatible at `https://openrouter.ai/api/v1`.

*Checked Sep 29, 2026.*
```

What changed:
- The limits are the same. The docs constants are `FREE_MODEL_RATE_LIMIT_RPM=20`, `FREE_MODEL_NO_CREDITS_RPD=50`, `FREE_MODEL_HAS_CREDITS_RPD=1e3` and `FREE_MODEL_CREDITS_THRESHOLD=10`.
- The docs now say the tier depends on "credits purchased (all time)". An account with a negative balance can get 402 errors, even on free models.
- The models API returns 20 zero-priced entries out of 460 models. The model list is new information for this entry.

Sources: https://openrouter.ai/docs/api/reference/limits, https://openrouter.ai/api/v1/models

## NVIDIA NIM — UPDATE

```markdown
### [NVIDIA NIM](https://build.nvidia.com)

Free prototyping endpoints for NVIDIA Developer Program members, no credit card. Rate-limited per model (commonly ~40 RPM); NVIDIA does not publish a fixed quota and does not raise free-tier limits on request.

Models: Kimi K3, Kimi K2.6, DeepSeek V4.1 Flash, GLM 5.3 / 5.3 Flash, Nemotron 3 Ultra / Super / 3.5 Lightning, GPT-OSS-20B, Gemma 4 31B, Mistral Large. OpenAI-compatible at `https://integrate.api.nvidia.com/v1`.

**Warning:** Trial terms: use is logged and may be used to improve NVIDIA products — do not send personal or confidential data.

*Checked Sep 29, 2026.*
```

What changed:
- The model list is new. The public `/v1/models` endpoint returns 81 models. Kimi K2.5, GPT-OSS-120B and DeepSeek-V3.2 are no longer listed, and there are no Llama 3.x chat models apart from the 3.2 vision models.
- The "1,000 inference credits at signup" claim is unverified. Third-party trackers say the credit system was removed. Forum users were still asking for credit increases in Aug–Sep 2026, and the Trial ToS PDF still mentions credits. I removed the number instead of guessing.
- The ~40 RPM figure comes from community reports and forum thread titles. It is not official.
- On Sep 28, 2026, a forum user relayed a moderator saying there is "no official way ... to receive a rate limit increase on that same tier".
- The privacy warning is new. The logging language comes from the NVIDIA trial terms, as quoted on the OpenCode Zen and Kilo docs pages.

Sources: https://integrate.api.nvidia.com/v1/models, https://docs.api.nvidia.com/nim/docs/api-catalog-quickstart-guide, https://forums.developer.nvidia.com/t/rate-limit-increase-request-40-rpm-200-rpm-build-nvidia-com-free-tier/384546, https://assets.ngc.nvidia.com/products/api-catalog/legal/NVIDIA%20API%20Trial%20Terms%20of%20Service.pdf, https://yangmao.ai/en/providers/nvidia-build/, https://kilo.ai/docs/gateway/models-and-providers

## OpenCode Zen — UPDATE

```markdown
### [OpenCode Zen](https://opencode.ai/docs/zen)

Hand-picked free models that change periodically (each is "free for a limited time"). Optimized for coding agents.

| Model | Model ID | Notes |
|---|---|---|
| Big Pickle | `big-pickle` | Stealth model; data may be used to improve it |
| Space Bunny Free | `space-bunny-free` | Stealth model; zero-retention provider |
| LongCat 2.5 Preview Free | `longcat-2.5-preview-free` | Zero-retention provider |
| MiMo-V2.6-Flash Free | `mimo-v2.6-flash-free` | Data may be used to improve the model |
| MiMo-V2.5 Free | `mimo-v2.5-free` | Data may be used to improve the model |
| Ling 3.0 Flash Fin Free | `ling-3.0-flash-fin-free` | Data may be used to improve the model |
| Nemotron 3 Ultra Free | `nemotron-3-ultra-free` | NVIDIA trial endpoint; logged |
| Nemotron 3.5 Lightning Free | `nemotron-3.5-lightning-free` | NVIDIA trial endpoint; logged |
| Muse Spark 1.3 Contributor Free | `muse-spark-1.3-contributor-free` | Prompts used to train Meta models |

OpenAI-compatible at `https://opencode.ai/zen/v1/chat/completions` (plus `/v1/responses`); Anthropic-format models use `https://opencode.ai/zen/v1/messages`. Model format in opencode: `opencode/<model-id>`.

*Checked Sep 29, 2026.*
```

What changed:
- DeepSeek V4 Flash Free is no longer in the docs' free list or pricing table. The ID `deepseek-v4-flash-free` still appears in `/zen/v1/models`, so it may just be unlisted.
- Six free models were added: Space Bunny, LongCat 2.5 Preview, MiMo-V2.6-Flash, Ling 3.0 Flash Fin, Nemotron 3.5 Lightning and Muse Spark 1.3 Contributor.
- The privacy notes are new, taken from the docs' privacy section.
- `jev-1.13-free` is also free. I left it out because it uses a specialised `/zen/v1/systemone` classification API, not chat.

Sources: https://opencode.ai/docs/zen, https://opencode.ai/zen/v1/models

## Google AI Studio — UPDATE

```markdown
### [Google AI Studio](https://aistudio.google.com/)

Google's developer platform for Gemini models. Free tier (no billing) with pay-as-you-go available.

Free-tier models: Gemini 3.8 / 3.7 / 3.6 / 3.5 Flash, Gemini 3.5 Flash-Lite, Gemini 3.1 Flash-Lite, Gemini 3 Flash Preview, plus Live/TTS variants and Gemma 4. **Gemini 3.1 Pro Preview is paid-only.** Gemini 2.5 models are now limited to projects that already used them.

Google no longer publishes a fixed free-tier table — limits are per project and shown in AI Studio. Reported Sep 2026: ~20 RPD on the 3.x Flash models, ~500 RPD on 3.5 / 3.1 Flash-Lite. RPD resets at midnight Pacific.

OpenAI-compatible endpoint: `https://generativelanguage.googleapis.com/v1beta/openai/`.

**Warning:** In the Free tier, Google may use your prompts and responses to improve their products. Use the Paid tier or Vertex AI for privacy.

*Checked Sep 29, 2026.*
```

What changed:
- The 2.5 Pro/Flash/Flash-Lite RPM/RPD table is gone. The official rate-limits page (updated 2026-09-02) no longer lists free-tier numbers and says to "View your active rate limits in AI Studio".
- The official pricing page marks these as "Free of charge" on the free tier: 3.8, 3.7, 3.6 and 3.5 Flash, 3.5 Flash-Lite, 3.1 Flash-Lite, 3 Flash Preview, and 2.5 Pro/Flash/Flash-Lite. 3.1 Pro Preview is "Not available" on the free tier.
- Changelog, Sep 18, 2026: "limiting access to the 2.5 models to users who have actively used them in the past." New users should treat 3.x as the free lineup.
- The ~20 and ~500 RPD figures come from third-party pages that say they were read from AI Studio. They are not official.
- The privacy row still says "Used to improve our products: Yes (Free) / No (Paid)".

Sources: https://ai.google.dev/gemini-api/docs/pricing, https://ai.google.dev/gemini-api/docs/rate-limits, https://ai.google.dev/gemini-api/docs/changelog, https://ai.google.dev/gemini-api/docs/openai, https://www.scriptbyai.com/gemini-api-free-tier-limits/, https://github.com/robhunter/agentdeals/issues/2017

## Kilo Code — Gateway — UPDATE

```markdown
### [Kilo Code — Gateway](https://kilo.ai/gateway)

VS Code + JetBrains coding extension (and CLI) with a built-in OpenAI-compatible gateway at `https://api.kilo.ai/api/gateway`. Kilo was acquired by Anaconda.

Free: `:free` models and the `kilo-auto/free` router, 200 req/hour per IP (anonymous or signed in). Current free models include Nemotron 3 Ultra / Super / 3.5 Lightning, Qwen3.8-27B, Laguna S/XS 2.1, Inkling Small, North Mini Code, and Step 3.7 Flash.
BYOK supported with no Kilo markup. Kilo Pass ($19/$49/$199 per month) adds up to 50% bonus credits.

**Warning:** Auto Free may route to providers that log prompts and use them for training (including NVIDIA trial endpoints).

*Checked Sep 29, 2026.*
```

What changed:
- The "first top-up: $20 bonus credits (60-day expiry)" offer does not appear on the pricing or gateway pages. The bonus mechanism is now Kilo Pass.
- The base URL and the `kilo-auto/free` router are new information. The gateway models API returns 19 zero-priced entries.
- There is a new data-handling warning in the docs.
- There is an Anaconda acquisition banner on every page.

Sources: https://kilo.ai/docs/gateway, https://kilo.ai/docs/gateway/models-and-providers, https://kilo.ai/docs/gateway/usage-and-billing, https://kilo.ai/pricing, https://api.kilo.ai/api/gateway/models

## Cloudflare Workers AI — UPDATE

```markdown
### [Cloudflare Workers AI](https://developers.cloudflare.com/workers-ai/)

10,000 Neurons/day free on both Workers Free and Paid (resets 00:00 UTC). Roughly ~49K output tokens/day on Llama 3.3 70B or ~147K on GPT-OSS-120B.

Models: GPT-OSS 120B/20B, Kimi K2.5, Llama 3.3 70B, Llama 4 Scout, Gemma 4 26B, Qwen3.8-27B, Nemotron 3 120B, GLM-4.7-Flash, Mistral Small 3.1, BGE embeddings, Whisper. Kimi K2.6/K2.7-Code, GLM 5.x and DeepSeek V4 require Workers Paid or AI Gateway credits.

OpenAI-compatible at `https://api.cloudflare.com/client/v4/accounts/<ACCOUNT_ID>/ai/v1`.

*Checked Sep 29, 2026.*
```

What changed:
- The allocation is unchanged.
- The "~150 LLM responses/day" figure had no basis in the docs. I replaced it with token figures computed from the published neuron rates:
  - Llama 3.3 70B uses 204,805 neurons per million output tokens, so 10k neurons buys about 48.8K output tokens.
  - GPT-OSS-120B uses 68,182 neurons per million output tokens, so 10k neurons buys about 147K.
- There is a new note that some models need a paid billing method.
- The model list was refreshed. Qwen2.5-Coder, Gemma 3 and DeepSeek-R1-distill are still listed but are older.
- The OpenAI-compatible base URL is new information.

Sources: https://developers.cloudflare.com/workers-ai/platform/pricing/, https://developers.cloudflare.com/workers-ai/configuration/open-ai-compatibility/

## DeepSeek Platform — UPDATE

```markdown
### [DeepSeek Platform](https://platform.deepseek.com)

New accounts are widely reported to get 5M free tokens (granted balance, ~30 days, phone verification); verify in your console. OpenAI (`https://api.deepseek.com`) + Anthropic (`https://api.deepseek.com/anthropic`) compatible.

PAYG (off-peak / peak, per 1M tokens): `deepseek-flash` (V4.1 Flash) $0.15/$0.30 in, $0.60/$1.20 out; `deepseek-v4-pro` $0.66/$1.32 in, $1.98/$3.96 out. Off-peak is half price — everything outside 01:00–04:00 and 06:00–10:00 UTC on weekdays. 1M context.

*Checked Sep 29, 2026.*
```

What changed:
- Model names changed. `deepseek-flash` is now DeepSeek-V4.1-Flash. The legacy `deepseek-v4-flash` name is still accepted but served by V4.1.
- Pro is now `DeepSeek-V4-Pro-0813`.
- Pricing moved to peak and off-peak rates. The old flat prices ($0.14/$0.28, $0.435/$0.87) are wrong.
- The official pricing page mentions a "granted balance" used before topped-up balance. It does not state a signup amount. The 5M-token figure is third-party only, so I added "verify in your console".

Sources: https://api-docs.deepseek.com/quick_start/pricing, https://api-docs.deepseek.com/, https://dev.to/tokenmixai/i-burned-through-deepseeks-5m-free-tokens-in-14-days-heres-the-exact-math-3n22, https://aicredits.dev/submissions/24-deepseek-5-million-free-tokens-for-new-users

## Groq — UPDATE

```markdown
### [Groq](https://console.groq.com)

LPU inference. Free plan, no credit card. OpenAI-compatible at `https://api.groq.com/openai/v1`.

| Model | RPM | RPD | TPM | TPD |
|---|---|---|---|---|
| `openai/gpt-oss-120b` | 30 | 1K | 8K | 200K |
| `openai/gpt-oss-20b` | 30 | 1K | 8K | 200K |
| `qwen/qwen3.8-27b` | 30 | 1K | 8K | 200K |
| `whisper-large-v3` / `-turbo` | 20 | 2K | — | 7.2K audio-sec/hour |

Llama 3.1 8B and Llama 3.3 70B are now Enterprise-only (contact sales).

*Checked Sep 29, 2026.*
```

What changed:
- Both Llama models are gone from the Free Plan table. The models page lists them as "Enterprise / Contact Sales".
- GPT-OSS 120B/20B and Qwen3.8-27B are the free chat models now.
- The table also lists Orpheus TTS and Prompt Guard models, which I omitted as niche.
- I did not independently confirm "no credit card" in the docs. It is carried over from the old entry.

Sources: https://console.groq.com/docs/rate-limits (and `.md` variant), https://console.groq.com/docs/models

## GitHub Models — STALE

This entry should be removed. There is no replacement block. GitHub points users to Microsoft/Azure AI Foundry, which is not free, and to GitHub Copilot, which the README already covers under Coding Plans. The Copilot Free tier is already mentioned there.

What changed:
- Jun 16, 2026: closed to new customers.
- Jul 30, 2026: fully retired. The playground, catalog, inference API and BYOK are all gone.

Sources: https://docs.github.com/en/github-models/use-github-models/prototyping-with-ai-models, https://github.blog/changelog/2026-07-30-github-models-is-now-retired/, https://github.blog/changelog/2026-07-01-github-models-is-being-fully-retired-on-july-30-2026/, https://github.blog/changelog/2026-06-16-github-models-is-no-longer-available-to-new-customers/

## xAI Grok API — UNVERIFIED (candidate for removal)

Use this block only if you want to keep the entry. I recommend removal unless you can confirm credits in console.x.ai.

```markdown
### [xAI Grok API](https://docs.x.ai)

No free tier is documented. Promotional signup credits and a data-sharing credit program have been reported by third parties but are not in xAI's docs — check console.x.ai before relying on them.

Models: Grok 4.7 (500K ctx, $2/$6 per 1M), Grok 4.3 (1M ctx, $1.25/$2.50), Grok Build 0.1 (coding, $1/$2). OpenAI-compatible (Responses API recommended); Anthropic SDK compatibility is deprecated.

**Warning:** If offered, Data Sharing opt-in is irreversible and lets xAI train on your prompts.

*Checked Sep 29, 2026.*
```

What changed:
- The official pricing, billing and full docs (`llms-full.txt`) never mention free, signup or data-sharing credits. Billing is prepaid credits or invoice only.
- Third-party sources disagree:
  - aitoolsrecap (corrected Sep 5, 2026) says $25 signup plus $150/month for data sharing is still active.
  - yangmao.ai (Jun 2026) says the data-sharing program should be treated as ended in May 2025.
- All three models in the README were retired on May 15, 2026: Grok 4 (`grok-4-0709`), Grok 4.1 Fast and Grok Code Fast. Their IDs now redirect to `grok-4.3` and `grok-build-0.1`.
- The docs now say "The Anthropic SDK compatibility is fully deprecated."
- The docs brand the company as "SpaceXAI (xAI)".

Sources: https://docs.x.ai/developers/pricing.md, https://docs.x.ai/docs/models, https://docs.x.ai/developers/migration/may-15-retirement.md, https://docs.x.ai/llms-full.txt, https://aitoolsrecap.com/Blog/how-to-get-free-grok-api-key-2026-step-by-step, https://yangmao.ai/en/questions/grok-api-free-credits/

## Mistral La Plateforme — UPDATE

```markdown
### [Mistral Studio (API)](https://console.mistral.ai)

Free plan (default for new accounts) includes **$10/month in API credits**, shared across Studio, the API, and Vibe Code; rate limits shown in the Admin Console. Enable pay-as-you-go to continue past the allowance. Pro ($14.99/month) includes $15/month in API credits.

Models: Mistral Medium 3.5, Mistral Large (2512), Mistral Small (2603), Devstral 2, Codestral, Ministral 3B/8B/14B, Voxtral, embeddings. OpenAI-compatible.

**Warning:** Model training on your data is opt-out, not opt-in.

*Checked Sep 29, 2026.*
```

What changed:
- The "Experiment plan, ~1B tokens/month" wording is outdated. The docs now describe "Free mode ... included monthly usage", and the pricing page says Free gets "$10 /mo in API credits".
- Plan structure: Free, Pro/Education, Team, Enterprise. Pro shows $15/month in API credits and Education $30/month. My reading of the rendered page may have swapped these two, so check the live page.
- The pricing table shows "Model training: Opt-out".
- Phone verification and "no credit card" were not confirmed in the current docs.
- I took the model names from OpenRouter's `mistralai/*` catalog because Mistral's model page did not render. Treat them as indicative.

Sources: https://mistral.ai/pricing, https://docs.mistral.ai/admin/billing-usage/usage-limits.md, https://docs.mistral.ai/admin/billing-usage/subscriptions.md, https://openrouter.ai/api/v1/models, https://pricepertoken.com/endpoints/mistral/free

---

## New free offers from these vendors worth noting

- **OpenCode Zen:** six new free models; see the table above.
- **Google:** Gemini 3.5 Flash-Lite and 3.1 Flash-Lite have the most generous free quota Google offers (reported at about 500 RPD).
- **TokenRouter:** runs a recurring pattern of one-week free windows on self-hosted model launches. None is live today.
- **OrcaRouter:** now has four always-free chat models (DeepSeek V4 Flash, GLM 5.3 Flash, Hy4 preview, Hy3), plus a free router.
- **Kilo and OpenRouter:** both carry the Nemotron 3 family and Qwen3.8-27B for free.

## Unresolved questions

1. **xAI:** keep the entry with the "no documented free tier" block, or remove it? Only a logged-in console.x.ai check can confirm the credits.
2. **NVIDIA NIM:** are signup credits still issued, or is it purely rate-limited now? This needs a logged-in check at build.nvidia.com.
3. **Google AI Studio:** the exact free RPM/RPD per model is only visible in a logged-in AI Studio project. Also, should the README still mention Gemini 2.5 for existing users?
4. **DeepSeek:** the 5M signup-token grant is not in official docs. Keep it with "verify", or drop it?
5. **Mistral:** does Free still require phone verification and no card? Is the Pro vs Education credit amount ($15 vs $30) right? Can the model names be confirmed from a Mistral-owned page?
6. **Groq:** "no credit card" is not restated in the current docs.
7. **OpenCode Zen:** is `deepseek-v4-flash-free` still callable at $0? It is in `/models` but not in the docs.
8. **Formatting:** should TokenRouter and OrcaRouter keep the CLAUDE.md footnote format, or use the `*Checked ...*` line as done here?
9. **Mistral heading:** should the heading be renamed from "La Plateforme" to "Mistral Studio"? The docs no longer use "La Plateforme". I proposed the rename, but you can keep the old title.
