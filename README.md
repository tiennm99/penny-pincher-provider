# Penny-Pincher Provider

Curated list of affordable and free LLM API providers — Claude Code guest passes,
coding-plan subscriptions, and free-tier APIs. Maintained for developers who want
capable models without premium pricing.

Contributions welcome — open a pull request or
[issue](https://github.com/tiennm99/penny-pincher-provider/issues/new) to add or
update an entry.

---

## Claude Code Guest Passes

One week of free Claude Pro (includes Claude Code). New users only; requires payment
info but can be cancelled before the trial ends.

**My passes:**

- ~~<https://claude.ai/referral/ZkoAngod1A>~~ — out of stock as of 2026-04-30

**Friend's passes:**

- ~~<https://claude.ai/referral/7RBJExZ7LA>~~ — out of stock as of 2026-05-31

Have a spare pass? Open a PR adding your link under *Friend's passes*, or open an issue.

---

## Providers with Coding Plans

Monthly subscriptions with request-based (not token-based) quotas, compatible with
Claude Code, Cursor, Cline, and similar tools.

### [opencode — Go](https://opencode.ai/go)

Open-source `opencode` CLI subscription. $5 first month, **$10/month** thereafter.

Models: GLM-5.1, Kimi K2.6, MiniMax M2.7, Qwen3.5/3.6 Plus, MiMo-V2. Per-5-hour limits vary (200–10,200 req).
API key portable — works with Claude Code via LiteLLM proxy or `oc-go-cc`. Model format: `opencode-go/<model-id>`.

My referral:

> Invite friends to OpenCode Go. Earn $5 when a friend subscribes, and they'll get $5 too. Share your referral link; your friend joins and subscribes to Go; you both get a $5 usage credit to apply toward your Go usage limits.
>
> Referral link: <https://opencode.ai/go?ref=HE42WGS8BM>

*Checked Apr 30, 2026.*

### [Z.ai](https://z.ai/subscribe)

Plans from **$18/month** (Lite/Pro/Max). OpenAI-compatible + Anthropic-compatible endpoint.
Models: GLM-5.1, GLM-5-Turbo.

> Referral: <https://z.ai/subscribe?ic=PLKIAYEIPW>

*Checked Apr 30, 2026.*

### [BigModel.cn — GLM Coding Plan](https://www.bigmodel.cn/glm-coding)

The Chinese (mainland) counterpart of Z.ai's GLM Coding Plan — same underlying Zhipu AI models, but billed in CNY through bigmodel.cn. Suited for users who can pay via Alipay / WeChat Pay or already have a 智谱 AI account.

Plans (monthly, after the 2026 price adjustment):
- **Lite**: ¥49/month
- **Pro**: ¥149/month
- **Max**: ¥469/month

All tiers support GLM-5.1, GLM-5-Turbo, GLM-4.7, and GLM-4.5-Air. Compatible with Claude Code, Cline, and 20+ coding tools via OpenAI-compatible API plus an Anthropic-compatible endpoint.

Referral program (challenge-based, resets every 30 invitees):
- Invited friend gets **5% off** their first GLM Coding Plan order.
- Referrer gets **10% cashback** once 3 friends subscribe, plus an **additional 10%** of the total paid amount for every 30 invitees.
- Rebate credit is usable for resource packs, API calls, and subscription renewals on the BigModel platform.

Source: <https://www.bigmodel.cn/glm-coding>, <https://docs.bigmodel.cn/cn/coding-plan/overview> [^bigmodel]

Homepage: <https://www.bigmodel.cn/glm-coding>

My referral:

>🚀 Join the GLM Coding Plan via my link — get 5% off your first order. Subscribe at https://www.bigmodel.cn/glm-coding?ic=VGRZKHKNKW (invitation code: `VGRZKHKNKW`).

[^bigmodel]: Checked on May 14, 2026

### [MiniMax](https://platform.minimax.io)

Token Plan — priced per **API call**, not token. $10–$150/month.

- Starter ($10): 1,500 M2.7 requests per 5-hour window
- Plus ($20): 4,500 requests + speech/image/music generation
- Max ($50): higher quotas across all models

Models: M2.7 (language), Speech 2.8, Image-01, Hailuo video, Music-2.5. Yearly plans ~17% off.

> Referral (10% off): <https://platform.minimax.io/subscribe/token-plan?code=CAQ5sxHAq6&source=link>

*Checked Apr 30, 2026.*

### [Kimi Code](https://www.kimi.com/code)

Moonshot's coding perk bundled with Kimi membership. Models: Kimi K-series. Rolling 5-hour quota window.

Tiers: Adagio (free), Andante, Presto. Pay-as-you-go also at `platform.moonshot.ai`.

*Checked Apr 30, 2026.*

### [Alibaba Cloud Model Studio — Coding Plan](https://www.alibabacloud.com/help/en/model-studio/coding-plan)

Pro plan: **$50/month** — 6,000 req/5-hour, 45,000 req/week, 90,000 req/month.

Models: qwen3.5-plus, qwen3-max, qwen3-coder, kimi-k2.5, glm-5, MiniMax-M2.5.
Tools: Claude Code, Cursor, Cline, Codex, and more. Lite plan no longer accepting new subscribers.

*Checked Apr 30, 2026.*

### [BytePlus ModelArk — Coding Plan](https://www.byteplus.com/en/activity/codingplan)

ByteDance. Lite: **$5/month**, Pro: **$25/month**.

Models: ByteDance-Seed-2.0, DeepSeek-V3.2, GLM-5.1, Kimi-K2.5.
Tools: Claude Code, Cursor, Cline, Roo Code, OpenCode.

*Checked Apr 30, 2026.*

### [Synthetic](https://synthetic.new/)

Privacy-first inference (no training on prompts/responses). **$30/month** subscription or pay-as-you-go.

Models: Kimi K2.5, MiniMax M2.5, GLM 5.1, GLM 4.7 Flash, vLLM-compatible open-source models.
OpenAI-compatible — works with Roo, Cline, Octofriend.

*Checked Apr 22, 2026.*

---

## Free Providers

Sorted by attractiveness — largest recurring free quota first.

### [LongCat AI](https://longcat.chat/platform)

Meituan. Public beta, no paid tier yet. Resets daily 00:00 Beijing Time.

| Model | Free quota |
|---|---|
| `LongCat-Flash-Lite` | **50M tokens/day** |
| `LongCat-Flash-Chat` | 500K tokens/day |
| `LongCat-Flash-Thinking` | 500K tokens/day |
| `LongCat-Flash-Omni-2603` (multimodal) | 500K tokens/day |
| `LongCat-2.0-Preview` | 10M tokens/2h (invite-only) |

OpenAI + Anthropic compatible endpoints. 256K context on most models.

*Checked Apr 28, 2026.*

### [Mistral La Plateforme](https://console.mistral.ai)

Free Experiment plan — up to ~1B tokens/month, no credit card (phone verification only).

Models: Mistral Large 3, Medium 3, Small 3.1, Codestral, Pixtral, embeddings. OpenAI-compatible.

*Checked Apr 30, 2026.*

### [Cerebras Cloud](https://cloud.cerebras.ai)

Wafer-scale chip inference. Free tier, no credit card.

| Model | RPM | TPD |
|---|---|---|
| `gpt-oss-120b` | 30 | — |
| `llama3.1-8b-instant` | 30 | 500K |
| `qwen-3-235b-a22b-instruct-2507` | 30 | — |
| `zai-glm-4.7` | 10 | — |

1M tokens/day shared cap.

*Checked Apr 28, 2026.*

### [xAI Grok API](https://x.ai/api)

$25 signup credits + $150/month via Data Sharing Program (eligible countries).

Models: Grok 4, Grok 4.1 Fast (2M ctx), Grok Code Fast. OpenAI + Anthropic compatible.

**Warning:** Data Sharing opt-in is irreversible and lets xAI train on your prompts.

*Checked Apr 30, 2026.*

### [OpenRouter](https://openrouter.ai)

Free models (`:free` suffix): 20 RPM, 50 req/day (free accounts); 1,000 req/day after $10 top-up.

*Checked Mar 25, 2026.*

### [Groq](https://console.groq.com)

LPU inference. Free tier, no credit card.

| Model | RPM | RPD | TPM | TPD |
|---|---|---|---|---|
| `llama-3.1-8b-instant` | 30 | 14,400 | 6K | 500K |
| `llama-3.3-70b-versatile` | 30 | 1,000 | 12K | 100K |
| `whisper-large-v3` | 20 | 2,000 | — | — |

*Checked Apr 28, 2026.*

### [GitHub Models](https://github.com/marketplace/models)

Free for all GitHub accounts. OpenAI-compatible at `https://models.github.ai/inference`.

Covers OpenAI, Anthropic, Llama, Mistral, DeepSeek, Grok, Phi. Rate limits vary per model
(e.g. GPT-4o: 10 RPM/50 RPD; DeepSeek-R1: 15 RPM/150 RPD). Requires PAT with `models:read`.

*Checked Apr 30, 2026.*

### [NVIDIA NIM](https://build.nvidia.com)

Free for NVIDIA Developer Program members, no credit card. ~40 RPM, ~1,000 req/month.

Models: Kimi K2.5, GPT-OSS, DeepSeek-V3.2, Llama 3.x, Mistral, Phi, Nemotron. OpenAI-compatible.

*Checked Apr 25, 2026.*

### [Cloudflare Workers AI](https://developers.cloudflare.com/workers-ai/)

10,000 Neurons/day (resets 00:00 UTC). ~150 LLM responses/day on Llama 3.3 70B.

Models: Llama 3.3 70B, Gemma 3, Qwen2.5-Coder, DeepSeek R1, BGE embeddings, Whisper.

*Checked Apr 28, 2026.*

### [Hugging Face Inference Providers](https://huggingface.co/docs/inference-providers)

Routes across Together, Fireworks, Novita, Cerebras, Replicate, DeepInfra, Scaleway.

Free: 100K monthly credits. PRO ($9/month): 2M credits. OpenAI-compatible at `https://router.huggingface.co/v1`.

*Checked Apr 30, 2026.*

### [Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)

$300 free credits for 90 days (new GCP customers). Not a recurring free tier.

Models: Gemini 3 Pro/Flash, Anthropic Claude on Vertex, DeepSeek, GLM, Qwen via MaaS.
Express Mode available without billing for limited evaluation quotas.

*Checked Apr 30, 2026.*

### [DeepSeek Platform](https://platform.deepseek.com)

5M free tokens at signup (no code needed). OpenAI + Anthropic compatible.

PAYG: V4 Flash $0.14/M in, $0.28/M out; V4 Pro $0.435/M in, $0.87/M out (cached: $0.03/M).

*Checked Apr 30, 2026.*

### [Scaleway Generative APIs](https://www.scaleway.com/en/generative-apis/)

EU/GDPR, Paris. 1M free tokens for new customers (no time limit advertised).

Models: Qwen3 (235B/397B/coder), Llama 3.3 70B, Mistral Small 3.2, DeepSeek R1 distill, Pixtral.

*Checked Apr 28, 2026.*

### [Kilo Code — Gateway](https://kilo.ai/gateway)

VS Code + JetBrains coding extension with built-in gateway.

Free: `:free` models, 200 req/hour per IP. First top-up: $20 bonus credits (60-day expiry).
BYOK supported — no Kilo subscription required for your own provider keys.

*Checked Apr 30, 2026.*

### [Pollinations AI](https://pollinations.ai)

Open-source, Berlin. Text, image, audio, video. Free publishable key (1 pollen/IP/hour).

Models: DeepSeek V4, Flux, GPT Image, Seedream, Whisper, ElevenLabs voices. OpenAI-compatible.

*Checked Apr 28, 2026.*

### [Together AI](https://www.together.ai)

$25 signup credits (one-time). 200+ models. OpenAI-compatible — swap base URL.

*Checked Apr 30, 2026.*

### [DeepInfra](https://deepinfra.com)

Sign-up credits (one-time). 100+ models from $0.02/M. OpenAI-compatible.

*Checked Apr 30, 2026.*

### [Fireworks AI](https://fireworks.ai)

$1 starter credits. 50+ models. Function calling, MCP support. OpenAI-compatible.

*Checked Apr 30, 2026.*

### [Modal Labs](https://modal.com) — Self-Host

$30/month recurring free credits (Starter plan). Deploy any open-source LLM via vLLM
as your own OpenAI-compatible endpoint. 3 seats, 100 containers, 10 concurrent GPUs.

*Checked Apr 30, 2026.*

---

## License

Apache 2.0
