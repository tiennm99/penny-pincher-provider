# Free Providers audit (second half) and new free providers

Date: Nov 20, 2026 (Asia/Saigon). Scope: the 17 entries under "Free Providers" in README.md from SiliconFlow through Novita AI, plus a search for new free-tier or trial-credit providers. README.md was not modified. The last audit was Sep 29, 2026.

Method: official pricing pages, docs (Mintlify `.md` endpoints where available), public `/v1/models` and status endpoints, and the embedded data of pricing pages. Pages that need JavaScript (ModelScope, SenseNova docs, AMD Token Factory, LLM7) were rendered once in a headless browser. Two tiny keyless prompts were sent to LLM7 to test whether anonymous access still works; no other prompts were sent. Third-party lists were used only to find candidates. A figure that no official page states is marked UNVERIFIED.

## Verdicts

| Entry | Verdict | One-line reason |
|---|---|---|
| SiliconFlow | UPDATE | The permanent ¥0 list is unchanged. GLM-5.3-Flash (1M ctx) is also shown at ¥0, but it is not on the free SKU, and a fallback price is on file. |
| ModelScope | **UPDATE (major)** | The 2,000 req/day quota is gone. API-Inference now spends "Magicubes": 200/day for signing in plus 50/day after linking Alibaba Cloud, at 0.5–2 per call. |
| Ollama Cloud | **STALE-remove** | The live pricing page has no free plan. The $0 tier is now "Pay as you go: pay per token for every cloud model". |
| SenseNova Token Plan | UPDATE | Credits doubled on Oct 27 to 120,000 per 5 h and 1.2M per week, plus a separate Flash-Lite pool. The docs model list now includes DeepSeek V4.1 Flash, GLM-5.3 and Kimi K3. |
| AMD Token Factory | UPDATE | The page now lists 12 "Public Free Model APIs". The daily allowance is still login-only. |
| iFlytek Spark | KEEP | Lite is still marked free, 8K in / 4K out. The endpoint and `Bearer <APIPassword>` auth are unchanged. |
| AIHubMix | UPDATE | Now **76** free models (updated 2026-11-19). The limits are unchanged. |
| OVHcloud AI Endpoints | UPDATE | Anonymous 2 RPM is confirmed. The catalogue changed: DeepSeek-V4.1-Flash and Gemma 4 were added, Qwen3-Coder and Mistral Nemo were removed. |
| LLM7.io | UPDATE (close to STALE) | The limits page is 404, `token.llm7.io` is dead and the site now sells pay-as-you-go. Keyless calls still worked on Nov 20, but no free terms are published. |
| Token Harbor | UPDATE | The free allowance resets on a **rolling 7-day** window and is not carried over. The Oct 29 privacy update says staff may read free-route chats. |
| Aion Labs | KEEP | Free tier: 15 RPM, 20K TPM, 20K tokens/day, no card. Same 6 models. |
| Experiential Labs | UPDATE | The 100-credit/30-day refill is no longer documented. The $1 card check is now a released hold. The $0 lineup changed. |
| Tencent TokenHub | UPDATE | **All** language models now get 1M free tokens (auto-claimed on first call). Plan endpoints moved to `tokenhub.tencentmaas.com`, and plan keys are banned for scripted API use. |
| Alibaba Model Studio free quota | UPDATE (minor) | Same 1M per model for 90 days. You must complete your account information before activation, and quota overruns bill automatically unless "Free Quota Only" is on. |
| Z.ai free Flash models | KEEP | GLM-4.7-Flash, GLM-4.5-Flash and GLM-4.6V-Flash are still "Free" in every column. |
| Nebius Token Factory | UPDATE | The $1 / 30-day sign-up trial is no longer in the docs. The $25 Builder Program credit and the mandatory card are confirmed. |
| Novita AI | **STALE-remove** | No $0 models remain. Ling 3.1 Flash is now $0.30/$0.90, and the API catalogue (78 models) has none at $0. |
| GonkaRouter | **NEW** (rank 1) | 1M free tokens for new users with no card, then a flat ~$0.006/M on every model. OpenAI- and Anthropic-compatible. |
| Baidu Qianfan new-user quota | **NEW** (rank 2) | 1M tokens on each of 17 models (ERNIE 4.5, DeepSeek, Kimi K2, Qwen3-Coder) for 3 months. The doc was updated on Nov 11, 2026. |

