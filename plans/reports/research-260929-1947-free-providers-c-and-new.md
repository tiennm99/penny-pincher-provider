# Research: Free Providers (batch C) refresh + new free/cheap LLM APIs

Date: 2026-09-29 (Asia/Saigon). Scope: 13 existing README entries (LongCat … Empero) plus discovery of new providers.
Method: official pages, official docs, and anonymous `GET /v1/models` calls (no prompts sent) made this session.
Secondary sources (the peter123023 and mnfst lists, blogs) were used only to find candidates, never as the sole basis for a figure.
`cheahjs/free-llm-api-resources` now returns **404** (the repo was deleted or made private), so it was not usable.

## Summary

| Entry | Status | One-line reason |
|---|---|---|
| LongCat (Meituan) | **STALE** | Official docs no longer mention a free daily quota; paid billing (token packs + PAYG) launched 2026-06-30 |
| SenseNova Token Plan | UPDATE | Free ¥0 beta confirmed; official page lists only SenseNova 6.8 Flash Lite + U1 Fast |
| AMD Token Factory | UPDATE | Free catalogue changed (8 free + 1 limited-free); daily quota figure not published publicly |
| Volcengine Ark | **STALE** | "2M tokens/day permanent free" is really a data-sharing rebate on *paid* usage; its term ends 2026-09-30 |
| Baidu Qianfan | **STALE** | ERNIE-Speed-128K / ERNIE-Lite-8K retired 2026-01-27 (official retirement doc) |
| iFlytek Spark | UPDATE | Lite still free; auth is `Bearer <APIPassword>`, 8K in / 4K out |
| AIHubMix | UPDATE | Now 60 free models; after the $1 top-up the limits are 100 req/day, 10 req/min, 1M tokens/day |
| OVHcloud AI Endpoints | UPDATE | Anonymous 2 RPM confirmed; model list refreshed |
| LLM7.io | UPDATE | Official limits and the free (`turbo`) model list changed |
| Token Harbor | UPDATE | Free models now DeepSeek V4.1 Flash, MiMo V2.6 Flash, TH-Rudder; Agent Pass includes $10 usage |
| Aion Labs | UPDATE | Limits unchanged; aion-3.5 / 3.5-mini added |
| Experiential Labs | UPDATE | Free credits are 100 (= $1) per 30 days after a $1 card verification, not ~500 |
| Empero | **STALE** | `/v1/models` returns 503 `maintenance`: "The endpoint is offline for now" |

Proposed additions, ranked by usefulness for coding agents: **NanoGPT Pro**, **Tencent TokenHub**, **Alibaba Model Studio free quota**, **Z.ai free Flash models**, **Nebius Token Factory**, **Novita free models**.

---

## Existing entries

### LongCat (Meituan) — STALE

Evidence:
- The official quick-start, FAQ, token-pack and pricing pages contain no free daily quota.
- The FAQ mentions only "活动赠送额度" (promotional gift credit), with no amount given.
- The changelog entry for 2026-06-30 reads "全新推出计费服务" (billing service launched): Token 资源包 (one-time token packs, valid 30 days, sold in limited daily flash sales at 10:00/16:00/21:00/23:00 CST) plus API 按量付费 (pay-as-you-go).
- Introductory PAYG price is ¥2 / ¥8 per 1M tokens (in / out), or $0.30 / $1.20. Cache hits cost ¥0.04 / $0.006.
- Models are now **LongCat-2.5-Preview** (added 2026-09-25, multimodal) and **LongCat-2.0**, both with 1M context and 128K max output.
- The old free Flash models were retired on 2026-05-29.
- The endpoint is alive: `https://api.longcat.chat/openai/v1/models` returns 401.

Recommendation: remove the entry from Free Providers. If you want to keep it as a cheap PAYG option instead, use this block:

