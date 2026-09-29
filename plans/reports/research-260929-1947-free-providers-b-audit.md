# Free Providers audit (batch B): 13 entries

Date: Sep 29, 2026. Scope: 13 entries under "Free Providers" in README.md, from Google Cloud Vertex AI through Ollama Cloud. README.md was not modified.
Method: official docs and pricing pages fetched with curl or WebFetch, Mintlify `.md` doc endpoints, and public `/v1/models` JSON where an endpoint exposes one. Third-party sources are used only where the official page gives no number, and each such use is labeled.

## Summary

| Entry | Status | Headline |
|---|---|---|
| Google Cloud Vertex AI | UPDATE | Renamed "Gemini Enterprise Agent Platform". The $300 credit cannot pay for partner MaaS models such as Claude. |
| Hugging Face Inference Providers | UPDATE | The free tier is **$0.10/month**, not "100K". PRO is $9/mo with **$2** of credits, not "2M". |
| Cerebras Cloud | UPDATE (close to STALE) | Cerebras no longer offers a permanent free tier. It now gives a **$5 / 30-day trial that requires a payment method**, and serves only 2 models. |
| BigModel.cn | UPDATE | GLM-4.5-Flash is gone from the price list. The free list is now GLM-4.7-Flash, GLM-4-Flash-250414, GLM-Z1-Flash, plus vision and image models. |
| Fireworks AI | UPDATE | Still $1. Adds a 10 RPM cap without a payment method and an Anthropic-compatible endpoint. |
| Scaleway Generative APIs | UPDATE | Still 1M tokens, plus 60 audio-minutes. The model catalogue changed. |
| SambaNova Cloud | UPDATE (conflicting sources) | The $5 credit is no longer advertised. The no-card tier is now **20 RPM / 20 RPD / 200K TPD** on 5 models. |
| Cohere | CURRENT (minor) | Same 1,000 calls/mo, 20 RPM, and non-commercial rule. The model list and the OpenAI-compat URL are updated. |
| Vercel AI Gateway | UPDATE | Official docs now say you must **add a payment method** to use the free credits. The docs no longer state the $5 figure. |
| Requesty | CURRENT (minor) | Still 200 req/day with no card. Adds base URLs. |
| SiliconFlow | UPDATE | The free list is longer: Qwen3-8B, Qwen3.5-4B, GLM-4-9B, GLM-Z1-9B, R1-0528-Qwen3-8B, and others. There is also an Anthropic endpoint. |
| ModelScope | UPDATE (quota UNVERIFIED on the official page) | Only 35 models are exposed now, not "50+". There is an Anthropic `/v1/messages` endpoint. |
| Ollama Cloud | UPDATE | Pricing changed on Aug 31, 2026. Session and weekly caps are gone. Free now means a monthly starter credit on starter models, with 1 concurrent request. |

No entry is outright STALE, because every vendor still offers some free allowance. **Cerebras** comes closest. It no longer has a no-card free tier and now looks like Fireworks-style trial credit. If the list's bar is "free without a card", remove it. If trials qualify, keep it.

---

## Google Cloud Vertex AI

**Status: UPDATE**

```markdown
### [Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)

Now branded **Gemini Enterprise Agent Platform** (formerly Vertex AI).

Free Trial: **$300** credit for 90 days (new GCP customers only; card verification). Not a recurring free tier. The $300 credit **cannot** pay for partner models offered as MaaS (e.g. Claude) or for Gemini API in AI Studio.

Express mode: `@gmail.com` accounts new to Google Cloud get a **90-day free tier with no billing info**, within express-mode quotas, on the APIs that support express mode (Gemini models). Separate from the $300 Free Trial.

Models: Gemini 3.x (Pro / Flash / Flash-Lite); partner models (Claude and others) need a paid billing account.

*Checked Sep 29, 2026.*
```

What changed:
- Google rebranded the product. The product page title is "Gemini Enterprise Agent Platform (formerly Vertex AI)".
- The free-features doc states the restriction directly: "You can't access or use the $300 credit for a generative AI partner model that is offered as a managed API ... model as a service." The old README line implied you could spend the credit on Claude, DeepSeek, GLM, and Qwen through MaaS. That was wrong for Claude and for any other partner MaaS model.
- Express mode is described as a 90-day free tier for new users with a @gmail.com account, with no billing information needed. It is separate from the Free Trial.
- The Gemini line now runs up to 3.8 Flash, according to the docs navigation.