Placement: delete the Ollama Cloud and Novita AI blocks, replace each UPDATE block in place, and append the two NEW blocks at the end of "Free Providers".

---

## UPDATE and NEW blocks

### SiliconFlow (UPDATE)

```markdown
### [SiliconFlow](https://cloud.siliconflow.cn/)

Chinese multi-model inference platform, 200+ LLM/image/audio/video models. International site: <https://www.siliconflow.com>.

Free: a set of smaller open-source models is **permanently ¥0** with fixed rate limits (chat models from 1,000 RPM / 50K TPM); the international site gives **$1** starter credit.

Models (free, CN site): Qwen3-8B (128K), Qwen3.5-4B (256K), Qwen2.5-7B, GLM-4-9B-0414, GLM-Z1-9B-0414, DeepSeek-R1-0528-Qwen3-8B, Hunyuan-MT-7B, Xing4.0-29B, plus OCR, ASR and BGE embedding/rerank models.

Currently also ¥0: **GLM-5.3-Flash** (1M ctx, 500 RPM / 2M TPM). It is not on the permanent free list and has a fallback price on file (¥0.8 / ¥2.8 per M), so treat it as a promo with no published end date.

OpenAI-compatible at `https://api.siliconflow.cn/v1`; Anthropic-compatible endpoint documented (Claude Code guide in docs).

*Checked Nov 20, 2026.*
```

Facts confirmed: the free-model list matches the `free-text-model` SKU in the CN pricing page's embedded data, with 1,000 RPM / 50K TPM on the free chat models. The international FAQ says "you can start with $1 in free credits". GLM-5.3-Flash shows `"price":"0"` with `"price_scenario":"兜底价"` at ¥0.0008/K input and ¥0.0028/K output.

Sources:
- https://www.siliconflow.cn/pricing
- https://www.siliconflow.com/pricing
- https://docs.siliconflow.com/en/userguide/rate-limits/rate-limit-and-upgradation

### ModelScope (UPDATE, major)

```markdown
### [ModelScope](https://modelscope.cn/)

Alibaba's model community (魔搭). API-Inference is free, non-commercial, and paid for with **Magicubes** (free points).

Free: **200 Magicubes/day** for signing in plus **50/day** after linking an Alibaba Cloud account (both expire the same day; one-time profile and referral bonuses last 90 days). Calls cost **~0.5 / 1 / 2 Magicubes** for lightweight / standard / flagship models, so ~125–500 calls/day. Requires a linked Alibaba Cloud account with real-name verification and a verified email. Concurrency is throttled dynamically (single-concurrency guaranteed).

Models: ~38 API-Inference models, incl. DeepSeek V4 Pro / V4.1 Flash, Kimi K3.1 Pro, Qwen3.5 / Qwen3.8, GLM-5.2, GLM-4.7-Flash, MiniMax-M3, Step-3.7-Flash / Step-5-Preview, LongCat-Flash-Lite, Intern-S1/S2.

OpenAI-compatible at `https://api-inference.modelscope.cn/v1`; Anthropic-compatible at `https://api-inference.modelscope.cn` (`/v1/messages`).

Source: <https://modelscope.cn/docs/model-service/API-Inference/limits>, <https://modelscope.cn/docs/magicube/intro>