```markdown
### [LongCat (Meituan)](https://longcat.chat/platform/docs/zh/)

Meituan's API platform for **LongCat-2.5-Preview** (multimodal) and **LongCat-2.0** (1M context, 128K max output).
**OpenAI** (`https://api.longcat.chat/openai`) and **Anthropic** (`https://api.longcat.chat/anthropic`) formats — works with Claude Code.

No standing free tier since paid billing launched (Jun 30, 2026). Pay-as-you-go launch price **$0.30 in / $1.20 out per 1M**
(cache hits $0.006/M); 30-day token packs sold in limited daily drops. Failed requests (401/403/429/500) are not billed.
Mainland-China users need real-name verification before paying.

Source: <https://longcat.chat/platform/docs/zh/api-pay-as-you-go>, <https://longcat.chat/platform/docs/zh/change-log>

*Checked Sep 29, 2026.*
```

Sources: <https://longcat.chat/platform/docs/zh/>, <https://longcat.chat/platform/docs/zh/faq>, <https://longcat.chat/platform/docs/zh/token-pack>, <https://longcat.chat/platform/docs/zh/change-log>

### SenseNova Token Plan — UPDATE

What changed:
- The official Token Plan page confirms "公测期完全免费开放，付费档位即将上线" (free during the public beta; paid tiers coming soon).
- It shows **Free ¥0/month**, **60,000 credits / 5 hours**, SenseNova 6.8 Flash Lite and SenseNova U1 Fast, and up to 20 API keys.
- The **600,000 credits/week** cap and the third-party models (DeepSeek V4, GLM-5.2, Kimi K3) do not appear on the official page. They come only from the peter123023 list.
- The peter123023 list removed SenseNova as a DeepSeek V4 Flash channel on 2026-09-22.
- The endpoint is alive: `https://token.sensenova.cn/v1/models` returns 401.

```markdown
### [SenseNova Token Plan](https://www.sensenova.cn/token-plan)

SenseTime (商汤). Public beta — **Free tier ¥0/month**, phone-number signup, no card.
OpenAI-compatible at `https://token.sensenova.cn/v1` plus an Anthropic-compatible endpoint.

Limits: **60,000 credits / 5 h** (special models excepted). Up to 20 API keys.

Models: SenseNova 6.8 Flash Lite (multimodal agent model) and SenseNova U1 Fast. Third-party models
(DeepSeek, GLM, Kimi) have been reported at 0 credits but are not listed on the official plan page.

**Warning:** SenseTime says paid Lite/Pro tiers are "coming soon" with no end date for the free beta —
don't build production on it.

Source: <https://www.sensenova.cn/token-plan>

*Checked Sep 29, 2026.*
```

Sources: <https://www.sensenova.cn/token-plan>, <https://www.sensenova.cn/models>

### AMD Token Factory (Radeon Cloud) — UPDATE

What changed:
- The live catalogue section `public_free` ("Public Free Model APIs") lists these models with badge **Free**: MiMo-V2.6-Flash, DeepSeek-V4.1-Flash, DeepSeek-V4-Flash, DeepSeek-V4-Flash-Vision-Exp, GLM-5.3-Flash, Qwen3.8-Flash-Next, Qwen3.8-27B and MiniCPM5-2B.
- MinerU2.5-Pro is listed as **Limited Free**.
- MiniCPM5-1B is gone from the list.
- Each model card says "Free to use. Points show relative usage—not a charge."
- The "~$10/day" quota is **not published** on any public page I could reach; it comes from the peter123023 list only.
- The base URL `https://developer.amd.com.cn/radeon/api/v1` is confirmed by the model cards and returns 401 without a key.

```markdown
### [AMD Token Factory (Radeon Cloud)](https://developer.amd.com.cn/radeon/tokenfactory)

AMD's official inference platform on Radeon GPUs. Free shared endpoints after sign-in; usage is metered in
"points" against a daily allowance (reported as ~$10-equivalent/day, resets daily — not stated on the public page).
OpenAI-compatible at `https://developer.amd.com.cn/radeon/api/v1`.