Sources:
- https://cloud.google.com/vertex-ai
- https://cloud.google.com/free/docs/free-cloud-features
- https://cloud.google.com/vertex-ai/generative-ai/docs/start/express-mode/overview

---

## Hugging Face Inference Providers

**Status: UPDATE**

```markdown
### [Hugging Face Inference Providers](https://huggingface.co/docs/inference-providers)

Router in front of 20 partners: Baseten, Cerebras, Cohere, DeepInfra, Fal AI, Featherless AI, Fireworks, Groq, HF Inference, Novita, Nscale, OVHcloud, Public AI, Replicate, Scaleway, Together, WaveSpeedAI, Z.ai and others. No markup over provider rates.

Free: **$0.10/month** in credits (subject to change). PRO (**$9/month**): **$2.00/month** in credits, usable across all HF compute. Pay-as-you-go beyond that requires buying credits.

OpenAI-compatible at `https://router.huggingface.co/v1` (~130 chat models).

*Checked Sep 29, 2026.*
```

What changed:
- The credit figures were wrong. The official table shows "Free Users $0.10, subject to change" and "PRO Users $2.00". The "100K / 2M credits" wording in the README does not match HF's units.
- The partner list grew. The old list named 7 providers. The router `/v1/models` endpoint currently returns 133 models from featherless-ai, deepinfra, novita, nscale, zai-org, together, cohere, fireworks-ai, baseten, scaleway, ovhcloud, publicai, groq, and cerebras.
- The PRO price is unchanged at $9/month.

Sources:
- https://huggingface.co/docs/inference-providers/pricing
- https://huggingface.co/docs/inference-providers/index
- https://huggingface.co/pricing
- https://router.huggingface.co/v1/models

---

## Cerebras Cloud

**Status: UPDATE (effectively no longer a free tier; candidate for removal if the list requires no-card free access)**

```markdown
### [Cerebras Cloud](https://cloud.cerebras.ai)

Wafer-scale chip inference. **Free Trial only**: **$5** in credits after adding a **verified payment method**, expiring 30 days after grant. No permanently free tier. OpenAI-compatible at `https://api.cerebras.ai/v1`.

| Model | RPM | Uncached TPM | TPD | Context (free) |
|---|---|---|---|---|
| `gpt-oss-120b` | 5 | 30K | 1M | 65K |
| `qwen-3.8-27b` | 5 | 30K | 1M | 64K |

Total TPM (incl. cached) is 3x uncached (90K). Access stops when credits run out or expire until you buy credits.

*Checked Sep 29, 2026.*
```

What changed:
- The free tier is gone. The official FAQ, asked "Is there a permanently free tier?", answers "No. The Free Trial is time- and credit-bounded: $5 in credits that expire 30 days after they're granted." It also says: "If you skip adding a payment method at sign-up, Playground and API access remain inactive."
- The model lineup shrank to 2 shared models, `gpt-oss-120b` and `qwen-3.8-27b`. `llama3.1-8b-instant`, `qwen-3-235b-a22b-instruct-2507`, and `zai-glm-4.7` are no longer in the Shared Inference catalogue.
- The rate limits changed to 5 RPM per model, 30K uncached TPM, 1M TPH, and 1M TPD.
- The free context limit is 64–65K, not 8K.

Sources:
- https://inference-docs.cerebras.ai/support/rate-limits
- https://inference-docs.cerebras.ai/models/overview
- https://inference-docs.cerebras.ai/resources/openai.md

---

## BigModel.cn

**Status: UPDATE**

```markdown
### [BigModel.cn](https://www.bigmodel.cn/)

Zhipu AI (智谱 AI). New users get a free token package to explore the API, playground, and AGI apps (reported as 20M, 25M via invite).

Permanently free models: **GLM-4.7-Flash** (200K ctx), GLM-4-Flash-250414 (128K), GLM-Z1-Flash (128K), GLM-4.6V-Flash, GLM-4.1V-Thinking-Flash, GLM-4V-Flash, plus CogView-3-Flash (image) and CogVideoX-Flash (video). Concurrency limits apply per model.

OpenAI-compatible at `https://open.bigmodel.cn/api/paas/v4`; Anthropic-compatible at `https://open.bigmodel.cn/api/anthropic`.