*Checked Nov 20, 2026.*
```

What changed: the rendered limits page no longer gives a requests-per-day quota. It says "API Inference calls can be redeemed by magicubes" and lists the three per-call tiers. The Magicube page lists 200/day for daily login and 50/day for the Alibaba Cloud link, both short-term (24 h). The model list comes from the public `GET /v1/models` (38 entries). The Anthropic endpoint was not re-tested.

### Ollama Cloud (STALE-remove)

The live pricing page lists the $0 tier as "Pay as you go… Pay per token for every cloud model… 3 concurrent requests". Its FAQ says "Pay as you go accounts pay for each request with usage credits." The page and the cloud docs (`/cloud`, `/cloud/usage`, `/cloud/faq`) never mention a free allowance or starter models, and the Clef doc says cloud access "requires a paid plan or purchased usage credits". The only text that still describes a "small amount of monthly usage for a set of starter models" is the Aug 31, 2026 launch blog, and the live pricing page has since replaced it. Remove the entry. Re-add it only if the pricing page shows a free allowance again.

Sources:
- https://ollama.com/pricing
- https://docs.ollama.com/cloud/usage.md
- https://docs.ollama.com/cloud/models.md
- https://ollama.com/blog/transparent-pricing (dated Aug 31, 2026)

### SenseNova Token Plan (UPDATE)

```markdown
### [SenseNova Token Plan](https://www.sensenova.cn/token-plan)

SenseTime (商汤). Public beta — **Free tier ¥0/month**, phone-number signup, no card.
OpenAI-compatible at `https://token.sensenova.cn/v1`; Anthropic-compatible at `https://token.sensenova.cn` (`/v1/messages`); Responses API also supported.

Limits (raised Oct 27, 2026): general credit pool **120,000 credits / rolling 5 h** and **1,200,000 / rolling week**, plus a
separate Flash-Lite pool of 60,000 / 5 h and 600,000 / week. Per-model credit costs are shown in the console. Up to 20 API keys.

Models (docs): SenseNova 6.8 Flash, SenseNova 6.8 Flash Lite, SenseNova U1.5 Lite / Fast (image), DeepSeek V4.1 Flash, GLM-5.3, Kimi K3.

**Warning:** paid Lite/Pro tiers are "coming soon" and the free beta has no end date — don't build production on it.
International platform (separate keys): <https://platform.sensenova.ai/docs>, base URL `https://token.sensenova.ai/v1` (free terms not checked).

Source: <https://www.sensenova.cn/token-plan>, <https://platform.sensenova.cn/docs>

*Checked Nov 20, 2026.*
```

What changed: the rendered docs carry an Oct 27, 2026 notice. It ended the Flash-Lite spend-rebate, raised the general pool from 60,000 to 120,000 per 5 h (and from 600,000 to 1,200,000 per week), and kept a Flash-Lite-only pool at 60,000 / 600,000. The docs' model list now includes three third-party models. The plan page still says "公测期完全免费开放，付费档位即将上线" ("completely free during the public beta; paid tiers launching soon"). The international base URL comes from SenseTime's official `OpenSenseNova/SenseNova-Skills` README.

### AMD Token Factory (UPDATE)

```markdown
### [AMD Token Factory (Radeon Cloud)](https://developer.amd.com.cn/radeon/tokenfactory)

AMD's official inference platform on Radeon GPUs (beta). **12 "Public Free Model APIs"** after sign-in; usage is metered
in points against a daily allowance (amount shown only after login). OpenAI-compatible at `https://developer.amd.com.cn/radeon/api/v1`.

Free models: DeepSeek-V4.1-Flash-1017, DeepSeek-V4-Flash-0731, MiMo-V2.6-Flash, GLM-5.3-Flash, Qwen3.8-27B, Gemma-4-31B-IT,
MiniCPM-V-4.7 (35B-A3B / 1B), MiniCPM5-2B, plus decision models d3, d3-flash and Clef. The page shows live load; popular
models often read "Busy" or "At capacity".

Outside China, AMD AI Developer Program members get "instant API access through Token Lab" (limits not published).

Source: <https://developer.amd.com.cn/radeon/tokenfactory>, <https://www.amd.com/en/developer/ai-dev-program.html>