Free models: DeepSeek-V4.1-Flash, DeepSeek-V4-Flash (+ Vision-Exp), MiMo-V2.6-Flash, GLM-5.3-Flash, Qwen3.8-Flash-Next,
Qwen3.8-27B, MiniCPM5-2B (1M context on the DeepSeek/MiMo models). Marked "experimental" stability; high
time-to-first-token has been reported.

Source: <https://developer.amd.com.cn/radeon/tokenfactory>

*Checked Sep 29, 2026.*
```

Sources: <https://developer.amd.com.cn/radeon/tokenfactory> (its catalogue JSON loads from `/radeon/api/tokenfactory/bootstrap`)

### Volcengine Ark (ByteDance) — STALE

Evidence from the official "协作奖励计划" (collaboration reward plan) doc, updated 2026-09-21:
- The plan is not a free tier. When you authorise data collection, Ark returns up to **5M tokens/model/day of your *paid* usage** the next day, as a free resource pack valid 30 days.
- You must have a real-name verified account with the no-charge 安心体验 (safe-trial) mode switched off. That means pay-as-you-go billing is on.
- The collected data "将授权提供给火山引擎用于…模型和算法优化" (is provided to Volcengine for model and algorithm optimisation), and Volcengine "可永久使用" (may use it permanently).
- The plan's term is "延长至2026年9月30日" (extended to 2026-09-30). Some models exited on 2026-09-01, and more exit on 2026-10-08.
- The entry point currently supports only Doubao-Seed-Evolving.
- What remains is the one-time new-user 免费推理额度 (free inference quota), counted per model. The amount appears only in the console; the doc's 500K figure is an illustrative example.
- "Doubao-Lite / DeepSeek R2 free within 2M/day" is not supported by any official page.
- The endpoint is alive: `https://ark.cn-beijing.volces.com/api/v3/models` returns 401.

Recommendation: remove the entry. The only thing left is an unquantified one-time trial, which needs mainland real-name verification.

Sources: <https://docs.volcengine.com/docs/82379/1391869>, <https://docs.volcengine.com/docs/82379/1399514>

### Baidu Qianfan — STALE

Evidence: Baidu's official model retirement doc lists **ERNIE-Speed-128K, ERNIE-Lite-8K and ERNIE-Tiny-8K as retired on 2026-01-27** ("no longer available for use"). It recommends DeepSeek-V3, ERNIE-Speed-Pro-128K or ERNIE-4.5-Turbo-32K instead, none of which it describes as free. I found no official page naming a current permanently free model. The endpoint `qianfan.baidubce.com/v2/models` returns 403 without auth.

Recommendation: remove the entry.

Sources: <https://cloud.baidu.com/doc/qianfan/s/zmh4stou3>

### iFlytek Spark — UPDATE

What changed:
- The official HTTP doc still says Lite "支持**免费使用**" (free to use), with **8K max input and 4K max output** (model id `lite`).
- Auth is `Authorization: Bearer <APIPassword>` from the console, not APIKey/APISecret.
- The doc says "兼容openAI SDK" with base_url `https://spark-api-open.xf-yun.com/v1/`.
- Neither "unlimited tokens" nor "2 QPS" appears in the official doc. The doc only mentions per-second and concurrency throttle error codes (11202/11203).
- The endpoint is alive: `/v1/models` returns 401.

```markdown
### [iFlytek Spark](https://xinghuo.xfyun.cn/sparkapi)

讯飞星火. **Spark Lite is free** (model id `lite`, 8K input / 4K output), throttled by per-second and concurrency limits
(third-party reports: 2 QPS, no token cap). OpenAI SDK-compatible at `https://spark-api-open.xf-yun.com/v1`
with `Authorization: Bearer <APIPassword>` from the console. Individual real-name verification required.

Source: <https://www.xfyun.cn/doc/spark/HTTP%E8%B0%83%E7%94%A8%E6%96%87%E6%A1%A3.html>