> Referral: <https://www.bigmodel.cn/invite?icode=rIX6uZrLYfy8fQ6Urca4xf2gad6AKpjZefIo3dVEyA%3D>

*Checked Sep 29, 2026.*
```

What changed:
- **GLM-4.5-Flash is no longer on the official price list.** The only "4.5" rows are GLM-4.5-Air and GLM-4.5V, and both are paid.
- The list of models priced "免费" (free) is longer than the README showed. The additions are listed in the block above.
- The new GLM-5.3-Flash is **paid**, at ¥0.8 input / ¥2.8 output per 1M tokens. It is not free. In the pricing table, "限时免费" (free for a limited time) applies only to the cache-storage column.
- Coding Plan subscribers get a free night-time window for GLM-5.3-Flash from Sep 3 to Oct 7, 2026. That offer belongs to the Coding Plan entry, not this one.
- The new-user token amount is **UNVERIFIED** on an official page. Third-party posts cite 20M tokens, with an extra 25M for invitees. The README's "25M" figure is plausible only for accounts that sign up by invite.

Sources:
- https://docs.bigmodel.cn/cn/guide/start/pricing.md
- https://docs.bigmodel.cn/cn/api/rate-limit.md
- https://docs.bigmodel.cn/cn/coding-plan/notice/event-glm-5.3-flash.md
- New-user gift (third-party): https://github.com/x2v-co/aiplans/issues/16
- New-user gift (third-party): https://blog.csdn.net/2402_82616859/article/details/146219601
- Endpoints probed: `open.bigmodel.cn/api/paas/v4/models` and `open.bigmodel.cn/api/anthropic/v1/messages` both return auth errors, which means both routes exist.

---

## Fireworks AI

**Status: UPDATE**

```markdown
### [Fireworks AI](https://fireworks.ai)

**$1** in free starter credits for serverless inference. Without a payment method (or without credits) the account is capped at **10 RPM**; adding a payment method raises it up to 6,000 RPM.

Models: GLM 5.3 / 5.3 Flash, Kimi K3, DeepSeek V4 Flash, Qwen 3.8 27B and other open models. Function calling, MCP support.

OpenAI-compatible at `https://api.fireworks.ai/inference/v1`; Anthropic-compatible at `https://api.fireworks.ai/inference` (works with Claude Code).

*Checked Sep 29, 2026.*
```

What changed:
- The official pricing page still says "Get started with $1 in free credits."
- The account quota page now documents a 10 RPM limit for "No payment method or no credits".
- Fireworks now documents an Anthropic Messages endpoint, including a Claude Code setup.
- The model names above come from the current serverless and training price tables.

Sources:
- https://fireworks.ai/pricing
- https://docs.fireworks.ai/guides/quotas_usage/account-quotas.md
- https://docs.fireworks.ai/tools-sdks/anthropic-compatibility.md

---

## Scaleway Generative APIs

**Status: UPDATE**

```markdown
### [Scaleway Generative APIs](https://www.scaleway.com/en/generative-apis/)

EU/GDPR, Paris. Free tier for new customers: first **1,000,000 tokens** plus **60 minutes** of audio transcription (no time limit advertised). OpenAI-compatible at `https://api.scaleway.ai/v1`.

Models: GLM-5.2, DeepSeek V4 Flash, Qwen3.8-27B, Qwen3.5-397B, Qwen3.6-35B, Qwen3-235B, Qwen3-Coder-30B, Gemma 4 26B, Mistral Medium 3.5, Mistral Small 3.2, gpt-oss-120b, Llama 3.3 70B, Pixtral 12B, Whisper.

*Checked Sep 29, 2026.*
```

What changed:
- The free tier now also includes 60 audio minutes. According to the docs FAQ, the free tier is applied to the most expensive usage first.
- DeepSeek R1 distill is no longer listed.
- New models are GLM-5.2, DeepSeek V4 Flash, Qwen3.8/3.6/3.5, Gemma 4, Mistral Medium 3.5, and gpt-oss-120b.
- Whether a card is needed to *activate* the free tier is not stated on these pages. Scaleway accounts generally require a payment method, so treat this as UNVERIFIED.

Sources:
- https://www.scaleway.com/en/generative-apis/
- https://www.scaleway.com/en/pricing/model-as-a-service/
- https://www.scaleway.com/en/docs/generative-apis/faq/

---

## SambaNova Cloud

**Status: UPDATE (official sources conflict)**

```markdown
### [SambaNova Cloud](https://cloud.sambanova.ai)

