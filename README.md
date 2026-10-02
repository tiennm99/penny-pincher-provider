# Penny-Pincher Provider

Curated list of affordable and free LLM API providers — coding-plan subscriptions
and free-tier APIs. Maintained for developers who want capable models without
premium pricing.

Contributions welcome — open a pull request or
[issue](https://github.com/tiennm99/penny-pincher-provider/issues/new) to add or
update an entry.

---

## Claude AI Ecosystem

### [AgentKit](https://agentkit.best/)

AgentKit (formerly **ClaudeKit**, `claudekit.cc`) sells production-ready kits of skills, slash
commands, subagents, and workflows for coding agents — native support for Claude Code, Codex, Antigravity,
Pi, and Oh My Pi; Cursor and DeepSeek Harness in beta; OpenCode, Grok, and GitHub Copilot in preview.
**Engineer** ($99) covers frontend, backend, database, DevOps, code review, and debugging; **Marketing** ($99)
adds research, SEO, competitor-intelligence, and copywriting agents; the bundle is **$149** (108+ skills,
95+ commands, 45 subagents). The **AgentKit App** desktop cockpit (macOS/Windows) is sold separately at
**$49/yr** (1 device) or **$99/yr** (3 devices).

> Referral: **20% off** your first purchase via <https://agentkit.best/?ref=BWA910UK> (code: `BWA910UK`).

*Checked Sep 29, 2026.*

---

## Providers with Coding Plans

Monthly subscriptions with a request, credit, or allowance quota instead of pure pay-per-token billing,
compatible with Claude Code, Cursor, Cline, and similar tools.

### [Z.ai](https://z.ai/subscribe)

GLM Coding Plan, credit-based since Jul 30, 2026. **Lite $18 / Pro $80 / Max $168 per month** (quarterly −20%,
yearly −30%). Credits per 5 h / per week: Lite 2,000 / 10,000 · Pro 12,000 / 60,000 · Max 28,000 / 140,000;
off-peak usage (outside Mon–Fri 14:00–18:00 UTC+8) costs 50% fewer credits.

Models: GLM-5.3, GLM-5.3-Flash (GLM-5.2/5.1 requests auto-route to GLM-5.3, GLM-4.7 to GLM-5.3-Flash). Includes
Vision, Web Search, Web Reader, and Zread MCP.
Endpoints: Anthropic `https://api.z.ai/api/anthropic`, OpenAI `https://api.z.ai/api/coding/paas/v4`.
Tools: Claude Code, Cursor, Cline, Roo Code, Kilo Code, OpenCode, OpenClaw, Crush, Goose (supported tools only).

> Referral: <https://z.ai/subscribe?ic=PLKIAYEIPW>

*Checked Sep 29, 2026.*

### [MiniMax](https://platform.minimax.io)

Token Plan — usage-based deduction from one shared quota (5-hour rolling + weekly windows). $22–$132/month.

- Plus ($22): 3-4 agents
- Max ($55): 4-5 agents
- Ultra ($132): 6-7 agents

Covers the full MiniMax lineup (M3 / M2.7 / image / speech); MiniMax H3 video, voice design, and rapid voice
cloning are excluded. Top-up Credits: 1,000 credits = $1, valid 365 days.
OpenAI- and Anthropic-compatible. Tools: Claude Code, Codex, Cursor, TRAE, Hermes Agent, OpenClaw, Pi.

> Referral (10% off) — **For Referred Users:** 10% off subscription + become a dev ambassador. **For Referrers:** 10% back in API voucher per paid referral, usable across all MiniMax models, plus priority access to events and model previews. [View details](https://platform.minimax.io/subscribe/token-plan?code=CAQ5sxHAq6&source=link)

*Checked Sep 29, 2026.*

### [Kimi Code](https://www.kimi.com/code)

Moonshot's coding perk bundled with Kimi membership (desktop app, CLI, VS Code; Claude Code, OpenCode, Codex,
Hermes Agent via API key). Plans: Go ¥49 (no Kimi Code), **Plus ¥99**, **Pro ¥199**, **Max ¥699** per month;
annual billing saves up to ¥1,680. Rolling 5-hour window plus a monthly total (weekly cap removed for new members).

Models: `k3` (K3, up to 1M context on Pro+), `k3-256k`, `kimi-for-coding` (K2.8 Preview), `kimi-for-coding-highspeed`
(K2.7 Code, Pro+). OpenAI- and Anthropic-compatible (`https://api.kimi.ai/coding/`). Pay-as-you-go also at
`platform.moonshot.ai`.

> Referral (code: `C8CJ6F`) — sign up or subscribe via my link and we each get a guaranteed benefit, up to **1-Year Membership Credits**:
> - Sign up: <https://kimi-bot.com/activities/viral-referral/share?scenario=invite&from=share_poster&invitation_code=C8CJ6F>
> - Subscribe: <https://kimi-bot.com/activities/viral-referral/share?scenario=subscribe&from=share_poster&invitation_code=C8CJ6F>

*Checked Sep 29, 2026.*

### Alibaba Cloud Model Studio

> Referral: Up to **$1,700** in free trial credits via <https://www.alibabacloud.com/campaign/benefits?referral_code=A92LU5> (code: `A92LU5`).

#### [Token Plan](https://www.alibabacloud.com/help/en/model-studio/token-plan-overview)

Credit-based subscription (Singapore region only). Tools: Claude Code, Cursor, Qwen Code, Codex, Qoder, OpenClaw.

**Personal Edition** (monthly quota, limited-time prices):
- Lite: **$6/month** (list $8) — 11,500 Credits
- Essential: **$10/month** (list $16) — 25,500 Credits
- Standard: **$18/month** (list $25) — 45,000 Credits
- Pro: **$68/month** (list $80) — 180,000 Credits
- Extra bundle: $15 — 20,000 Credits (up to 5, needs an active plan)

**Team Edition** (per seat, no training on your data):
- Standard: **$20/seat/month** (list $30) — 25,000 Credits
- Pro: **$75/seat/month** (list $100) — 100,000 Credits
- Max: **$200/seat/month** — 250,000 Credits
- Shared quota pack: **$700** — 625,000 Credits

Models (Personal): auto, qwen3.8-max, qwen3.8-flash, qwen3.7-max, qwen3.7-plus, qwen3.6-flash, deepseek-v4.1-flash,
deepseek-v4-pro, glm-5.3, glm-5.2, plus image (qwen-image-3.0-pro, wan2.7-image/-pro), audio, and HappyHorse video.
Team Edition adds kimi-k2.7-code/k2.6/k2.5, glm-5.1/5, MiniMax-M2.5, deepseek-v3.2.

#### [Coding Plan](https://www.alibabacloud.com/help/en/model-studio/coding-plan)

Pro plan: **$50/month** — 6,000 req/5-hour, 45,000 req/week, 90,000 req/month.

Models: qwen3.7-plus, qwen3.6-plus, kimi-k2.5, glm-5, MiniMax-M2.5 (recommended); qwen3.5-plus, qwen3-max-2026-01-23,
qwen3-coder-next, qwen3-coder-plus, glm-4.7.
Endpoints: OpenAI `https://coding-intl.dashscope.aliyuncs.com/v1`, Anthropic `.../apps/anthropic`.
Tools: Claude Code, Cursor, Cline, Codex, OpenCode, Qwen Code, Qoder, Kilo CLI, OpenClaw, Hermes Agent, and more.
Lite closed to new subscribers (Mar 20, 2026) and to renewals/upgrades (Apr 13, 2026).

**Note:** limited slots, restocked daily at 00:00 UTC+8 (first come, first served); Alibaba now recommends Token Plan
instead. As of Jun 5, 2026 it was effectively unbuyable (purchase not re-tested Sep 2026).

*Checked Sep 29, 2026.*

### [opencode — Go](https://opencode.ai/go)

OpenCode subscription for curated open models. **Go $10/month**, **Go Plus $40/month** (higher limits). Limits are
monthly dollar amounts per model (5-hour = 20%, weekly = 50% of the monthly limit); e.g. Go allows ~220 GLM-5.3 or
~3,200 MiniMax M3 requests per 5 h. Falls back to Zen balance when enabled.

Models: GLM-5.3/5.3-Flash/5.2, Kimi K3/K2.7 Code/K2.6, MiniMax M3/M2.7, Qwen3.8 Max/Flash, Qwen3.7 Plus,
DeepSeek V4.1 Flash/V4 Pro/V4 Flash, MiMo-V2.6(-Pro/-Flash)/V2.5(-Pro), LongCat-2.0, Hy4 preview, Hy3, Grok 4.7/4.6,
GPT 6 Luna/5.6 Luna, plus limited-time free models.
Endpoints: `https://opencode.ai/zen/go/v1/{chat/completions,messages,responses}`. Claude Code works natively via the
Anthropic endpoint; also validated with Codex, Hermes, ZCode, Pi, jcode, Kilo Code CLI. Model format: `opencode-go/<model-id>`.

*Checked Sep 29, 2026.*

### [Synthetic](https://synthetic.new/)

Privacy-first inference (no training on prompts/responses). **$30/month per pack** ($1/day) — 500 requests/5 h,
1 concurrent request per model (buy more packs to raise both), or usage-based pay-per-token.

Models: Kimi-K3, DeepSeek-V4.1-Flash (beta), GLM-5.3-Flash, GLM-4.7-Flash, Qwen3.8-27B, gpt-oss-120b,
NVIDIA Nemotron-3-Super-120B; nomic-embed-text-v1.5 embeddings included.
OpenAI-compatible (`https://api.synthetic.new/openai/v1`) and Anthropic-compatible
(`https://api.synthetic.new/anthropic/v1`) — guides for Claude Code, Crush, OpenCode, GitHub Copilot, OpenClaw,
Xcode, Roo, KiloCode, Octofriend.

> Referral: **$10.00** in subscription credit via <https://synthetic.new/?referral=CNBFyw28zF0dZoj>

*Checked Sep 29, 2026.*

### [BytePlus ModelArk — Coding Plan](https://www.byteplus.com/en/activity/codingplan)

ByteDance. Lite: **$10/month** ($30/quarter), Pro: **$50/month** ($150/quarter). New-user first-purchase promo
($5/$25) suspended since Mar 17, 2026.
Limits: Lite ~1,900 req/5 h, ~12,000/week, ~24,000/month; Pro 5× Lite (~9,500 / ~60,000 / ~120,000).

Models: Auto, Dola-Seed-2.0-Pro/Lite/Code, ByteDance-Seed-Code, GLM-5.3-Flash, GLM-5.2, GLM-5.1, Kimi-K2.5,
DeepSeek-V4.1-Flash, DeepSeek-V4-Pro/Flash, GPT-OSS-120b.
Endpoints: OpenAI `https://ark.ap-southeast.bytepluses.com/api/coding/v3`, Anthropic `.../api/coding`.
Tools: Claude Code, Cursor, Cline, Codex, Roo Code, Kilo Code, OpenCode, OpenClaw, TraeCode, Hermes Agent.

> Referral: <https://www.byteplus.com/activity/codingplan?ac=MMAUCIS9NT1S&rc=2739UWRE> — campaign (10% off first
> order) is scheduled to end **Sep 30, 2026**.