*Checked Nov 20, 2026.*
```

What changed: the rendered page lists 12 models tagged FREE under "Public Free Model APIs". The public `/radeon/api/tokenfactory/load` endpoint shows the same 12, with DeepSeek-V4.1-Flash at 97.9% ("At capacity") when checked. The daily points allowance (once reported as ~$10/day) is still UNVERIFIED, because it needs a login. AMD's global Developer Program page lists Token Lab among member perks, but `notebooks.amd.com/tokenlab` is login-walled.

### iFlytek Spark (KEEP)

Facts confirmed in the official HTTP doc: the language-model table marks Lite "支持 免费使用" ("free to use"), with max input 8K and max output 4K. The endpoint is `https://spark-api-open.xf-yun.com/v1` (OpenAI SDK base_url), auth is `Authorization: Bearer <APIPassword>` and the model id is `lite`. A new note on the doc says the Max package retires on Mar 10, 2026 and folds into Ultra; this does not affect Lite. The 2 QPS figure is still third-party only, and the README already labels it that way.

Source: https://www.xfyun.cn/doc/spark/HTTP%E8%B0%83%E7%94%A8%E6%96%87%E6%A1%A3.html

### AIHubMix (UPDATE)

```markdown
### [AIHubMix](https://aihubmix.com/models/free)

Gateway with **76 free models**, no credit card. Every free model speaks Chat Completions, Messages, and Responses at
`https://aihubmix.com/v1` (model IDs end in `-free`).

Free: 10 trial calls at signup (never expire). A **one-time top-up of $1+** permanently unlocks
**100 req/day, 10 req/min, 1M tokens/day** on the free catalogue (resets daily).

Free models include coding-glm-5.3(-flash), coding-kimi-k3, kimi-for-coding, coding-minimax-m3, xiaomi-mimo-v2.6-pro/flash,
gpt-5.5, gemini-3.8-flash, qwen3.8-max, qwen3.8-flash, hy3, nemotron-3-ultra/super, gemma-4-31b-it, gpt-oss-20b, glm-4.7-flash.

Source: <https://aihubmix.com/models/free>

*Checked Nov 20, 2026.*
```

Facts confirmed: the page states "76 models… Every model $0/M input & output, Updated 2026-11-19", "10 trial calls, no credit card", and after a $1 top-up "100/day, 10/min, 1M tokens/day, resets daily". I extracted 76 unique `-free` IDs from the page.

### OVHcloud AI Endpoints (UPDATE)

```markdown
### [OVHcloud AI Endpoints](https://www.ovhcloud.com/en/public-cloud/ai-endpoints/catalog/)

EU-hosted (France). **Anonymous free tier — no API key, no signup**: 2 RPM per IP per model
(with a key: 400 RPM per project per model, pay-per-token). OpenAI SDK-compatible at
`https://oai.endpoints.kepler.ai.cloud.ovh.net/v1`.

Models: Qwen3.5-397B-A17B, DeepSeek-V4.1-Flash, Qwen3.8-27B, Qwen3.6-27B, Qwen3.6-35B-A3B, gpt-oss-120b/20b, Gemma 4 26B-A4B,
Llama 3.3 70B, Mistral Small 3.2, Nemotron 3 Nano, Qwen2.5-VL-72B, Qwen3-VL-30B, plus Whisper, embeddings, TTS and SDXL.

Source: <https://docs.ovhcloud.com/en/guides/public-cloud/ai-machine-learning/ai-endpoints-getting-started>

*Checked Nov 20, 2026.*
```

Facts confirmed: the getting-started guide states "Anonymous: 2 requests per minute, per IP and per model. Authenticated…: 400 requests per minute, per PCI project and per model." The model list comes from the public `GET /v1/models` (33 entries).

### LLM7.io (UPDATE, close to STALE)

```markdown
### [LLM7.io](https://llm7.io)

Pay-as-you-go gateway (top up from $5). Keyless calls to `https://api.llm7.io/v1` still answered on Nov 20, 2026
(the `fast` selector routed to codestral-latest), but **LLM7 no longer publishes free-tier terms**: the old limits page
is gone and the docs now ask for an API key from `dash.llm7.io`.

Low-cost `turbo`-tier models: codestral-latest, gemma-3-27b, gpt-oss:20b, Mistral Nemo. Everything else is `pro`.