RDU (dataflow chip) inference. **Free tier** applies when no payment method is linked: **20 RPM, 20 requests/day, 200K tokens/day** per model. Adding a card moves you to the Developer tier (pay-as-you-go, 60–240 RPM, 20M tokens/day across models).

Free-tier models: DeepSeek-V3.1, DeepSeek-V3.2 (preview), Llama 3.3 70B, gpt-oss-120b, Gemma 4 31B (preview).

OpenAI-compatible and Anthropic-compatible at `https://api.sambanova.ai/v1`.

*Checked Sep 29, 2026.*
```

What changed:
- The **$5 / 30-day credit is no longer advertised.** The Plans page's "Free" card now reads "Add a payment method and purchase credits to run your first requests." That contradicts the rate-limits doc, which still has a Free Tier tab "applied when there is no payment method linked."
- The free-tier limits are now 20 **RPD**, down from the old per-model daily figure, with 200K TPD.
- The model lineup changed. Whisper, Llama 4, and Qwen3 are gone. The public `/v1/models` endpoint returns DeepSeek-V3.1, DeepSeek-V3.2, Meta-Llama-3.3-70B-Instruct, MiniMax-M2.7, MiniMax-M3, gemma-4-31B-it, and gpt-oss-120b. The MiniMax models appear only in the Developer tier table.
- SambaNova now documents an Anthropic-compatible endpoint.
- The blog link in the README describes the 2024 launch credit. That page says credits expire in 3 months, not 30 days, and it is no longer current evidence.

Sources:
- https://docs.sambanova.ai/docs/en/models/rate-limits
- https://cloud.sambanova.ai/plans
- https://cloud.sambanova.ai/pricing
- https://api.sambanova.ai/v1/models
- https://docs.sambanova.ai/docs/en/features/anthropic-compatibility.md

---

## Cohere

**Status: CURRENT (minor refresh)**

```markdown
### [Cohere](https://dashboard.cohere.com/api-keys)

Trial API key, no credit card. **1,000 calls/month**, 20 RPM per chat model (Rerank 10 RPM, Embed 2,000 inputs/min).

Models: Command A+, Command A Reasoning / Vision / Translate, Command A, Command R+, Command R, Command R7B, North Mini Code, Aya Expanse / Aya Vision, plus rerank and embeddings.

OpenAI-compatible at `https://api.cohere.ai/compatibility/v1`.

**Warning:** trial keys are **not permitted for production or commercial use** — production needs a production key (paid). New model variants (e.g. Command A Reasoning) stay at trial limits even on prod keys.

*Checked Sep 29, 2026.*
```

What changed:
- There was no material change to the free terms. The pricing FAQ still says "trial keys are rate limited and are not permitted to be used for production or commercial purposes."
- The model list gains North Mini Code and the Command A variants.
- The OpenAI Compatibility API URL is added.

Sources:
- https://docs.cohere.com/docs/rate-limits.md
- https://cohere.com/pricing
- https://docs.cohere.com/v2/docs/how-does-cohere-pricing-work.md
- https://docs.cohere.com/docs/compatibility-api.md
- https://docs.cohere.com/docs/models.md

---

## Vercel AI Gateway

**Status: UPDATE**

```markdown
### [Vercel AI Gateway](https://vercel.com/docs/ai-gateway)

Single endpoint routing to many providers, with failover and BYOK. OpenAI-compatible at `https://ai-gateway.vercel.sh/v1`; also Anthropic Messages, OpenResponses and Cohere-compatible APIs.

Free: a **monthly included credit** (reported as **$5 / 30 days**; does not roll over), starting with your first request. **Requires a valid payment method on the team.** Covers only free-tier-eligible models with lower per-model rate limits. Buying credits moves you to the paid tier permanently and the monthly free credit stops.

Source: <https://vercel.com/docs/ai-gateway/pricing>