*Checked Sep 29, 2026.*

### [Volcengine Ark — Coding Plan](https://www.volcengine.com/activity/codingplan)

ByteDance's mainland-China sibling of the BytePlus plan (火山引擎方舟 Coding Plan), billed in CNY. Lite **¥40/month**,
Pro **¥200/month** (per Volcengine's own articles; the live price widget advertises "limited-time from ¥9.9" and
needs JavaScript). Lite ~1,200 req/5 h, 9,000/week, 18,000/month; Pro 5× Lite.

Models: DeepSeek-V4.1-Flash, GLM-5.3 series, Doubao-Seed-Evolving, Kimi-K3, Kimi-K2.8-Preview. Tools: Claude Code,
Cursor, and others. Invite program: 5% voucher for the referrer, 5% off for the friend.

Source: <https://www.volcengine.com/activity/codingplan>, <https://www.volcengine.com/article/37898>

*Checked Sep 29, 2026.*

### [Atlas Cloud — Coding Plan](https://www.atlascloud.ai/coding-plan)

Third-party aggregator plan with **full API access** (rare among coding plans). Starter **$10**, Lite **$20**, Plus **$50**,
Max **$100** per month — 16.5M / 33M / 82.5M / 165M points per week.

Models: 18 LLMs incl. DeepSeek, GLM, Kimi, MiniMax. Tools: Claude Code, Codex, Cursor, OpenClaw.