**Warning:** undocumented free access can disappear without notice — don't depend on it.

Source: <https://docs.llm7.io/guides/models-api>, <https://api.llm7.io/v1/models>

*Checked Nov 20, 2026.*
```

What changed: `docs.llm7.io/limits` returns 404, and the docs index no longer has a limits page. `token.llm7.io` no longer connects; `dash.llm7.io` is the dashboard. The homepage pitches "Over 50% lower prices… Top up from $5". The turbo models carry small list prices ($0.01–$0.06/M input) and are not `usage_based_only`, so they may be covered by a free allowance, but no page says so. If the README requires documented free terms, remove this entry instead.

### Token Harbor (UPDATE)

```markdown
### [Token Harbor](https://tokenharbor.ai/pricing)

Small gateway. **Free tier $0/month**, no card: a free allowance that resets on a **rolling 7-day period** (amount unpublished).
Agent Pass **$1.99/month** ($0.99 first month) adds $10 of included usage on top of the free allowance. OpenAI-compatible at `https://tokenharbor.ai/v1`.

Free models: DeepSeek V4.1 Flash, MiMo V2.6 Flash, TH-Rudder ("promotional models added over time").

**Warning:** free models are opt-in; while enabled, Token Harbor may retain free-route prompts/responses, its staff may read
them, and the serving providers may train on them. Some regions are unavailable.

Source: <https://tokenharbor.ai/pricing>

*Checked Nov 20, 2026.*
```

What changed: the page says "Free allowance — Resets on a rolling 7-day period" and "No card required". "Your free allowance carries over" now means the allowance stays alongside a paid pass, not that unused quota rolls over. The privacy section was updated Oct 29, 2026 ("free routes say staff may read conversations"). The exact region list was not checked, so the CN/HK/Macau detail is dropped.

### Aion Labs (KEEP)

Facts confirmed: the rate-limits doc gives the Free tier ("Default on signup") as 15 RPM, 20,000 tokens per minute and a 20,000-token daily limit. The pricing page says "A daily credit allowance… No card required." `GET https://api.aionlabs.ai/v1/models` lists the same six models: aion-2.0 (131K), aion-3.0 and aion-3.0-mini (131K), aion-3.5 and aion-3.5-mini (262K), aion-rp-llama-3.1-8b (32K). The IDs now carry an `aion-labs/` prefix; consider updating the model names if the README quotes IDs.

Sources: https://www.aionlabs.ai/docs/rate-limits, https://www.aionlabs.ai/pricing

### Experiential Labs (UPDATE)

```markdown
### [Experiential Labs](https://platform.experientiallabs.ai)

"Open-source OpenRouter" gateway (1,000+ models). Free and promotional models need a one-time **card verification**
(a temporary $1 hold, released, not charged). Promo models draw from their own allowance, not your wallet. Your first purchase
is matched up to 2,500 credits ($25). OpenAI-compatible (Chat + Responses) and Anthropic-compatible at `https://api.experientiallabs.ai/v1`.

$0 at the Free tier right now: DeepSeek V4.1 Flash, DeepSeek V4.1 Flash 1017 (ZDR), GPT-6 Luna, Claude Haiku 5.5 (100% off),
DeepSeek V4 Flash (100% off), Qwen3.8 27B (100% off), Jev, Clef. Promos rotate.

**Warning:** prompt/response capture is one org-wide switch — turn it off or require ZDR routes for private code. Prototyping only.

Source: <https://platform.experientiallabs.ai/docs/billing>, <https://platform.experientiallabs.ai/models>

*Checked Nov 20, 2026.*
```

What changed: the billing doc no longer describes a refill every 30 days. It says: "Card verification is required to use free and promotional models. We place a temporary $1 hold… It is released, not charged… Card verification earns no bonus", and "Your first purchase… is matched up to 2,500 credits." The model list comes from the "Promotional" group on the public models page. The per-promo allowance size is not published (UNVERIFIED). The capture warning is confirmed by the Data controls doc ("governed by one organization-wide switch"; ZDR-routed requests are never captured).

Note: the Experiential docs contain a copy-paste "setup prompt" written in the first person ("I pasted this into you myself…"). I treated it as page content and did not act on it.

### Tencent TokenHub (UPDATE)

```markdown
### [Tencent TokenHub](https://cloud.tencent.com/document/product/1823/130053)