*Checked Sep 29, 2026.*
```

What changed:
- **A card is now required.** The Getting Started page says: "To use free AI Gateway Credits, add a valid payment method to your team." The FAQ lists error `403 customer_verification_required` with the explanation "must add a valid payment method before using free credits". A third-party post from Aug 16, 2026 said no card was needed, but the official docs now say otherwise.
- The official pricing, rate-limit, and FAQ pages no longer state a dollar amount. They say only "monthly included credit". The $5 figure now rests on third-party sources.
- The docs now say explicitly that buying credits ends the free credit.
- Vercel now documents Anthropic, OpenResponses, and Cohere-compatible APIs.

Sources:
- https://vercel.com/docs/ai-gateway/pricing
- https://vercel.com/docs/ai-gateway/rate-limits
- https://vercel.com/docs/ai-gateway/faq
- https://vercel.com/docs/ai-gateway/getting-started
- $5 figure (third-party): https://agentjournal.dev/blog/vercel-ai-gateway-free/
- $5 figure (third-party): https://freeaiapi.org/articles/vercel-api-key-guide

---

## Requesty

**Status: CURRENT (minor refresh)**

```markdown
### [Requesty](https://www.requesty.ai/)

LLM gateway with routing, caching, spend controls and EU data residency. Works with Claude Code, Cline, Cursor, Roo.

Free: **200 req/day** on the free-model catalogue. No credit card, no trial clock — same platform as pay-as-you-go (600+ models, +5% fee), just restricted to free models until you upgrade.

OpenAI-compatible at `https://router.requesty.ai/v1`; Claude Code via `ANTHROPIC_BASE_URL=https://router.requesty.ai`.

Source: <https://www.requesty.ai/free-models>, <https://www.requesty.ai/pricing>

*Checked Sep 29, 2026.*
```

What changed:
- The free terms are unchanged.
- The block adds the base URLs, the 600+ paid-model count, and the 5% pay-as-you-go fee.
- The public `/v1/models` endpoint lists 12 models at $0. Most are NVIDIA Nemotron 3 variants, plus Gemma 4 31B, Poolside Laguna, and Mistral Leanstral. I did not add them to the README block, because $0 in the model list may not equal free-tier eligibility.

Sources:
- https://www.requesty.ai/free-models
- https://www.requesty.ai/pricing
- https://router.requesty.ai/v1/models

---

## SiliconFlow

**Status: UPDATE**

```markdown
### [SiliconFlow](https://cloud.siliconflow.cn/)

Chinese multi-model inference platform, 200+ LLM/image/audio/video models. International site: <https://www.siliconflow.com>.

Free: a set of smaller open-source models is **permanently ¥0** with fixed rate limits (chat models from 1,000 RPM / 50K TPM); the international site gives **$1** starter credit.

Models (free, CN site): Qwen3-8B (128K), Qwen3.5-4B (256K), Qwen2.5-7B, GLM-4-9B-0414, GLM-Z1-9B-0414, DeepSeek-R1-0528-Qwen3-8B, Hunyuan-MT-7B, Xing4.0-29B, plus OCR, ASR and BGE embedding/rerank models.

OpenAI-compatible at `https://api.siliconflow.cn/v1`; Anthropic-compatible at `https://api.siliconflow.cn/` (Claude Code guide in docs).

*Checked Sep 29, 2026.*
```

What changed:
- I built the free-model list from the price-"0" entries in the CN pricing page's embedded model data.
- The docs say "The Rate Limits for free models are fixed." The chat rate range starts at 1,000 RPM / 50,000 TPM, consistent with the README.
- SiliconFlow now documents an Anthropic-compatible endpoint.
- The "identity verification required" claim is **UNVERIFIED**. I could not reach a docs page that states it.

Sources:
- https://www.siliconflow.cn/pricing
- https://www.siliconflow.com/pricing
- https://docs.siliconflow.com/en/userguide/rate-limits/rate-limit-and-upgradation
- https://docs.siliconflow.cn/cn/usercases/use-siliconcloud-in-ClaudeCode

---

## ModelScope

**Status: UPDATE (quota numbers UNVERIFIED against the official page, which renders only with JavaScript)**

```markdown
### [ModelScope](https://modelscope.cn/)

Alibaba's model community (魔搭). API-Inference free for registered users.

Free: **2,000 req/day** total, **≤500 req/day per model** (some large models lower). Requires binding an Alibaba Cloud account with real-name verification. Quotas may be adjusted at any time.