*Checked Sep 29, 2026.*
```

### AIHubMix — UPDATE

What changed:
- The official free page (updated 2026-09-28) lists **60 free models** from 16 authors, all at $0.
- Every model speaks Chat Completions, Messages and Responses.
- New accounts get 10 trial calls, no card needed, and the calls never expire.
- A **one-time top-up of $1 or more** switches every free model to daily quotas: **100 req/day, 10 req/min, 1M tokens/day**, reset daily.
- Model IDs carry a `-free` suffix.

```markdown
### [AIHubMix](https://aihubmix.com/models/free)

Gateway with **60 free models**, no credit card. Every free model speaks Chat Completions, Messages, and Responses at
`https://aihubmix.com/v1` (model IDs end in `-free`).

Free: 10 trial calls at signup (never expire). A **one-time top-up of $1+** permanently unlocks
**100 req/day, 10 req/min, 1M tokens/day** on the free catalogue (resets daily).

Free models include coding-glm-5.3(-flash), coding-kimi-k3, coding-minimax-m3, xiaomi-mimo-v2.6-pro/flash, mimo-v2.5-pro,
gpt-5.5, gemini-3.8-flash, qwen3.6-plus-preview, hy3, nemotron-3-ultra/super, gemma-4-31b-it, gpt-oss-20b, glm-4.7-flash.

Source: <https://aihubmix.com/models/free>