Source: <https://www.atlascloud.ai/coding-plan>

*Checked Sep 29, 2026.*

### [NanoGPT](https://nano-gpt.com/pricing)

Pay-as-you-go gateway for every major model, plus an optional **Pro subscription: $12/month — 60 million included input
tokens per week** on subscription models (web + API), and 5% off eligible paid text models.

Subscription models include GLM-5.3 / 5.3-Flash, Kimi K2.6 / K2.7 Code, MiniMax M3 / M2.7, DeepSeek V4 Flash / V4 Pro,
MiMo-V2.5(-Pro), Qwen3.8-27B, Nemotron 3 Ultra. OpenAI-compatible at `https://api.nano-gpt.com/api/v1`
(also `/messages` and `/responses`); use `https://api.nano-gpt.com/api/subscription/v1` to keep requests on the
subscription only. Pay-as-you-go deposits start at $1 (card).

Source: <https://nano-gpt.com/pricing>, <https://docs.nano-gpt.com/api-reference/endpoint/subscription-usage>

*Checked Sep 29, 2026.*

### [Xiaomi MiMo Open Platform](https://platform.xiaomimimo.com)

I'm on Xiaomi MiMo Open Platform — running Xiaomi's flagship MiMo V2.6 and the rest of the lineup. Sign up with my code and you'll instantly get $2 in API credits.

After signup, enter the code at the bottom-left of the console. Credits valid 40 days.

**Token Plan** (monthly): Lite $6 / ¥39 (4.1B credits), Standard $16 / ¥99 (11B), Pro $50 / ¥329 (38B),
Max $100 / ¥659 (82B). Annual plans 12% off; 12% off first Individual purchase; 0.8× consumption 00:00–08:00
Beijing time. Team Edition from $16/seat. Models: mimo-v2.6-pro, mimo-v2.6-flash, ASR/TTS (mimo-v2.5 and
mimo-v2.5-pro retire Oct 21, 2026). Works with OpenCode, OpenClaw, Claude Code.

> Referral: Code `T8ESAY` · <https://platform.xiaomimimo.com?ref=T8ESAY>

*Checked Sep 29, 2026.*

### [GitHub Copilot Pro](https://github.com/features/copilot/plans)

Cheapest mainstream coding seat. **$10/month** — unlimited code completions and next-edit suggestions, plus
**1,500 GitHub AI Credits/month** (1,000 base + 500 flex; 1 credit = $0.01) for chat, agent mode, code review,
cloud agent, and CLI. Pro models include Claude Haiku 4.5, Sonnet 4.6/5/5.5, GPT-5.4/5.6 Luna/6 Luna, Gemini 3.x
Flash, Grok 4.x, Kimi K3 — Opus/Fable and GPT-6 Sol/Astra need Pro+ or Max.
Copilot Pro+ is $39/month (7,000 credits); Copilot Max is $100/month (20,000 credits). Extra usage billed at $0.01/credit.