Models: ~35 API-Inference models, incl. DeepSeek V4 Pro / V4.1 Flash, Qwen3.5 / Qwen3.8, GLM-5.2, GLM-4.7-Flash, MiniMax-M3, Step-3.7-Flash, LongCat-Flash-Lite, Intern-S1.

OpenAI-compatible at `https://api-inference.modelscope.cn/v1`; Anthropic-compatible at `https://api-inference.modelscope.cn` (`/v1/messages`).

*Checked Sep 29, 2026.*
```

What changed:
- The public `/v1/models` endpoint returns **35** models, not "50+".
- An Anthropic `/v1/messages` route exists. It answered an empty POST with a schema validation error, not a 404.
- The 2,000/day and 500/model quota comes only from secondary sources: Cherry Studio docs and search snippets. The official limits page did not render without JavaScript.

Sources:
- https://api-inference.modelscope.cn/v1/models
- https://modelscope.cn/docs/model-service/API-Inference/limits (JavaScript only; content not extracted)
- Secondary: https://github.com/CherryHQ/cherry-studio-docs/blob/main/pre-basic/providers/modelscope.md

---

## Ollama Cloud

**Status: UPDATE**

```markdown
### [Ollama Cloud](https://ollama.com/cloud)

Hosted counterpart to the local `ollama` CLI — same commands and API, models run on Ollama's GPUs. Prompts are not used for training.

Free: a **starter amount of usage credits each month** (exact amount unpublished) on a smaller set of **starter models**, **1 concurrent request**, no credit card. Buying pay-as-you-go credits unlocks all cloud models. Session/weekly caps were removed on Aug 31, 2026.

Models: DeepSeek V4, GLM-5.3, Kimi K3 / K2.7 Code, MiniMax M3, gpt-oss, Gemma 4, Nemotron 3, Mistral Large 3 (paid rates published per model).

OpenAI-compatible at `https://ollama.com/v1`; Anthropic-compatible at `https://ollama.com/v1/messages`.

*Checked Sep 29, 2026.*
```

What changed:
- Ollama switched to credit-based pricing on Aug 31, 2026. The blog post says: "The free plan now includes a small amount of monthly usage for a set of starter models ... no 5-hour or weekly limits."
- The pricing FAQ confirms free concurrency is 1 and that free usage resets monthly from the signup date.
- Neither the starter amount nor the list of starter models is published.
- The "16 model families" count was not re-verified. The block lists the families shown in the price table instead.

Sources:
- https://ollama.com/pricing
- https://ollama.com/blog/transparent-pricing
- https://docs.ollama.com/cloud.md
- https://docs.ollama.com/api/openai-compatibility.md
- https://docs.ollama.com/api/anthropic-compatibility.md
- https://ollama.com/v1/models

---

## New free offers from these vendors

- **Vertex express mode.** This is the one notable no-billing option, a 90-day free tier for Gemini. It is already mentioned in the entry and is now described more precisely.
- **BigModel's night-time GLM-5.3-Flash window.** This runs Sep 3 to Oct 7, 2026. It is a Coding Plan perk, not a free API tier, so if it gets a mention it belongs in the "BigModel.cn — GLM Coding Plan" section.
- None of the other vendors launched a new free tier. Several moved the other way:
  - Cerebras, SambaNova, and Vercel now require a card to get their free allowance.
  - Ollama replaced its caps with credits.

## Unresolved questions

1. **Cerebras inclusion policy.** Cerebras now offers a card-gated 30-day trial. Should it stay in "Free Providers", as Fireworks and Vertex do, or be removed?
2. **SambaNova.** The Plans page says you must buy credits, while the rate-limit doc still describes a no-card Free Tier. Which one is live cannot be settled without signing up for an account.
3. **Vercel $5 amount.** The official docs no longer state the dollar figure. It rests on third-party sources dated August 2026.
4. **ModelScope quotas** (2,000/day, 500/model, real-name requirement). The official limits page requires JavaScript and could not be read.
5. **BigModel new-user token gift** (20M, or 25M via invite). This was not confirmed on an official page.
6. **Ollama starter credit amount and starter model list.** Neither is published.
7. **Vertex express-mode quotas** (per-model RPM/RPD). These were not extracted from the docs.
8. **Scaleway and SiliconFlow sign-up requirements** (card for Scaleway, identity verification for SiliconFlow). These were not confirmed on any page I could reach.