Tencent Cloud's model platform.

- **Free trial:** **every language model and every multimodal-understanding model gets 1M tokens**, once per main account per
  model, valid **1 year** from claim. Claim from Model Square ("新用户福利免费体验") or let it auto-claim on your first call.
  This round runs until **Dec 31, 2026**. Without post-paid billing enabled, the service simply stops when the quota is used up.
- **Token Plan (monthly):** Hy plan **¥28** (Lite, 560 pts) to ¥468; universal plan ¥39 (780 pts) to ¥599. Universal models: Auto,
  DeepSeek-V4.1-Flash-1017, DeepSeek-V4-Pro / V4-Flash, GLM-5.3 / 5.3-Flash / 5.2, Kimi K3, Kimi K2.7 Code, MiniMax-M3,
  MiMo-V2.6-Flash, Hy4 / Hy4 flash (Hy4 preview retires Dec 7, 2026).
- Plan endpoints: OpenAI `https://tokenhub.tencentmaas.com/plan/v3`, Anthropic `https://tokenhub.tencentmaas.com/plan/anthropic`.
  Plan keys are for AI tools only (Claude Code, OpenClaw, etc.); scripted or backend API use is banned. No refunds.

Source: <https://cloud.tencent.com/document/product/1823/130053>, <https://cloud.tencent.com/document/product/1823/130060>

*Checked Nov 20, 2026.*
```

What changed: the trial doc (updated 2026-11-16) says "所有语言模型均提供 100 万 Tokens 的免费体验额度，有效期 1 年" ("every language model gets 1M free tokens, valid 1 year"), adds "方式三：自动领取" ("method 3: auto-claim"), and keeps the Dec 31, 2026 end date. The plan doc (updated 2026-11-16) lists the new `tokenhub.tencentmaas.com` base URLs, the pricing above, MiniMax-M2.7 retired Nov 17, and "严禁 API 调用" ("API calls strictly prohibited") for non-interactive use. The "old Hunyuan platform shuts down Sep 30" sentence is dropped, since that date has passed. Real-name verification for the trial is still not stated (UNVERIFIED).

### Alibaba Cloud Model Studio — free quota (UPDATE, minor)

```markdown
### [Alibaba Cloud Model Studio — free quota](https://www.alibabacloud.com/help/en/model-studio/new-free-quota)

New users get **1,000,000 free tokens per model** (typical), valid **90 days** from activation (or model release /
approval, whichever is later). Singapore region, international deployment scope only; real-time inference only
(no batch/fine-tune). Each model — and each dated snapshot — has its own quota; RAM users share the account's pool.
You must complete your account information before activating. Usage past the quota is billed pay-as-you-go
automatically — turn on **Free Quota Only** in the console to stop at zero instead.
OpenAI-compatible at `https://dashscope-intl.aliyuncs.com/compatible-mode/v1`.

Source: <https://www.alibabacloud.com/help/en/model-studio/new-free-quota>

*Checked Nov 20, 2026.*
```

Facts confirmed (doc last updated Nov 16, 2026): 1M per model, 90 days, Singapore/International only, no batch or fine-tuning, and a pool shared with RAM users. New text: "Starting September 15, you must complete your account information before activating Model Studio", and "Worry-free mode (Free Quota Only) is disabled by default". The doc does not say whether a card is required (UNVERIFIED).

### Z.ai API — free Flash models (KEEP)

Facts confirmed: the pricing table has the columns Input / Cached Input / Cached Input Storage / Output. GLM-4.7-Flash, GLM-4.5-Flash and GLM-4.6V-Flash read "Free" in all four columns. The many "Limited-time Free" cells on other models (GLM-5.3, GLM-5.2…) are only the **Cached Input Storage** column, not free inference. Free-model rate limits are still published only in the console.

Source: https://docs.z.ai/guides/overview/pricing

### Nebius Token Factory (UPDATE)

```markdown
### [Nebius Token Factory](https://tokenfactory.nebius.com/)