Free tier: 2,000 completions/month plus a small AI-credit allowance, auto model selection only, no card.
Free Copilot Student for verified students; free Pro for verified teachers and maintainers of popular open-source repos.

Tools: VS Code, JetBrains, Neovim, Xcode, Visual Studio, Copilot CLI, Copilot app, and the Copilot cloud agent on
github.com.

*Checked Sep 29, 2026.*

---

## Free Providers

### [TokenRouter](https://www.tokenrouter.com/)

Unified AI gateway (145 models listed) exposing OpenAI-, Anthropic- and Gemini-format APIs behind one key.

- **Free model:** `nvidia/nemotron-3-nano-omni-30b-a3b-reasoning:free` at $0/M input and output.
- **Launch promos:** TokenRouter runs short free windows on self-hosted launches (e.g. GLM 5.3 was free for all accounts, no card, until Sep 4, 2026). Watch the [blog](https://www.tokenrouter.com/blog).
- **API:** OpenAI Chat Completions at `https://api.tokenrouter.com/v1` with a TokenRouter API key.

Source: [TokenRouter models](https://www.tokenrouter.com/models)

*Checked Sep 29, 2026.*

### [OrcaRouter](https://www.orcarouter.ai/)

OpenAI-compatible gateway with access to 200+ models, automatic routing, and failover (also accepts Anthropic and Gemini formats).

> Referral: <https://www.orcarouter.ai/ref/ref_3976ba42abf37dc55c1d> (code: `ref_3976ba42abf37dc55c1d`).

- **Always-free models ($0):** `deepseek/deepseek-v4-flash-free`, `z-ai/glm-5.3-flash-free`, `tencent/hy4-preview-free`, `tencent/hy3-free`, plus the `orcarouter/free` router. Requires a linked GitHub account with some history, or any paid purchase.
- **Hy4 Deposit Match:** 100% match on top-ups for `tencent/hy4-preview` (min $20 top-up, cap ≈$200 derived from API quota units), enroll by **Oct 28, 2026**.
- **DeepSeek V4.1 Flash Deposit Match:** 30% match (min $20 top-up, up to $100), enroll by **Oct 2, 2026**.
- **GPT-6 Astra Deposit Match:** 100% match for `openai/gpt-6-astra` (min $20, up to $100), card required, enroll by **Oct 5, 2026**.
- **API:** `https://api.orcarouter.ai/v1`.

Offers can change quickly; check the [live offers page](https://www.orcarouter.ai/offers) before claiming.

*Checked Sep 29, 2026.*

### [OpenRouter](https://openrouter.ai)

Free models (`:free` suffix): 20 RPM, 50 req/day; 1,000 req/day once you have bought at least $10 in credits (all time). BYOK requests are not gated by the free-model cap.

Current free lineup includes NVIDIA Nemotron 3 Ultra 550B / Super 120B / 3.5 Lightning, Google Gemma 4 (26B-A4B, 31B), Qwen3.8-27B, Poolside Laguna S/XS 2.1, Thinking Machines Inkling / Inkling Small, Cohere North Mini Code, plus the `openrouter/free` auto-router. OpenAI-compatible at `https://openrouter.ai/api/v1`.

*Checked Sep 29, 2026.*

### [NVIDIA NIM](https://build.nvidia.com)

Free prototyping endpoints for NVIDIA Developer Program members, no credit card. Rate-limited per model (commonly ~40 RPM per community reports); NVIDIA does not publish a fixed quota and does not raise free-tier limits on request.

Models: Kimi K3, Kimi K2.6, DeepSeek V4.1 Flash, GLM 5.3 / 5.3 Flash, Nemotron 3 Ultra / Super / 3.5 Lightning, GPT-OSS-20B, Gemma 4 31B, Mistral Large. OpenAI-compatible at `https://integrate.api.nvidia.com/v1`.

**Warning:** trial terms say use is logged and may be used to improve NVIDIA products — do not send personal or confidential data.

*Checked Sep 29, 2026.*

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

### [Google AI Studio](https://aistudio.google.com/)

Google's developer platform for Gemini models. Free tier (no billing) with pay-as-you-go available.

Free-tier models: Gemini 3.8 / 3.7 / 3.6 / 3.5 Flash, Gemini 3.5 Flash-Lite, Gemini 3.1 Flash-Lite, Gemini 3 Flash Preview, plus Live/TTS variants and Gemma 4. **Gemini 3.1 Pro Preview is paid-only.** Gemini 2.5 models are now limited to projects that already used them.

Google no longer publishes a fixed free-tier table — limits are per project and shown in AI Studio. Third-party reports (Sep 2026): ~20 RPD on the 3.x Flash models, ~500 RPD on 3.5 / 3.1 Flash-Lite. RPD resets at midnight Pacific.

OpenAI-compatible endpoint: `https://generativelanguage.googleapis.com/v1beta/openai/`.

**Warning:** In the Free tier, Google may use your prompts and responses to improve their products. Use the Paid tier or Vertex AI for privacy.

*Checked Sep 29, 2026.*

### [Kilo Code — Gateway](https://kilo.ai/gateway)

VS Code + JetBrains coding extension (and CLI) with a built-in OpenAI-compatible gateway at `https://api.kilo.ai/api/gateway`. Kilo was acquired by Anaconda.

Free: `:free` models and the `kilo-auto/free` router, 200 req/hour per IP (anonymous or signed in). Current free models include Nemotron 3 Ultra / Super / 3.5 Lightning, Qwen3.8-27B, Laguna S/XS 2.1, Inkling Small, North Mini Code, and Step 3.7 Flash.
BYOK supported with no Kilo markup. Kilo Pass ($19/$49/$199 per month) adds up to 50% bonus credits.

**Warning:** Auto Free may route to providers that log prompts and use them for training (including NVIDIA trial endpoints).

*Checked Sep 29, 2026.*

### [Cloudflare Workers AI](https://developers.cloudflare.com/workers-ai/)

10,000 Neurons/day free on both Workers Free and Paid (resets 00:00 UTC). Roughly ~49K output tokens/day on Llama 3.3 70B or ~147K on GPT-OSS-120B.

Models: GPT-OSS 120B/20B, Kimi K2.5, Llama 3.3 70B, Llama 4 Scout, Gemma 4 26B, Qwen3.8-27B, Nemotron 3 120B, GLM-4.7-Flash, Mistral Small 3.1, BGE embeddings, Whisper. Kimi K2.6/K2.7-Code, GLM 5.x and DeepSeek V4 require Workers Paid or AI Gateway credits.

OpenAI-compatible at `https://api.cloudflare.com/client/v4/accounts/<ACCOUNT_ID>/ai/v1`.

*Checked Sep 29, 2026.*

### [DeepSeek Platform](https://platform.deepseek.com)

New accounts are widely reported to get 5M free tokens (granted balance, ~30 days, phone verification) — verify in your console. OpenAI (`https://api.deepseek.com`) + Anthropic (`https://api.deepseek.com/anthropic`) compatible.

PAYG (off-peak / peak, per 1M tokens): `deepseek-flash` (V4.1 Flash) $0.15/$0.30 in, $0.60/$1.20 out; `deepseek-v4-pro` $0.66/$1.32 in, $1.98/$3.96 out. Off-peak is half price — everything outside 01:00–04:00 and 06:00–10:00 UTC on weekdays. 1M context.

*Checked Sep 29, 2026.*

### [Groq](https://console.groq.com)

LPU inference. Free plan (no card reported; not restated in current docs). OpenAI-compatible at `https://api.groq.com/openai/v1`.

| Model | RPM | RPD | TPM | TPD |
|---|---|---|---|---|
| `openai/gpt-oss-120b` | 30 | 1K | 8K | 200K |
| `openai/gpt-oss-20b` | 30 | 1K | 8K | 200K |
| `qwen/qwen3.8-27b` | 30 | 1K | 8K | 200K |
| `whisper-large-v3` / `-turbo` | 20 | 2K | — | 7.2K audio-sec/hour |

Llama 3.1 8B and Llama 3.3 70B are now Enterprise-only (contact sales).

*Checked Sep 29, 2026.*

### [Mistral Studio](https://console.mistral.ai)

Formerly "La Plateforme". Free plan (default for new accounts) includes **$10/month in API credits**, shared across Studio, the API, and Vibe Code; rate limits shown in the Admin Console. Enable pay-as-you-go to continue past the allowance. Pro ($14.99/month) includes $15/month in API credits (per the pricing page; verify).

Models (indicative): Mistral Medium 3.5, Mistral Large (2512), Mistral Small (2603), Devstral 2, Codestral, Ministral 3B/8B/14B, Voxtral, embeddings. OpenAI-compatible.

**Warning:** Model training on your data is opt-out, not opt-in.

*Checked Sep 29, 2026.*

### [Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)

Now branded **Gemini Enterprise Agent Platform** (formerly Vertex AI).

Free Trial: **$300** credit for 90 days (new GCP customers only; card verification). Not a recurring free tier. The $300 credit **cannot** pay for partner models offered as MaaS (e.g. Claude) or for Gemini API in AI Studio.

Express mode: `@gmail.com` accounts new to Google Cloud get a **90-day free tier with no billing info**, within express-mode quotas, on the APIs that support express mode (Gemini models). Separate from the $300 Free Trial.

Models: Gemini 3.x (Pro / Flash / Flash-Lite); partner models (Claude and others) need a paid billing account.

*Checked Sep 29, 2026.*

### [Hugging Face Inference Providers](https://huggingface.co/docs/inference-providers)

Router in front of 20 partners: Baseten, Cerebras, Cohere, DeepInfra, Fal AI, Featherless AI, Fireworks, Groq, HF Inference, Novita, Nscale, OVHcloud, Public AI, Replicate, Scaleway, Together, WaveSpeedAI, Z.ai and others. No markup over provider rates.

Free: **$0.10/month** in credits (subject to change). PRO (**$9/month**): **$2.00/month** in credits, usable across all HF compute. Pay-as-you-go beyond that requires buying credits.

OpenAI-compatible at `https://router.huggingface.co/v1` (~130 chat models).

*Checked Sep 29, 2026.*

### [Cerebras Cloud](https://cloud.cerebras.ai)

Wafer-scale chip inference. **Free Trial only**: **$5** in credits after adding a **verified payment method**, expiring 30 days after grant. No permanently free tier. OpenAI-compatible at `https://api.cerebras.ai/v1`.

| Model | RPM | Uncached TPM | TPD | Context (free) |
|---|---|---|---|---|
| `gpt-oss-120b` | 5 | 30K | 1M | 65K |
| `qwen-3.8-27b` | 5 | 30K | 1M | 64K |

Total TPM (incl. cached) is 3x uncached (90K). Access stops when credits run out or expire until you buy credits.

*Checked Sep 29, 2026.*

### [Fireworks AI](https://fireworks.ai)

**$1** in free starter credits for serverless inference. Without a payment method (or without credits) the account is capped at **10 RPM**; adding a payment method raises it up to 6,000 RPM.

Models: GLM 5.3 / 5.3 Flash, Kimi K3, DeepSeek V4 Flash, Qwen 3.8 27B and other open models. Function calling, MCP support.

OpenAI-compatible at `https://api.fireworks.ai/inference/v1`; Anthropic-compatible at `https://api.fireworks.ai/inference` (works with Claude Code).

*Checked Sep 29, 2026.*

### [Scaleway Generative APIs](https://www.scaleway.com/en/generative-apis/)

EU/GDPR, Paris. Free tier for new customers: first **1,000,000 tokens** plus **60 minutes** of audio transcription (no time limit advertised). OpenAI-compatible at `https://api.scaleway.ai/v1`.

Models: GLM-5.2, DeepSeek V4 Flash, Qwen3.8-27B, Qwen3.5-397B, Qwen3.6-35B, Qwen3-235B, Qwen3-Coder-30B, Gemma 4 26B, Mistral Medium 3.5, Mistral Small 3.2, gpt-oss-120b, Llama 3.3 70B, Pixtral 12B, Whisper.

*Checked Sep 29, 2026.*

### [SambaNova Cloud](https://cloud.sambanova.ai)

RDU (dataflow chip) inference. **Free tier** applies when no payment method is linked: **20 RPM, 20 requests/day, 200K tokens/day** per model. Adding a card moves you to the Developer tier (pay-as-you-go, 60–240 RPM, 20M tokens/day across models). The $5 signup credit is no longer advertised, and the Plans page now says to add a payment method first — the two official pages disagree.

Free-tier models: DeepSeek-V3.1, DeepSeek-V3.2 (preview), Llama 3.3 70B, gpt-oss-120b, Gemma 4 31B (preview).

OpenAI-compatible and Anthropic-compatible at `https://api.sambanova.ai/v1`.

Source: <https://docs.sambanova.ai/docs/en/models/rate-limits>

*Checked Sep 29, 2026.*

### [Cohere](https://dashboard.cohere.com/api-keys)

Trial API key, no credit card. **1,000 calls/month**, 20 RPM per chat model (Rerank 10 RPM, Embed 2,000 inputs/min).

Models: Command A+, Command A Reasoning / Vision / Translate, Command A, Command R+, Command R, Command R7B, North Mini Code, Aya Expanse / Aya Vision, plus rerank and embeddings.

OpenAI-compatible at `https://api.cohere.ai/compatibility/v1`.

**Warning:** trial keys are **not permitted for production or commercial use** — production needs a production key (paid). New model variants (e.g. Command A Reasoning) stay at trial limits even on prod keys.

*Checked Sep 29, 2026.*

### [Vercel AI Gateway](https://vercel.com/docs/ai-gateway)

Single endpoint routing to many providers, with failover and BYOK. OpenAI-compatible at `https://ai-gateway.vercel.sh/v1`; also Anthropic Messages, OpenResponses and Cohere-compatible APIs.

Free: a **monthly included credit** (reported as **$5 / 30 days**; does not roll over), starting with your first request. **Requires a valid payment method on the team.** Covers only free-tier-eligible models with lower per-model rate limits. Buying credits moves you to the paid tier permanently and the monthly free credit stops.

Source: <https://vercel.com/docs/ai-gateway/pricing>

*Checked Sep 29, 2026.*

### [Requesty](https://www.requesty.ai/)

LLM gateway with routing, caching, spend controls and EU data residency. Works with Claude Code, Cline, Cursor, Roo.

Free: **200 req/day** on the free-model catalogue. No credit card, no trial clock — same platform as pay-as-you-go (600+ models, +5% fee), just restricted to free models until you upgrade.

OpenAI-compatible at `https://router.requesty.ai/v1`; Claude Code via `ANTHROPIC_BASE_URL=https://router.requesty.ai`.

Source: <https://www.requesty.ai/free-models>, <https://www.requesty.ai/pricing>

*Checked Sep 29, 2026.*

### [SiliconFlow](https://cloud.siliconflow.cn/)

Chinese multi-model inference platform, 200+ LLM/image/audio/video models. International site: <https://www.siliconflow.com>.

Free: a set of smaller open-source models is **permanently ¥0** with fixed rate limits (chat models from 1,000 RPM / 50K TPM); the international site gives **$1** starter credit.

Models (free, CN site): Qwen3-8B (128K), Qwen3.5-4B (256K), Qwen2.5-7B, GLM-4-9B-0414, GLM-Z1-9B-0414, DeepSeek-R1-0528-Qwen3-8B, Hunyuan-MT-7B, Xing4.0-29B, plus OCR, ASR and BGE embedding/rerank models.

OpenAI-compatible at `https://api.siliconflow.cn/v1`; Anthropic-compatible endpoint documented (Claude Code guide in docs).

*Checked Sep 29, 2026.*

### [ModelScope](https://modelscope.cn/)

Alibaba's model community (魔搭). API-Inference free for registered users.

Free: **2,000 req/day** total, **≤500 req/day per model** (some large models lower; figures from secondary sources — the official limits page needs JavaScript). Requires binding an Alibaba Cloud account with real-name verification. Quotas may be adjusted at any time.

Models: ~35 API-Inference models, incl. DeepSeek V4 Pro / V4.1 Flash, Qwen3.5 / Qwen3.8, GLM-5.2, GLM-4.7-Flash, MiniMax-M3, Step-3.7-Flash, LongCat-Flash-Lite, Intern-S1.

OpenAI-compatible at `https://api-inference.modelscope.cn/v1`; Anthropic-compatible at `https://api-inference.modelscope.cn` (`/v1/messages`).

*Checked Sep 29, 2026.*

### [Ollama Cloud](https://ollama.com/cloud)

Hosted counterpart to the local `ollama` CLI — same commands and API, models run on Ollama's GPUs. Prompts are not used for training.

Free: a **starter amount of usage credits each month** (exact amount unpublished) on a smaller set of **starter models**, **1 concurrent request**, no credit card. Buying pay-as-you-go credits unlocks all cloud models. Session/weekly caps were removed on Aug 31, 2026.

Models: DeepSeek V4, GLM-5.3, Kimi K3 / K2.7 Code, MiniMax M3, gpt-oss, Gemma 4, Nemotron 3, Mistral Large 3 (paid rates published per model).

OpenAI-compatible at `https://ollama.com/v1`; Anthropic-compatible at `https://ollama.com/v1/messages`.

*Checked Sep 29, 2026.*

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

### [AMD Token Factory (Radeon Cloud)](https://developer.amd.com.cn/radeon/tokenfactory)

AMD's official inference platform on Radeon GPUs. Free shared endpoints after sign-in; usage is metered in
"points" against a daily allowance (reported as ~$10-equivalent/day, resets daily — not stated on the public page).
OpenAI-compatible at `https://developer.amd.com.cn/radeon/api/v1`.

Free models: DeepSeek-V4.1-Flash, DeepSeek-V4-Flash (+ Vision-Exp), MiMo-V2.6-Flash, GLM-5.3-Flash, Qwen3.8-Flash-Next,
Qwen3.8-27B, MiniCPM5-2B (1M context on the DeepSeek/MiMo models). Marked "experimental" stability; high
time-to-first-token has been reported.

Source: <https://developer.amd.com.cn/radeon/tokenfactory>

*Checked Sep 29, 2026.*

### [iFlytek Spark](https://xinghuo.xfyun.cn/sparkapi)

讯飞星火. **Spark Lite is free** (model id `lite`, 8K input / 4K output), throttled by per-second and concurrency limits
(third-party reports: 2 QPS, no token cap). OpenAI SDK-compatible at `https://spark-api-open.xf-yun.com/v1`
with `Authorization: Bearer <APIPassword>` from the console. Individual real-name verification required.

Source: <https://www.xfyun.cn/doc/spark/HTTP%E8%B0%83%E7%94%A8%E6%96%87%E6%A1%A3.html>

*Checked Sep 29, 2026.*

### [AIHubMix](https://aihubmix.com/models/free)

Gateway with **60 free models**, no credit card. Every free model speaks Chat Completions, Messages, and Responses at
`https://aihubmix.com/v1` (model IDs end in `-free`).

Free: 10 trial calls at signup (never expire). A **one-time top-up of $1+** permanently unlocks
**100 req/day, 10 req/min, 1M tokens/day** on the free catalogue (resets daily).

Free models include coding-glm-5.3(-flash), coding-kimi-k3, coding-minimax-m3, xiaomi-mimo-v2.6-pro/flash, mimo-v2.5-pro,
gpt-5.5, gemini-3.8-flash, qwen3.6-plus-preview, hy3, nemotron-3-ultra/super, gemma-4-31b-it, gpt-oss-20b, glm-4.7-flash.

Source: <https://aihubmix.com/models/free>

*Checked Sep 29, 2026.*

### [OVHcloud AI Endpoints](https://www.ovhcloud.com/en/public-cloud/ai-endpoints/catalog/)

EU-hosted (France). **Anonymous free tier — no API key, no signup**: 2 RPM per IP per model
(with a key: 400 RPM per project per model, pay-per-token). OpenAI SDK-compatible at
`https://oai.endpoints.kepler.ai.cloud.ovh.net/v1`.

Models: Qwen3.5-397B-A17B, Qwen3.8-27B, Qwen3.6-27B, Qwen3-Coder-30B-A3B, gpt-oss-120b/20b, Llama 3.3 70B,
Mistral Small 3.2, Mistral Nemo, Qwen2.5-VL-72B, plus Whisper, embeddings, and TTS.

Source: <https://docs.ovhcloud.com/en/guides/public-cloud/ai-machine-learning/ai-endpoints-getting-started>

*Checked Sep 29, 2026.*

### [LLM7.io](https://token.llm7.io)

Gateway with keyless access. Anonymous: 10 req/min, 60 req/hour, **500K tokens/day**; a free token from
`token.llm7.io` raises this to 40 req/min, 100 req/hour, **1M tokens/day**. OpenAI-compatible at `https://api.llm7.io/v1`.

Free (`turbo`-tier) models: DeepSeek-V4-Flash-0731 (400K ctx), codestral-latest, minimax-m2.7 (180K ctx), Mistral Nemo.
Everything else needs Pro ($12/month) or a topped-up balance.

Source: <https://docs.llm7.io/limits>

*Checked Sep 29, 2026.*

### [Token Harbor](https://tokenharbor.ai/pricing)

Small gateway. **Free tier $0/month** with a rolling allowance (amount unpublished, unused allowance carries over).
Agent Pass **$1.99/month** ($0.99 first month) adds $10 of included usage. OpenAI-compatible at `https://tokenharbor.ai/v1`.

Free models: DeepSeek V4.1 Flash, MiMo V2.6 Flash, TH-Rudder ("promotional models added over time").

**Warning:** free models are opt-in and their prompts/responses may be retained for diagnostics and model
improvement. Access is restricted in some regions (reported: mainland China, Hong Kong, Macau).

Source: <https://tokenharbor.ai/pricing>

*Checked Sep 29, 2026.*

### [Aion Labs](https://www.aionlabs.ai/app/api-keys/)

Permanent free tier, no credit card. **15 RPM, 20K tokens/day**. OpenAI-compatible at `https://api.aionlabs.ai/v1`.

Models: aion-3.5 / aion-3.5-mini (256K ctx), aion-3.0 / aion-3.0-mini, aion-2.0 (128K ctx, reasoning),
aion-rp-llama-3.1-8b. Tuned for roleplay/storytelling rather than coding.

Source: <https://www.aionlabs.ai/docs/rate-limits>

*Checked Sep 29, 2026.*

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

### [Alibaba Cloud Model Studio — free quota](https://www.alibabacloud.com/help/en/model-studio/new-free-quota)

New users get **1,000,000 free tokens per model** (typical), valid **90 days** from activation (or model release /
approval, whichever is later). Singapore region, international deployment scope only; real-time inference only
(no batch/fine-tune). Each model — and each dated snapshot — has its own quota; RAM users share the account's pool.
OpenAI-compatible at `https://dashscope-intl.aliyuncs.com/compatible-mode/v1`.

Source: <https://www.alibabacloud.com/help/en/model-studio/new-free-quota>

*Checked Sep 29, 2026.*

### [Z.ai API — free Flash models](https://docs.z.ai/guides/overview/pricing)

Zhipu's international platform (no mainland ID needed). **GLM-4.7-Flash**, **GLM-4.5-Flash** (text) and **GLM-4.6V-Flash** (vision) are priced
**Free** for input, cached input, and output. OpenAI-compatible at `https://api.z.ai/api/paas/v4`.

Rate/concurrency limits for free models are shown only in the console (not published).

Source: <https://docs.z.ai/guides/overview/pricing>

*Checked Sep 29, 2026.*

### [Nebius Token Factory](https://tokenfactory.nebius.com/)

Formerly Nebius AI Studio; EU-based open-model inference (60+ models). **$1 trial credit on first sign-up, valid 30 days**; joining the
free **Nebius Builder Program** adds a **$25 Token Factory credit** (open to everyone; meant for learning/testing).
OpenAI-compatible at `https://api.tokenfactory.nebius.com/v1`.

**Warning:** setting up a billing account (bank card) is mandatory to finish onboarding.

Source: <https://docs.tokenfactory.nebius.com/other-capabilities/billing-new>, <https://dev.nebius.com/builders>

*Checked Sep 29, 2026.*

### [Novita AI](https://novita.ai/pricing)

Open-model inference platform. Two models are priced **$0 in / $0 out**: `inclusionai/ling-3.1-flash` and
`inclusionai/ling-3.0-flash-sante` (262K ctx). OpenAI-compatible at `https://api.novita.ai/openai`.

Rate limits for the free models and any signup credit: not published on the pricing page.

Source: <https://novita.ai/pricing>

*Checked Sep 29, 2026.*

---

## License

Apache 2.0