*Checked Sep 29, 2026.*
```

### OVHcloud AI Endpoints — UPDATE

What changed:
- The official getting-started doc says anonymous use is limited to "2 requests per minute, per IP and per model". With an API key the limit is "400 requests per minute, per PCI project and per model", billed.
- The live `GET https://oai.endpoints.kepler.ai.cloud.ovh.net/v1/models` (no key) returns 24 models.
- Qwen3.8-27B and Qwen3.5-9B are new. The chat models are Qwen3.5-397B-A17B, Qwen3.8-27B, Qwen3.6-27B, Qwen3.5-9B, Qwen3-Coder-30B-A3B, gpt-oss-120b/20b, Meta-Llama-3_3-70B, Mistral-Small-3.2-24B, Mistral-Nemo, Mistral-7B and Qwen2.5-VL-72B.
- The catalogue shows non-zero per-token prices; those apply to keyed use.
- A 2026-09-28 third-party report (xibodev/llmgw-core#40) found that anonymous chat calls to those models still work and return 429 when the quota runs out.

```markdown
### [OVHcloud AI Endpoints](https://www.ovhcloud.com/en/public-cloud/ai-endpoints/catalog/)

EU-hosted (France). **Anonymous free tier — no API key, no signup**: 2 RPM per IP per model
(with a key: 400 RPM per project per model, pay-per-token). OpenAI SDK-compatible at
`https://oai.endpoints.kepler.ai.cloud.ovh.net/v1`.

Models: Qwen3.5-397B-A17B, Qwen3.8-27B, Qwen3.6-27B, Qwen3-Coder-30B-A3B, gpt-oss-120b/20b, Llama 3.3 70B,
Mistral Small 3.2, Mistral Nemo, Qwen2.5-VL-72B, plus Whisper, embeddings, and TTS.

Source: <https://docs.ovhcloud.com/en/guides/public-cloud/ai-machine-learning/ai-endpoints-getting-started>

*Checked Sep 29, 2026.*
```

### LLM7.io — UPDATE

What changed:
- The official limits doc gives these limits:
  - Anonymous: 1/s, 10/min, 60/hour, and **500K tokens per 24 h**.
  - Free token: 2/s, 40/min, 100/hour, and **1M tokens per 24 h**.
  - Pro: $12/month.
- Only `turbo`-tier models are open to anonymous and free-token users.
- The live `/v1/models` lists four turbo models: DeepSeek-V4-Flash-0731 (400K context, 71.5% availability in the last hour), codestral-latest, minimax-m2.7 (180K) and mistral-Nemo-Instruct-2407.
- gpt-oss-20b is no longer listed.
- I found nothing official supporting the "UK" location claim, so the proposed block drops it.

```markdown
### [LLM7.io](https://token.llm7.io)

Gateway with keyless access. Anonymous: 10 req/min, 60 req/hour, **500K tokens/day**; a free token from
`token.llm7.io` raises this to 40 req/min, 100 req/hour, **1M tokens/day**. OpenAI-compatible at `https://api.llm7.io/v1`.

Free (`turbo`-tier) models: DeepSeek-V4-Flash-0731 (400K ctx), codestral-latest, minimax-m2.7 (180K ctx), Mistral Nemo.
Everything else needs Pro ($12/month) or a topped-up balance.

Source: <https://docs.llm7.io/limits>

*Checked Sep 29, 2026.*
```

### Token Harbor — UPDATE

What changed:
- The official pricing page describes the Free plan as $0/month with a monthly allowance counted in 4-week windows. The amount is still unpublished, and the allowance carries over.
- Free models are now **DeepSeek V4.1 Flash, MiMo V2.6 Flash and TH-Rudder**.
- Agent Pass costs $1.99/month ($0.99 for the first month). It includes **$10 of usage**, "boosted" to up to $20 on selected models, and adds GLM 5.3 Flash, GPT-6 Luna and Qwen3.8 Flash.
- Free models are opt-in, and while enabled Token Harbor "may retain those prompts and responses for … model or product improvement".
- The terms still restrict access from some jurisdictions. The specific CN/HK/Macau `region_blocked` wording was not re-verified.
- The endpoint is alive: `/v1/models` returns 401.

```markdown
### [Token Harbor](https://tokenharbor.ai/pricing)

Small gateway. **Free tier $0/month** with a rolling allowance (amount unpublished, unused allowance carries over).
Agent Pass **$1.99/month** ($0.99 first month) adds $10 of included usage. OpenAI-compatible at `https://tokenharbor.ai/v1`.

Free models: DeepSeek V4.1 Flash, MiMo V2.6 Flash, TH-Rudder ("promotional models added over time").

**Warning:** free models are opt-in and their prompts/responses may be retained for diagnostics and model
improvement. Access is restricted in some regions (reported: mainland China, Hong Kong, Macau).

Source: <https://tokenharbor.ai/pricing>

*Checked Sep 29, 2026.*
```

### Aion Labs — UPDATE (minor)

What changed:
- The official rate-limits doc still gives the Free tier **15 RPM, 20,000 TPM and a 20,000-token daily limit**.
- Any top-up moves the account to Tier 1: 50 RPM, 1M TPM, and no daily limit.
- Public `/v1/models` now also lists **aion-3.5** and **aion-3.5-mini** (256K context, released 2026-09-23).
- The pricing page says "A daily credit allowance… No card required."

```markdown
### [Aion Labs](https://www.aionlabs.ai/app/api-keys/)

Permanent free tier, no credit card. **15 RPM, 20K tokens/day**. OpenAI-compatible at `https://api.aionlabs.ai/v1`.

Models: aion-3.5 / aion-3.5-mini (256K ctx), aion-3.0 / aion-3.0-mini, aion-2.0 (128K ctx, reasoning),
aion-rp-llama-3.1-8b. Tuned for roleplay/storytelling rather than coding.

Source: <https://www.aionlabs.ai/docs/rate-limits>

*Checked Sep 29, 2026.*
```

### Experiential Labs — UPDATE

What changed:
- The official billing doc sets "One credit is $0.01".
- The Free plan's recurring benefit "starts with the card verification (a one-time $1 charge, credited to your balance)". After that, "the total balance replenishes up to **100 credits**" every 30 days. That is $1/month, not ~500 credits.
- The live model page shows three models at $0: **GPT-6 Luna** ("100% off"), **MiMo-V2.6-Pro** ("Free", ZDR) and **Jev**. Qwen3.8 27B and DeepSeek V4 Flash are "75% off", not free.
- The docs say captured prompts are governed by an org-wide switch, and ZDR routes are never captured. I did not find an official statement of the claim that free traffic is exchanged for training traces.
- Anthropic API and Responses are supported. The endpoint `/v1/models` returns 401.

```markdown
### [Experiential Labs](https://platform.experientiallabs.ai)

"Open-source OpenRouter" gateway. Free plan: after a one-time **$1 card verification** (credited to your balance), the
balance **refills to 100 credits ($1) every 30 days**. OpenAI-compatible (Chat + Responses) and Anthropic-compatible at
`https://api.experientiallabs.ai/v1`.

$0 models right now: GPT-6 Luna (promo, 100% off), MiMo-V2.6-Pro (free, zero-data-retention route), Jev.
Qwen3.8 27B and DeepSeek V4 Flash are 75% off.

**Warning:** prompt/response capture is controlled by an org-wide switch — turn it off or require ZDR routes for private
code. Free-promo uptime varies by model (e.g. MiMo-V2.6-Pro ~76%). Prototyping only.

Source: <https://platform.experientiallabs.ai/docs/billing>, <https://platform.experientiallabs.ai/models>

*Checked Sep 29, 2026.*
```

### Empero — STALE

Evidence: `GET https://free.empero.org/v1/models` returns **HTTP 503** with `{"code":"maintenance","message":"The endpoint is offline for now and will be back soon…"}`. The landing page shows "00 — MAINTENANCE Qwen3.8-27B-FP8 … Quick restart in progress". The lab's site (empero.org) is alive, but the free API is down.

Recommendation: remove the entry, or strike it through with an "offline since at least Sep 29, 2026" note, and re-check later.

Sources: <https://free.empero.org>, <https://free.empero.org/v1/models>

---

## Proposed additions

The ranking weighs coding-agent value: model strength, Anthropic or OpenAI compatibility, the size of the quota, and how much friction it takes to get a key. Each block states which README section it belongs in.

### 1. NanoGPT — Pro subscription (section: Providers with Coding Plans)

This is the strongest cheap coding option found. The model list is broad and includes current coding models, and the API speaks both OpenAI and Anthropic `/messages`. The live subscription catalogue (`/api/subscription/v1/models`) returns 292 models.

```markdown
### [NanoGPT](https://nano-gpt.com/pricing)

Pay-as-you-go gateway for every major model, plus an optional **Pro subscription: $12/month — 60 million included input
tokens per week** on subscription models (web + API), and 5% off eligible paid text models.

Subscription models include GLM-5.3 / 5.3-Flash, Kimi K2.6 / K2.7 Code, MiniMax M3 / M2.7, DeepSeek V4 Flash / V4 Pro,
MiMo-V2.5(-Pro), Qwen3.8-27B, Nemotron 3 Ultra. OpenAI-compatible at `https://api.nano-gpt.com/api/v1`
(also `/messages` and `/responses`); use `https://api.nano-gpt.com/api/subscription/v1` to keep requests on the
subscription only. Pay-as-you-go deposits start at $1 (card).

Source: <https://nano-gpt.com/pricing>, <https://docs.nano-gpt.com/api-reference/endpoint/subscription-usage>

*Checked Sep 29, 2026.*
```

### 2. Tencent TokenHub (section: Free Providers; the Token Plan could also be listed under Coding Plans)

The free offer is a one-time trial rather than a recurring free tier. It is still large: 1M tokens per model, valid for one year. The paid Hy Token Plan starts at ¥28/month and covers GLM-5.3, Kimi K3 and DeepSeek V4 Pro, over both OpenAI and Anthropic endpoints. TokenHub replaces the old Hunyuan platform, which shuts down 2026-09-30.

```markdown
### [Tencent TokenHub](https://cloud.tencent.com/document/product/1823/130053)

Tencent Cloud's model platform (replaces the old Hunyuan platform, which shuts down Sep 30, 2026).

- **Free trial:** **1M tokens per language/multimodal model**, claimed once per main account per model from the
  Model Square "新用户福利" button; valid **1 year** from claim. Claim window ends **Dec 31, 2026**.
- **Token Plan (monthly):** Hy plan from **¥28** (Lite, 560 pts) to ¥468; universal plan ¥39–¥599. Models: DeepSeek-V4-Flash/Pro,
  MiniMax-M2.7/M3, GLM-5.2/5.3/5.3-Flash, Kimi K2.7 Code, Kimi K3 (+ Hy3, Hy4 preview on the Hy plan).
- Plan endpoints: OpenAI `https://api.lkeap.cloud.tencent.com/plan/v3`, Anthropic `https://api.lkeap.cloud.tencent.com/plan/anthropic`.

Which models qualify for the free trial is shown in the console. Real-name verification requirement: not confirmed.

Source: <https://cloud.tencent.com/document/product/1823/130053>, <https://cloud.tencent.com/document/product/1823/130060>

*Checked Sep 29, 2026.*
```

### 3. Alibaba Cloud Model Studio — new-user free quota (section: Free Providers, or a sub-heading under the existing Alibaba entry)

The README already covers Alibaba's paid plans but not the free quota. The quota is large and per-model, so it effectively multiplies across the Qwen coder and plus models. It expires after 90 days.

```markdown
#### [Model Studio free quota](https://www.alibabacloud.com/help/en/model-studio/new-free-quota)

New users get **1,000,000 free tokens per model** (typical), valid **90 days** from activation (or model release /
approval, whichever is later). Singapore region, international deployment scope only; real-time inference only
(no batch/fine-tune). Each model — and each dated snapshot — has its own quota; RAM users share the account's pool.
OpenAI-compatible at `https://dashscope-intl.aliyuncs.com/compatible-mode/v1`.

Source: <https://www.alibabacloud.com/help/en/model-studio/new-free-quota>

*Checked Sep 29, 2026.*
```

### 4. Z.ai — free Flash models (section: Free Providers)

This is the international counterpart of the BigModel.cn free models: GLM Flash models at $0 with no mainland ID needed. The models are smaller than GLM-5.x, but they cost nothing to use.

```markdown
### [Z.ai API — free Flash models](https://docs.z.ai/guides/overview/pricing)

Zhipu's international platform. **GLM-4.7-Flash**, **GLM-4.5-Flash** (text) and **GLM-4.6V-Flash** (vision) are priced
**Free** for input, cached input, and output. OpenAI-compatible at `https://api.z.ai/api/paas/v4`.

Rate/concurrency limits for free models are shown only in the console (not published).

Source: <https://docs.z.ai/guides/overview/pricing>

*Checked Sep 29, 2026.*
```

### 5. Nebius Token Factory (section: Free Providers)

This gives a small trial plus a notably larger $25 program credit, and the catalogue has 60+ open models. It needs a bank card.

```markdown
### [Nebius Token Factory](https://tokenfactory.nebius.com/)

Formerly Nebius AI Studio; EU-based open-model inference. **$1 trial credit on first sign-up, valid 30 days**; joining the
free **Nebius Builder Program** adds a **$25 Token Factory credit** (open to everyone; meant for learning/testing).
OpenAI-compatible at `https://api.tokenfactory.nebius.com/v1`.

**Warning:** setting up a billing account (bank card) is mandatory to finish onboarding.

Source: <https://docs.tokenfactory.nebius.com/other-capabilities/billing-new>, <https://dev.nebius.com/builders>

*Checked Sep 29, 2026.*
```

### 6. Novita AI — free models (section: Free Providers)

The free models are real, but they are the weakest for coding and their limits are unpublished. It is listed for completeness.

```markdown
### [Novita AI](https://novita.ai/pricing)

Open-model inference platform. Two models are priced **$0 in / $0 out**: `inclusionai/ling-3.1-flash` and
`inclusionai/ling-3.0-flash-sante` (262K ctx). OpenAI-compatible at `https://api.novita.ai/openai`.

Rate limits for the free models and any signup credit: not published on the pricing page.

Source: <https://novita.ai/pricing>

*Checked Sep 29, 2026.*
```

### Candidates rejected (verified this session)

| Candidate | Reason |
|---|---|
| Together AI | Official docs: "does not currently offer free trials"; $5 minimum purchase |
| Kimi / Moonshot platform | No free credits; $1 minimum recharge, $5 voucher after $5 cumulative; Tier0 = 3 RPM, 1 concurrent request |
| Featherless | No free tier; plans from $25/month |
| Chutes | Plus $10 / Pro $20 give a "daily quota", but the page does not state the amount |
| Perplexity | API pricing page shows no free tier or subscriber credit |
| Upstage | Only 10 free Studio agent runs; no API credit stated |
| Inference.net | Pay-as-you-go plan has no signup credit; $50 credit only on the $250/month plan |
| Venice | Only a one-time $10 credit for Pro subscribers, or DIEM staking |
| Baseten | "New accounts come with credits"; no amount given |
| Hyperbolic | Docs are now GPU-rental focused; no LLM free credit found |
| Kluster | `api.kluster.ai` does not resolve (DNS failure) |
| iFlow | `apis.iflow.cn/v1/models` returns 404 |
| Pollinations | Live OpenAI-compatible API, but "Quest Pollen" free amounts are unpublished; legacy `pk_` keys are capped at 1 pollen/IP/hour |
| ZenMux | Lists `z-ai/glm-4.7-flash-free` and `z-ai/glm-4.6v-flash-free`; free-model limits undocumented (docs URL 404) |
| BazaarLink | 3 `:free` models at $0 (`auto:free`, qwen3.7-flash, deepseek-v4-flash-0731); allowance unpublished |
| Parasail, Targon, Crofai | Pricing pages gave no extractable free-tier text |
| Poe API | Docs return 403 to plain HTTP; could not verify |
| Codestral free endpoint | No official page confirming that `codestral.mistral.ai` is still free (only secondary blogs) |
| Cloudflare AI Gateway | A gateway only; no inference credit of its own |
| Onomeo | Daily check-in scheme described only by a secondary source; not verified |

Not re-checked this session: DeepInfra, Lambda, Crusoe.

---

## Flags on other README entries (outside this batch, not changed)

- **Mistral La Plateforme:** the official pricing page now says the Free plan has "**$10 /mo in API credits**" with a training opt-out. The README's "~1B tokens/month" is out of date.
- **Vercel AI Gateway, NVIDIA NIM:** the peter123023 weekly audit of 2026-09-27 says a Vercel promo ended and that the NIM model lineup changed (DeepSeek V4 Flash, V4 Pro and MiniMax M3 delisted; GLM-5.3 and V4.1 Flash added). Not verified here.
- **Cerebras, GitHub Models:** a secondary search snippet claimed the Cerebras free tier returns 402 and GitHub Models returns 410. The OpenRouter comparison article (updated 2026-09-24) still lists both as active. This session, `models.github.ai/catalog/models` returned HTTP 200 with body `OK`, and `api.cerebras.ai/v1/models` returned 403 unauthenticated. **Inconclusive**, so re-verify both with real keys.

## Unresolved questions

1. **LongCat:** new accounts may still get a promotional gift quota ("活动赠送额度"). It is visible only after signup, so the STALE verdict rests on what the documentation leaves out.
2. **AMD Token Factory:** what the daily points allowance is, and whether it still equals ~$10. It is visible only after login.
3. **SenseNova:** whether the 600K/week cap and the 0-credit third-party models (DeepSeek V4, GLM-5.2, Kimi K3) are still current. Only the console or docs behind JavaScript show this.
4. **Z.ai free Flash models and Novita free models:** the rate and concurrency limits are console-only.
5. **Tencent TokenHub:** which language models qualify for the 1M-token trial, and whether real-name verification is needed to claim it. A developer-community article says the validity is 90 days, while the official doc says 1 year; the report uses the official doc.
6. **Empero:** whether the maintenance ends soon enough to keep the entry with a warning instead of removing it.
7. **Token Harbor:** whether the exact `region_blocked` list is still CN, HK and Macau. The terms mention regional restrictions only in general terms.