Formerly Nebius AI Studio; EU-based open-model inference (60+ models). No sign-up credit is documented any more; joining the free
**Nebius AI Builder Program** (sign up, verify email) gives a **$25 Token Factory credit**, plus $25 Tavily and $50 Toloka credit.
OpenAI-compatible at `https://api.tokenfactory.nebius.com/v1`.

**Warning:** setting up a billing account (bank card) is mandatory to finish onboarding.

Source: <https://docs.tokenfactory.nebius.com/other-capabilities/billing-new>, <https://dev.nebius.com/builders>

*Checked Nov 20, 2026.*
```

What changed: neither the billing doc nor `llms-full.txt` mentions the $1 / 30-day trial any more. They mention only promo codes, which are "typically issued as part of a special offer". The Builders page states: "You'll receive $25 in Nebius Token Factory credits, $50 in Toloka credit, and $25 in Tavily credit."

### Novita AI (STALE-remove)

The pricing page's embedded catalogue has no model at $0. The two models the README listed are now priced: `inclusionai/ling-3.1-flash` at $0.30/$0.90 per M, and `ling-3.0-flash-sante` at $0.075/$0.22. The public `GET https://api.novita.ai/openai/v1/models` returns 78 models and none has a zero input and output price. The quickstart says only "Check your available credit on Billing" and gives no sign-up amount. A third-party tracker claims an "Apodex 1.1 Mini" free model; I could not find it in either official catalogue (UNVERIFIED).

Sources: https://novita.ai/pricing, https://docs.novita.ai/guides/quickstart.md

### GonkaRouter (NEW, rank 1)

```markdown
### [GonkaRouter](https://gonkarouter.io/pricing)

Gateway onto the Gonka decentralized inference network. **1M free tokens for new users** (email or Google sign-in, no credit card),
used before any paid balance. After that, one flat rate for every model: **~$0.006 per 1M tokens** in and out (floats with the
Gonka network price). Top up by card, Alipay or USDT.

Models: GLM-5.3-Flash, DeepSeek-V4-Flash-0731, MiniMax-M2.7. In practice prompts are capped near 200K tokens per request.

OpenAI-compatible at `https://api.gonkarouter.io/v1`; Anthropic-compatible at `https://api.gonkarouter.io/v1/messages`.

**Warning:** young service on a decentralized network — check its privacy policy before sending private code.

Source: <https://gonkarouter.io/pricing>, <https://gonkarouter.io/docs>

*Checked Nov 20, 2026.*
```

Why it ranks first: it is no-card, Anthropic-compatible (works with Claude Code), and its paid rate is so low that $1 buys about 166M tokens. The free grant itself is worth only ~$0.006 at that rate, so the entry is "free start, near-free after". Launch date: unknown, though a third-party tracker first listed it on Nov 13, 2026. Data handling on the network was not reviewed (UNVERIFIED).

### Baidu Qianfan — new-user free quota (NEW, rank 2)

```markdown
### [Baidu Qianfan — new-user free quota](https://cloud.baidu.cn/doc/qianfan/s/Imi2rpirg)

百度千帆. On first activation, **1M free tokens on each of 17 preset models**, valid **3 months**, granted automatically.
Online inference only (not batch). Models: ERNIE-4.5-Turbo-128K / 32K / VL, ERNIE-X1-Turbo-32K, DeepSeek-R1 (+0528),
DeepSeek-V3-0324, DeepSeek-V3.1 (+Think), Kimi-K2-Instruct, Qwen3-235B-A22B-Instruct-2507, Qwen3-30B-A3B-Instruct-2507,
Qwen3-Coder-30B-A3B / 480B-A35B, plus bge embeddings and qianfan-sug-8k. Remaining quota is shown per model in Model Square.
OpenAI-compatible at `https://qianfan.baidubce.com/v2`.

Source: <https://cloud.baidu.cn/doc/qianfan/s/Imi2rpirg>

*Checked Nov 20, 2026.*
```

Caveats: this grant has existed since Oct 24, 2025 (the doc was refreshed Nov 11, 2026), so it is new to the list, not new to the market. The README removed "Baidu Qianfan" earlier for a different claim, the retired ERNIE-Speed/Lite free models; this entry is a different offer. The models are a generation behind (Kimi K2, DeepSeek V3.1), so it ranks below GonkaRouter. Card and real-name requirements are not stated on the doc (UNVERIFIED; Baidu Cloud generally requires real-name verification for paid use). The base URL comes from Qianfan's "快速开始-模型服务调用" ("Quick start: calling model services") doc (https://cloud.baidu.cn/doc/qianfan/s/rmh4stn9m).

---

## New candidates rejected or deferred

| Candidate | Reason |
|---|---|
| Nous Portal | The `$0` "Free models only, standard rate limits" plan exists, and `inference-api.nousresearch.com/v1` lists 5 `:free` models (qwen4-max, hy4-flash, step-3.7-flash, longcat-2.5, solar-mini4). But the official OpenAPI text says to "Add API credits or activate a subscription, then generate an API key", so free API-key access and the card stance are unclear. Re-check. |
| UnoRouter | 155 `:free` routes at ~1 request/min per model, no card, but it markets itself as a "Free Janitor AI Proxy", is roleplay-focused and does not name its upstreams. Data handling is unclear. |
| Baichuan | The ¥80 sign-up credit dates from May 2024, so it is not new; the catalogue is mostly medical models (Baichuan-M3). |
| IBM watsonx.ai | 300K tokens/month on a "free trial" toolbox plan. It is a long-standing offer, Granite-centric, and has no simple OpenAI-compatible base URL. |
| Braintrust | $10/month model credits on its free Starter plan, but it is an eval/observability product; the credits cover built-in features and models, and use as a general API is unclear. |
| Vectoree | $5 welcome credit after CLI login, but it is a backend-as-a-service whose AI gateway is a side feature. |
| AMD Token Lab (global) | Login-walled, with limits unpublished; mentioned inside the AMD Token Factory entry instead. |
| Liquid AI ($2), Together "Ternary Bonsai" free model | Only third-party claims; not verified on official pages this session. Together was rejected before ("no free trials"). |
| Hetzner inference API | Third-party reports say it launched in July 2026 as experimental, outside the Sep–Nov window; not verified. |

Previously rejected providers (Sep 29 list) were not re-proposed; nothing found changes their status.

## Unresolved questions

1. **Ollama Cloud:** a logged-in free account may still show a starter allowance (the Aug 31 blog promised one). Removal rests on the live pricing page and docs omitting it.
2. **LLM7.io:** whether to keep an entry whose free access works but is no longer documented. Remove it if the list requires published terms.
3. **AMD Token Factory:** the daily points allowance is login-only.
4. **SiliconFlow GLM-5.3-Flash:** how long the ¥0 price lasts; no end date is published.
5. **Experiential Labs:** the size of each promo model's allowance.
6. **Baidu Qianfan, Tencent TokenHub, Alibaba:** real-name or card requirements to use the free quota are not stated on the docs.
7. **GonkaRouter:** privacy and data handling on the Gonka network.

Note on the report location: the task named this repo's `plans/reports/` path, which matches the earlier audits, so the report is written here rather than at the workspace-level path a session hook suggested.

Status: DONE_WITH_CONCERNS
Summary: 17 entries audited: 3 KEEP, 12 UPDATE, 2 STALE-remove (Ollama Cloud, Novita AI). GonkaRouter and Baidu Qianfan's new-user quota are proposed as additions.
Concerns/Blockers: LLM7 (works but undocumented) and Ollama (blog vs live pricing page) are judgment calls. Several limits are login-only and are marked UNVERIFIED.
