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

AgentKit (formerly **ClaudeKit**, `claudekit.cc`) sells production-ready kits of skills, slash commands,
and workflows for coding agents — 7 runtimes: Claude Code, Codex, Cursor, Pi, Oh My Pi, DeepSeek Harness, and Grok
(Antigravity, OpenCode, and GitHub Copilot in preview). **Engineer** ($99, one-time) covers planning, implementation,
testing, code review, debugging, and shipping; **Marketing** ($99, one-time) adds research,
competitor-intelligence, content, and growth skills. The **Bundle** is **$149**: both kits plus 12 months of the
**AgentKit Desktop App** (3 devices). The Desktop App alone is **$49/yr** (1 device) or **$99/yr** (3 devices),
native on macOS, Windows, and Linux.

> Referral: **20% off** your first purchase via <https://agentkit.best/?ref=BWA910UK> (code: `BWA910UK`).

*Checked Nov 20, 2026.*

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
Endpoints: Anthropic `https://api.z.ai/api/anthropic`, OpenAI `https://api.z.ai/api/coding/paas/v4`. For keys created from
Oct 16, 2026, only a key made under **API Keys → Personal Coding Plan** draws plan quota; a Standard API key is billed
pay-as-you-go (older keys on plan accounts keep working as "Compatible").
Tools (plan usable only in these): Claude Code, Codex, OpenCode, Pi, Cursor, Cline, TRAE, Qoder, Droid, Kilo Code,
Roo Code, Crush, Goose, OpenClaw, Hermes Agent, and more.

> Referral: <https://z.ai/subscribe?ic=PLKIAYEIPW>

*Checked Nov 20, 2026.*

### [MiniMax](https://www.minimax.io/m-plan)

**M Plan** (replaced Token Plan for new buyers) — one shared quota with 5-hour and weekly windows (image and video only
the weekly window). **Go $22 / Explore $55 / Build $132 per month**; usage 1× / 3× / 7.5× of Go. Annual billing:
pay 10 months, get 2 free.

All tiers: MiniMax M3.1 Flash text, H3 Image, speech, web search, and image understanding; Explore and Build add H3
video. Overflow draws from purchased Credits (valid one year). Separate M Plan API key; OpenAI- and Anthropic-compatible
(`https://api.minimax.io/anthropic`). Tools: MiniMax Code, Claude Code, Codex, Cursor, OpenCode, Pi, Hermes Agent,
OpenClaw.

*Checked Nov 20, 2026.*

### [Kimi Code](https://www.kimi.com/code)

Moonshot's coding perk bundled with Kimi membership (desktop app, CLI, VS Code; Claude Code, OpenCode, Codex,
Hermes Agent via API key). Plans: Go ¥49 (no Kimi Code), **Plus ¥99**, **Pro ¥199**, **Max ¥699**, **Ultra ¥1,399**
per month; annual billing saves up to ¥3,360/year. Rolling 5-hour window plus a monthly total (weekly cap removed for
new members). Optional pay-as-you-go **Extra Usage** balance (from ¥25) once the quota runs out.

Models: `k3.1-pro` (K3.1 Pro, thinking only), `k3.1-pro-highspeed` (Pro+), `k3`, `k3-256k`, `kimi-for-coding`
(K2.8 Preview), `kimi-for-coding-highspeed` (K2.7 Code, Pro+); 1M context on Pro+. OpenAI- and Anthropic-compatible
(`https://api.kimi.ai/coding/`, mainland `https://api.kimi.com/coding/`). Pay-as-you-go also at `platform.moonshot.ai`.

> Referral (code: `C8CJ6F`) — sign up or subscribe via my link and we each get a guaranteed benefit, up to **1-Year Membership Credits**:
> - Sign up: <https://kimi-bot.com/activities/viral-referral/share?scenario=invite&from=share_poster&invitation_code=C8CJ6F>
> - Subscribe: <https://kimi-bot.com/activities/viral-referral/share?scenario=subscribe&from=share_poster&invitation_code=C8CJ6F>

*Checked Nov 20, 2026.*

### Alibaba Cloud Model Studio

> Referral: sign up through <https://www.alibabacloud.com/campaign/benefits?referral_code=A92LU5> (code: `A92LU5`) to try
> Token Plan, with Qwen and leading third-party models through OpenAI-compatible APIs.

#### [Token Plan](https://www.alibabacloud.com/help/en/model-studio/token-plan-overview)

Credit-based subscription (Singapore region only), monthly quota, no weekly cap. Tools: Claude Code, Cursor, Codex,
Qwen Code, Qoder, OpenClaw, Hermes Agent, TRAE, DeepSeek Harness.

**Personal Edition** (quotas raised Nov 9, 2026):
- Lite: **$6/month** — 20,000 Credits (new-user price **$3** for accounts that never bought a Personal plan, until Nov 30, 2026 UTC+8)
- Essential: **$10/month** — 45,000 Credits (new-user price **$5** for accounts that never bought a Personal plan, until Nov 30, 2026 UTC+8)
- Standard: **$18/month** — 80,000 Credits
- Pro: **$43/month** — 200,000 Credits
- Extra bundle: $15 — 20,000 Credits (up to 5, needs an active plan)

**Team Edition** (per seat, no training on your data):
- Standard: **$20/seat/month** — 25,000 Credits
- Advanced: **$75/seat/month** — 100,000 Credits
- Premium: **$180/seat/month** — 250,000 Credits
- Shared quota pack: **$700** — 625,000 Credits

Models (Personal): auto, qwen4-max, qwen3.8-max, qwen3.8-flash, qwen3.7-max, qwen3.7-plus, qwen3.6-flash,
deepseek-v4.1-flash, deepseek-v4-pro, glm-5.3, glm-5.2, plus image (qwen-image-3.0-pro, wan2.7-image/-pro), audio, and
video (wan3.0-video, HappyHorse 1.1). Team Edition adds qwen3.6-plus, kimi-k2.7-code/k2.6/k2.5, glm-5.1/5, MiniMax-M2.5.

#### [Coding Plan](https://www.alibabacloud.com/help/en/model-studio/coding-plan)

Pro plan: **$50/month** — 6,000 req/5-hour, 45,000 req/week, 90,000 req/month.

Models (exact versions only): qwen3.7-plus, qwen3.6-plus, kimi-k2.5, glm-5, MiniMax-M2.5 (recommended); qwen3.5-plus.
Endpoints: OpenAI `https://coding-intl.dashscope.aliyuncs.com/v1`, Anthropic `.../apps/anthropic`.
Tools: Claude Code, Cursor, Cline, Codex, OpenCode, Qwen Code, Qoder, Kilo CLI, OpenClaw, Hermes Agent, and more.
Lite closed to new subscribers (Mar 20, 2026) and to renewals/upgrades (Apr 13, 2026).

**Note:** limited slots, restocked daily at 00:00 UTC+8 (first come, first served). As of Jun 5, 2026 it was effectively
unbuyable (purchase not re-tested Nov 2026).

*Checked Nov 20, 2026.*

### [opencode — Go](https://opencode.ai/go)

OpenCode subscription for curated open (and some closed) models. **Go $10/month**, **Go Plus $40/month** (higher
limits), **Go Teams $20/member/month** (2-member minimum; each member gets their own allowance). Limits are monthly
dollar amounts per model (5-hour = 20%, weekly = 50% of the monthly limit); e.g. Go allows ~3,210 MiniMax-M3 or
~994 Kimi K2.7 Code requests per 5 h. Extra Usage falls back to your Console credit when enabled.

Models (32): GLM-5.3/5.3-Flash/5.2, Kimi K3.1 Pro/K3/K2.7 Code, MiniMax M3/M3.1 Flash, Qwen4 Max, Qwen3.8 Max/Flash,
Qwen3.7 Plus, DeepSeek V4.1 Flash/V4 Pro, MiMo-V2.6-Pro/-Flash, LongCat-2.0, Hy4, Hy4 preview, Hy3, Step 5 Preview,
Grok 4.7, GPT-6 Luna, GPT-5.6 Luna, Claude Haiku 5.5, Gemini 4 Argon, plus limited-time free models.
Endpoints: Anthropic `https://opencode.ai/inference/go/anthropic/v1`, OpenAI `https://opencode.ai/inference/go/openai/v1`
(chat completions and responses); model list at `https://opencode.ai/inference/go/v1/models`. Works in OpenCode, Claude Code, Codex, Pi,
Hermes; also validated with ZCode, jcode, Kilo Code CLI. Model format: `opencode-go/<model-id>`.

*Checked Nov 20, 2026.*

### [Synthetic](https://synthetic.new/)

Privacy-first inference ("we never train on your data, and we never store API prompts or completions"). Plans:
**Go $9**, **Standard $30**, **Big $90**, **Bigger $300** per month. One weekly credit limit that regenerates over the week; models draw credits at discounted rates.
The Big and Bigger plans include Fast mode (2× speed, 2× credits) and Infinite mode (slow, never counts against the limit;
DeepSeek V4.1 Flash only), both in beta.

Models: Kimi-K3.1-Pro, GLM-5.3 (beta), GLM-5.3-Flash, GLM-4.7-Flash, DeepSeek-V4.1-Flash-1017, Qwen3.8-27B,
gpt-oss-120b.
OpenAI-compatible (`https://api.synthetic.new/openai/v1`) and Anthropic-compatible
(`https://api.synthetic.new/anthropic/v1`) — guides for Claude Code, Crush, OpenCode, GitHub Copilot, OpenClaw,
Xcode, Octofriend.

> Referral: subscribe via <https://synthetic.new/?referral=CNBFyw28zF0dZoj> and we each get **$10.00** in subscription
> credit on the Standard plan or higher, or **$3.00** on the Go plan. It doesn't stack with other offers.

*Checked Nov 20, 2026.*

### [BytePlus ModelArk — Coding Plan](https://www.byteplus.com/en/activity/codingplan)

ByteDance. Lite: **$10/month** ($30/quarter), Pro: **$50/month** ($150/quarter). New-user first-purchase promo
($5/$25) suspended since Mar 17, 2026.
Limits: Lite ~1,900 req/5 h, ~12,000/week, ~24,000/month; Pro 5× Lite (~9,500 / ~60,000 / ~120,000). Coding tools only,
not for raw API calls.

Models: Auto, Dola-Seed-2.0-Pro/Lite/Code, GLM-5.2, GLM-5.3-Flash, DeepSeek-V4.1-Flash, DeepSeek-V4-Pro/Flash
(GLM and DeepSeek models with 1M context).
Endpoints: OpenAI `https://ark.ap-southeast.bytepluses.com/api/coding/v3`, Anthropic `.../api/coding`.
Tools: Claude Code, Cursor, Cline, Codex, Roo Code, Kilo Code, OpenCode, OpenClaw, TraeCode, Hermes Agent.

*Checked Nov 20, 2026.*

### [Volcengine Ark — Coding Plan](https://www.volcengine.com/activity/codingplan)

ByteDance's mainland-China sibling of the BytePlus plan (火山引擎方舟 Coding Plan), billed in CNY. Lite and Pro tiers
(monthly, quarterly, yearly); list prices are shown only after login and were not verified. Lite ~1,200 req/5 h, ~9,000/week,
~18,000/month; Pro ~6,000 / ~45,000 / ~90,000. Coding tools only.

Models: DeepSeek-V4.1-Flash-1017, GLM-5.3 series, Doubao-Seed-Evolving, Kimi-K3.1-pro, and more (Doubao Seed 2.0,
MiniMax, Kimi, DeepSeek series), or Auto. Tools: Claude Code, Codex CLI, Cursor, TRAE, OpenCode, OpenClaw, Hermes Agent.
A separate **Agent Plan** (Small / Medium / Large / Max, "限时 9.9 元起") adds multimodal models and web-search harness.

Source: <https://www.volcengine.com/activity/codingplan>, <https://www.volcengine.com/docs/82379/2165245>

*Checked Nov 20, 2026.*

### [Atlas Cloud — Coding Plan](https://www.atlascloud.ai/coding-plan)

Third-party aggregator plan with **full API access** (rare among coding plans). Starter **$10**, Lite **$20**, Plus **$50**,
Max **$100**, Ultra **$200**, Enterprise **$500** per month — 16.5M / 33M / 82.5M / 165M / 330M / 825M points per week,
plus a monthly cap (whichever hits first; weekly resets Monday 00:00 UTC). Pay-per-use packs: $99 / $299 / $599
(280M / 850M / 1,700M points, valid 90 days).

Models: 18 LLMs incl. DeepSeek V4.1 Flash / V4 Pro, GLM-5.3-Flash / 5.2, Kimi K2.7 Code, Qwen3.8 Max, Doubao Seed 2.1,
MiniMax M2.5. Tools: Claude Code, Codex, Cursor, OpenClaw (20+ supported).

Source: <https://www.atlascloud.ai/coding-plan>

*Checked Nov 20, 2026.*

### [NanoGPT](https://nano-gpt.com/pricing)

Pay-as-you-go gateway for every major model (no markup over list prices), plus an optional **Pro subscription:
$12/month — 60 million included input tokens per week** on subscription models (web + API; output on included models
is free, cached input counts in full), **100 images/day** on 4 image models, and 5% off eligible paid text models.
Resets every Monday 00:00 UTC; closed models (Claude, GPT, Gemini, Grok), video, and voice are billed from balance.

Subscription models include GLM-5.3 / 5.3-Flash, Kimi K2.6 / K2.7 Code, MiniMax M3 / M3.1 Flash, DeepSeek V4.1 Flash /
V4 Pro, MiMo-V2.6-Pro / -Flash, Qwen3.8-27B / Flash, Nemotron 3 Ultra. OpenAI-compatible at
`https://api.nano-gpt.com/api/v1` (also `/messages` and `/responses`); use `https://api.nano-gpt.com/api/subscription/v1`
to keep requests on the subscription only. Pay-as-you-go deposits start at $1 (card).

Source: <https://nano-gpt.com/pricing>, <https://docs.nano-gpt.com/api-reference/endpoint/subscription-usage>

*Checked Nov 20, 2026.*

### [Xiaomi MiMo Open Platform](https://platform.xiaomimimo.com)

Invite builders to try MiMo V2.6, Xiaomi's flagship model: friends who sign up with my code get **10% off** their first
paid Token Plan order, applied automatically at checkout. Auto-bind via the link, or enter the code in the console
sidebar after signup.

**Token Plan** (monthly): Lite $6 / ¥39 (4.1B credits), Standard $16 / ¥99 (11B), Pro $50 / ¥329 (38B),
Max $100 / ¥659 (82B). Annual plans 12% off; 12% off first Individual purchase; 0.8× consumption 00:00–08:00
Beijing time. Team Edition from $16/seat. Models: mimo-v2.6-pro, mimo-v2.6-flash, ASR/TTS (TTS free for a limited
time); Pro and Max add mimo-v2.6-pro-ultraspeed. Works with OpenCode, OpenClaw, Claude Code.

> Referral: Code `T8ESAY` · <https://platform.xiaomimimo.com?ref=T8ESAY>

*Checked Nov 20, 2026.*

### [GitHub Copilot Pro](https://github.com/features/copilot/plans)

Cheapest mainstream coding seat. **$10/month** — unlimited code completions and next-edit suggestions, plus
**1,500 GitHub AI Credits/month** (1,000 base + 500 flex; 1 credit = $0.01) for chat, agent mode, code review,
cloud agent, and CLI. Pro models include Claude Haiku 4.5/5.5, Sonnet 4.6/5/5.5, GPT-5.3-Codex, GPT-5.6 Luna,
GPT-6 Luna, GPT-6.1 Terra, Gemini 3.8 Flash, Gemini 4 Hydrogen, Grok 4.5/4.6/4.7, Kimi K3, MAI Code — Opus, Fable,
Gemini 4 Argon/Carbon/Neon, and GPT-6.x Sol/Astra need Pro+ or Max.
Copilot Pro+ is $39/month (7,000 credits); Copilot Max is $100/month (20,000 credits). Extra usage billed at $0.01/credit.

Free tier: 2,000 completions/month plus a small AI-credit allowance, auto model selection only, no card.
Free Copilot Student for verified students; free Pro for verified teachers and maintainers of popular open-source repos.

Tools: VS Code, JetBrains, Neovim, Xcode, Visual Studio, Copilot CLI, Copilot app, and the Copilot cloud agent on
github.com.

*Checked Nov 20, 2026.*

### [StepFun — Step Plan](https://platform.stepfun.ai/step-plan)

Credit-based monthly allowance (~$1 ≈ 7M Credits), no 5-hour or weekly windows. **Flash Mini
$6.99** (400M Credits), **Flash Plus $9.99** (1,600M), **Flash Pro $29** (8,000M), **Flash Max $99** (40,000M) per
month; quarterly and yearly prepay cheaper. Booster packs $6.99 / 400M and $9.99 / 1,600M (30-day validity).

Models: step-5-preview, step-3.7-flash, step-3.5-flash, step-3.5-flash-2603, plus StepAudio 2.5 TTS/ASR.
Endpoints: Anthropic `https://api.stepfun.ai/step_plan` (Claude Code), OpenAI `https://api.stepfun.ai/step_plan/v1`.
Tools: Claude Code, Cursor, Trae, OpenClaw, and others. Pay by Stripe or account balance.

Source: <https://platform.stepfun.ai/docs/en/step-plan/overview.md>

*Checked Nov 20, 2026.*

### [Tencent Cloud — Token Plan](https://www.tencentcloud.com/document/product/1300/81315)

International (Singapore region) Personal Edition of Tencent's TokenHub plan, credit-based monthly quota. **Lite $7**
(1,000 credits), **Standard $17** (2,600), **Pro $51** (7,900), **Max $103** (15,900) per month; one plan per root
account, shared with sub-accounts. Supported AI tools only, no scripts or app backends. The mainland CNY plan and free
trial are under Tencent TokenHub in Free Providers.

Models: Hy4, Hy4 flash, GLM-5.3-Flash, GLM-5.2, Kimi K3, Kimi-K2.6, DeepSeek-V4.1-Flash-1017, DeepSeek-V4-Pro/Flash,
MiniMax-M3, MiMo-V2.6-Flash, Auto.
Endpoints: OpenAI `https://tokenhub-intl.tencentcloudmaas.com/plan/v3`, Anthropic
`https://tokenhub-intl.tencentcloudmaas.com/plan/anthropic` (dedicated `sk-tp-` key).
Tools: Claude Code, Codex, Cursor, Cline, OpenCode, Kilo Code, TRAE, CodeBuddy, OpenClaw, and more.

Source: <https://www.tencentcloud.com/document/product/1300/81315>

*Checked Nov 20, 2026.*

### [LLM Gateway — DevPass](https://devpass.llmgateway.io/pricing)

Open-source (AGPLv3 core, self-hostable) LLM gateway with a flat-price plan for coding agents. **Lite $29 / Pro $79 /
Max $179 per month**, each including **2×** its price in model usage ($58 / $158 / $358) metered at provider list rates.
Daily pacing caps each rolling 24 h at 8% / 9% / 10% of the monthly allowance; models priced $5+/M input or $15+/M
output share a weekly fair-use slice (10% / 12% / 15%). Unused allowance carries over up to the plan price. Monthly
billing only; no provider pinning on DevPass.

Without a plan: pay-as-you-go at provider list rates plus a **5% fee on credit top-ups** (+1.5% for non-US cards,
$10 minimum); BYOK is free. No free models are live — the catalogue's $0 models were all deactivated by Oct 15, 2026.

OpenAI-compatible at `https://api.llmgateway.io/v1`, Anthropic Messages at `/v1/messages`. Works with Claude Code,
OpenCode, Cursor, Cline, Codex CLI, and other OpenAI/Anthropic-compatible tools.

> Referral: <https://llmgateway.io/?ref=jdsmz02j3nmaB9BqziZt>

Source: <https://devpass.llmgateway.io/pricing.md>, <https://llmgateway.io/pricing.md>

*Checked Nov 20, 2026.*

---

## Free Providers

### [TokenRouter](https://www.tokenrouter.com/)

Unified AI gateway (155 models listed) exposing OpenAI-, Anthropic- and Gemini-format APIs behind one key.

- **Free model:** `nvidia/nemotron-3-nano-omni-30b-a3b-reasoning:free` at $0/M input and output.
- **Launch promos:** TokenRouter runs short free windows on self-hosted launches (e.g. GLM 5.3 was free for all accounts, no card, until Sep 4, 2026). Watch the [blog](https://www.tokenrouter.com/blog).
- **API:** OpenAI Chat Completions at `https://api.tokenrouter.com/v1` with a TokenRouter API key.

Source: [TokenRouter models](https://www.tokenrouter.com/models)

*Checked Nov 20, 2026.*

### [OrcaRouter](https://www.orcarouter.ai/)

OpenAI-compatible gateway with access to 200+ models, automatic routing, and failover (also accepts Anthropic and Gemini formats).

> Referral: <https://www.orcarouter.ai/ref/ref_3976ba42abf37dc55c1d> (code: `ref_3976ba42abf37dc55c1d`).

- **Always-free models ($0):** `deepseek/deepseek-v4.1-flash-free`, `deepseek/deepseek-v4-flash-free`, `z-ai/glm-5.3-flash-free`, `tencent/hy4-preview-free`, `tencent/hy3-free`, plus the `orcarouter/free` router. Requires a linked GitHub account with some history, or any paid purchase.
- **DeepSeek V4.1 Flash "Unlimited" Deposit Match:** 100% match on top-ups for `deepseek/deepseek-v4.1-flash` (min $20 top-up, no cap listed), enroll by **Dec 18, 2026**; match credit expires Jan 17, 2027.
- **Fable 5.2 Deposit Match:** 100% match for `anthropic/claude-fable-5.2` (min $10 top-up, cap ≈$200 derived from API quota units), enroll by **Dec 11, 2026**; match credit expires Jan 10, 2027.
- **API:** `https://api.orcarouter.ai/v1`.

Offers can change quickly; check the [live offers page](https://www.orcarouter.ai/offers) before claiming.

*Checked Nov 20, 2026.*

### [OpenRouter](https://openrouter.ai)

Free models (`:free` suffix): 20 RPM, 50 req/day; 1,000 req/day once you have bought at least $10 in credits (all time). BYOK requests are not gated by the free-model cap.

Current free lineup includes NVIDIA Nemotron 3 Ultra / 3.5 Super VL / 3.5 Lightning / 3 Nano Omni, Google Gemma 4 (26B-A4B, 31B), inclusionAI Ling 3.2 Flash, Baidu ERNIE 5.5 Flash Preview, Recursive Flint, Particle-1, LiquidAI LFM3-1.7B, Dots3-Note Preview, plus the `openrouter/free` auto-router. OpenAI-compatible at `https://openrouter.ai/api/v1`.

*Checked Nov 20, 2026.*

### [NVIDIA NIM](https://build.nvidia.com)

Free prototyping endpoints for NVIDIA Developer Program members, no credit card. Rate-limited per model (commonly ~40 RPM per community reports); NVIDIA does not publish a fixed quota and does not raise free-tier limits on request.

Models: Kimi K3.1 Pro, MiniMax M3.1 Flash, Mistral Large 4, GLM 5.3 Flash, Step 5 Preview, Nemotron 3 Ultra / 3.5 Super VL / 3.5 Lightning / 3 Nano Omni, Gemma 4 31B, Laguna XS 2.1, Muse Glimmer 30B. OpenAI-compatible at `https://integrate.api.nvidia.com/v1`.

**Warning:** trial terms say use is logged and may be used to improve NVIDIA products — do not send personal or confidential data.

*Checked Nov 20, 2026.*

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

### [Google AI Studio](https://aistudio.google.com/)

Google's developer platform for Gemini models. Free tier (no billing) with pay-as-you-go available.

Free-tier models: Gemini 4 Hydrogen, Gemini 3.8 / 3.6 Flash, Gemini 3.5 / 3.1 Flash-Lite, Gemini 3 Flash Preview, plus TTS / Live / Transcribe variants, embeddings and Gemma 4. **Gemini 4 Carbon / Argon / Neon and Gemini 3.1 Pro Preview are paid-only.** Gemini 3.7 Flash and 3.5 Flash are deprecated (requests re-route to 3.8 / 3.6 Flash); Gemini 2.5 Pro and 2.5 Flash re-route to 3.8 Flash and 3.5 Flash-Lite on Dec 1, 2026.

Google no longer publishes a free-tier rate-limit table — limits are per project and shown in AI Studio. RPD resets at midnight Pacific. Some free projects need verification.

OpenAI-compatible endpoint: `https://generativelanguage.googleapis.com/v1beta/openai/`.

**Warning:** In the Free tier, Google may use your prompts and responses to improve their products. Use the Paid tier or Vertex AI for privacy.

*Checked Nov 20, 2026.*

### [Kilo Code — Gateway](https://kilo.ai/gateway)

VS Code + JetBrains coding extension (and CLI) with a built-in OpenAI-compatible gateway at `https://ai-gateway.kilo.ai/api/v1`. Kilo was acquired by Anaconda.

Free: `:free` models and the `kilo-auto/free` router, 200 req/hour per IP (anonymous or signed in). Current free models include Nemotron 3 Ultra / 3.5 Super VL / 3.5 Lightning / 3 Nano Omni, Ling 3.2 Flash, ERNIE 5.5 Flash Preview, Flint, Beam 1.0, Particle-1, LFM3-1.7B and Dots3-Note Preview.
BYOK supported with no Kilo markup (5% processing fee on credit purchases). Kilo Pass ($19/$49/$199 per month) adds up to 50% bonus credits.

**Warning:** Auto Free may route to providers that log prompts and use them for training (including NVIDIA trial endpoints).

*Checked Nov 20, 2026.*

### [Cloudflare Workers AI](https://developers.cloudflare.com/workers-ai/)

10,000 Neurons/day free on both Workers Free and Paid (resets 00:00 UTC). Roughly ~49K output tokens/day on Llama 3.3 70B or ~147K on GPT-OSS-120B.

Models: GPT-OSS 120B/20B, Kimi K2.5, Llama 3.3 70B, Llama 4 Scout, Gemma 4 26B, Qwen3.8-27B, Nemotron 3 120B, GLM-4.7-Flash, Mistral Small 3.1, BGE embeddings, Whisper. Kimi K2.6/K2.7-Code, GLM 5.2/5.3/5.3-Flash, DeepSeek V4 Flash/V4.1 Flash/V4 Pro and Inkling 2 Small require Workers Paid or AI Gateway credits.

OpenAI-compatible at `https://api.cloudflare.com/client/v4/accounts/<ACCOUNT_ID>/ai/v1`.

*Checked Nov 20, 2026.*

### [DeepSeek Platform](https://platform.deepseek.com)

New accounts are widely reported to get 5M free tokens (granted balance, ~30 days, phone verification) — verify in your console. OpenAI (`https://api.deepseek.com`) + Anthropic (`https://api.deepseek.com/anthropic`) compatible.

PAYG (off-peak / peak, per 1M tokens): `deepseek-flash` (V4.1 Flash) $0.15/$0.30 in, $0.60/$1.20 out; `deepseek-v4-pro` $0.66/$1.32 in, $1.98/$3.96 out. Off-peak is half price — everything outside 01:00–04:00 and 06:00–10:00 UTC on weekdays. 1M context.

*Checked Nov 20, 2026.*

### [Groq](https://console.groq.com)

LPU inference. Free plan (no card reported; not restated in current docs). OpenAI-compatible at `https://api.groq.com/openai/v1`.

| Model | RPM | RPD | TPM | TPD |
|---|---|---|---|---|
| `openai/gpt-oss-120b` | 30 | 1K | 8K | 200K |
| `openai/gpt-oss-20b` | 30 | 1K | 8K | 200K |
| `qwen/qwen3.8-27b` | 30 | 1K | 8K | 200K |
| `whisper-large-v3` / `-turbo` | 20 | 2K | — | 7.2K audio-sec/hour |

Llama 3.1 8B and Llama 3.3 70B are now Enterprise-only (contact sales).

*Checked Nov 20, 2026.*

### [Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)

Now branded **Gemini platform** (formerly Gemini Enterprise Agent Platform / Vertex AI).

Express mode: `@gmail.com` accounts new to Google Cloud get a **90-day free tier with no billing info**, within express-mode quotas, on the APIs that support express mode (Gemini models). For new users this is the only no-cost way to use Gemini on the platform.

Free Trial: **$300** credit for 90 days (new GCP customers only; card or other payment method required). **For sign-ups or upgrades on or after Nov 16, 2026, the $300 credit cannot pay for Gemini platform services**; it also never covers partner models offered as MaaS (e.g. Claude) or Gemini API in AI Studio.

Partner models (Claude and others) need a paid billing account.

*Checked Nov 20, 2026.*

### [Cerebras Cloud](https://cloud.cerebras.ai)

Wafer-scale chip inference. **Free Trial only**: **$5** in credits after adding a **verified payment method**, expiring 30 days after grant. No permanently free tier. OpenAI-compatible at `https://api.cerebras.ai/v1`.

| Model | RPM | Uncached TPM | Total TPM | Token caps | Context (free) |
|---|---|---|---|---|---|
| `gpt-oss-120b` | 5 | 30K | 90K | 1M/hour, 1M/day | 65K |
| `qwen-3.8-27b` | 300 | 150K | 750K (temporary; normally 450K) | none | 64K |

Qwen 3.8 27B has the same per-minute limits on Free Trial and Pay as You Go. Access stops when credits run out or expire until you buy credits.

*Checked Nov 20, 2026.*

### [Fireworks AI](https://fireworks.ai)

**$1** in free starter credits for serverless inference. Without a payment method (or without credits) the account is capped at **10 RPM**; adding a payment method raises it up to 6,000 RPM.

Models: GLM 5.3 / 5.3 Flash, Kimi K3 / K3.1 Pro, DeepSeek V4.1 Flash, Qwen 3.8 27B / 3.8 Max and other open models. Function calling, MCP support.

OpenAI-compatible at `https://api.fireworks.ai/inference/v1`; Anthropic-compatible at `https://api.fireworks.ai/inference` (works with Claude Code).

*Checked Nov 20, 2026.*

### [Scaleway Generative APIs](https://www.scaleway.com/en/generative-apis/)

Now "Generative APIs - Serverless". EU/GDPR, Paris. Free tier for new customers: first **1,000,000 tokens** plus **60 minutes** of audio transcription (no time limit advertised; applied to the most expensive tokens first). OpenAI-compatible at `https://api.scaleway.ai/v1`.

Models: GLM-5.3, GLM-5.2, DeepSeek V4.1 Flash, DeepSeek V4 Flash, Qwen3.8-27B, Qwen3.5-397B, Qwen3.6-35B, Qwen3-235B, Qwen3-Coder-30B, Gemma 4 26B, Mistral Medium 3.5, Mistral Small 3.2, gpt-oss-120b, Llama 3.3 70B, Pixtral 12B, Voxtral Small, Whisper.

*Checked Nov 20, 2026.*

### [SambaNova Cloud](https://cloud.sambanova.ai)

RDU (dataflow chip) inference. **Free tier** applies when no payment method is linked: **20 RPM, 20 requests/day, 200K tokens/day** per model. Adding a card moves you to the Developer tier (pay-as-you-go, 60 RPM / 12,000 requests/day per model, 20M tokens/day across models). The $5 signup credit is no longer advertised, and the Plans page says to add a payment method and purchase credits first — the two official pages disagree.

Free-tier models: gpt-oss-120b, Gemma 4 31B. All SambaCloud models are labelled Preview (evaluation only, not for production).

OpenAI-compatible and Anthropic-compatible at `https://api.sambanova.ai/v1`.

Source: <https://docs.sambanova.ai/docs/en/models/rate-limits>

*Checked Nov 20, 2026.*

### [Cohere](https://dashboard.cohere.com/api-keys)

Trial API key, no credit card. **1,000 calls/month**, 20 RPM per chat model (Rerank 10 RPM, Embed 2,000 inputs/min).

Models: Command A+, Command A Reasoning / Vision / Translate, Command A, Command R+, Command R, Command R7B, North Mini Code, Aya Expanse / Aya Vision, plus rerank and embeddings.

OpenAI-compatible at `https://api.cohere.ai/compatibility/v1`.

**Warning:** trial keys are **not permitted for production or commercial use** — production needs a production key (paid). New model variants (e.g. Command A Reasoning) stay at trial limits even on prod keys.

*Checked Nov 20, 2026.*

### [Vercel AI Gateway](https://vercel.com/docs/ai-gateway)

Single endpoint routing to many providers, with failover and BYOK (BYOK needs purchased credits). OpenAI-compatible at `https://ai-gateway.vercel.sh/v1`; also Anthropic Messages, OpenResponses and Cohere-compatible APIs.

Free: a **monthly included credit** (reported as **$5 / 30 days**; does not roll over), starting with your first request. **Requires a valid payment method on the team.** Covers only free-tier-eligible models with lower per-model rate limits. Buying credits moves you to the paid tier permanently and the monthly free credit stops. $0 promo models currently listed: Reflection Beam 1.0, NVIDIA Nemotron 3.5 Lightning, Recursive Flint, Ampersand v0.1 and the stealth Glyph Cluster.

Source: <https://vercel.com/docs/ai-gateway/pricing>

*Checked Nov 20, 2026.*

### [Requesty](https://www.requesty.ai/)

LLM gateway with routing, caching, spend controls and EU data residency. Works with Claude Code, Cline, Cursor, Roo.

Free: **200 req/day** on the free-model catalogue. No credit card, no trial clock — same platform as pay-as-you-go (600+ models, +5% fee), just restricted to free models until you upgrade.

OpenAI-compatible at `https://router.requesty.ai/v1`; Claude Code via `ANTHROPIC_BASE_URL=https://router.requesty.ai`.

Source: <https://www.requesty.ai/free-models>, <https://www.requesty.ai/pricing>

*Checked Nov 20, 2026.*

### [SiliconFlow](https://cloud.siliconflow.cn/)

Chinese multi-model inference platform, 200+ LLM/image/audio/video models. International site: <https://www.siliconflow.com>.

Free: a set of smaller open-source models is **permanently ¥0** with fixed rate limits (chat models from 1,000 RPM / 50K TPM); the international site gives **$1** starter credit.

Models (free, CN site): Qwen3-8B (128K), Qwen3.5-4B (256K), Qwen2.5-7B, GLM-4-9B-0414, GLM-Z1-9B-0414, DeepSeek-R1-0528-Qwen3-8B, Hunyuan-MT-7B, Xing4.0-29B, plus OCR, ASR and BGE embedding/rerank models.

Currently also ¥0: **GLM-5.3-Flash** (1M ctx, 500 RPM / 2M TPM). It is not on the permanent free list and has a fallback price on file (¥0.8 / ¥2.8 per M), so treat it as a promo with no published end date.

OpenAI-compatible at `https://api.siliconflow.cn/v1`; Anthropic-compatible endpoint documented (Claude Code guide in docs).

*Checked Nov 20, 2026.*

### [ModelScope](https://modelscope.cn/)

Alibaba's model community (魔搭). API-Inference is free, non-commercial, and paid for with **Magicubes** (free points).

Free: **200 Magicubes/day** for signing in plus **50/day** after linking an Alibaba Cloud account (both expire the same day; one-time profile and referral bonuses last 90 days). Calls cost **~0.5 / 1 / 2 Magicubes** for lightweight / standard / flagship models, so ~125–500 calls/day. Requires a linked Alibaba Cloud account with real-name verification and a verified email. Concurrency is throttled dynamically (single-concurrency guaranteed).

Models: ~38 API-Inference models, incl. DeepSeek V4 Pro / V4.1 Flash, Kimi K3.1 Pro, Qwen3.5 / Qwen3.8, GLM-5.2, GLM-4.7-Flash, MiniMax-M3, Step-3.7-Flash / Step-5-Preview, LongCat-Flash-Lite, Intern-S1/S2.

OpenAI-compatible at `https://api-inference.modelscope.cn/v1`; Anthropic-compatible at `https://api-inference.modelscope.cn` (`/v1/messages`).

Source: <https://modelscope.cn/docs/model-service/API-Inference/limits>, <https://modelscope.cn/docs/magicube/intro>

*Checked Nov 20, 2026.*

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

### [AMD Token Factory (Radeon Cloud)](https://developer.amd.com.cn/radeon/tokenfactory)

AMD's official inference platform on Radeon GPUs (beta). **12 "Public Free Model APIs"** after sign-in; usage is metered
in points against a daily allowance (amount shown only after login). OpenAI-compatible at `https://developer.amd.com.cn/radeon/api/v1`.

Free models: DeepSeek-V4.1-Flash-1017, DeepSeek-V4-Flash-0731, MiMo-V2.6-Flash, GLM-5.3-Flash, Qwen3.8-27B, Gemma-4-31B-IT,
MiniCPM-V-4.7 (35B-A3B / 1B), MiniCPM5-2B, plus decision models d3, d3-flash and Clef. The page shows live load; popular
models often read "Busy" or "At capacity".

Outside China, AMD AI Developer Program members get "instant API access through Token Lab" (limits not published).

Source: <https://developer.amd.com.cn/radeon/tokenfactory>, <https://www.amd.com/en/developer/ai-dev-program.html>

*Checked Nov 20, 2026.*

### [iFlytek Spark](https://xinghuo.xfyun.cn/sparkapi)

讯飞星火. **Spark Lite is free** (model id `lite`, 8K input / 4K output), throttled by per-second and concurrency limits
(third-party reports: 2 QPS, no token cap). OpenAI SDK-compatible at `https://spark-api-open.xf-yun.com/v1`
with `Authorization: Bearer <APIPassword>` from the console. Individual real-name verification required.

Source: <https://www.xfyun.cn/doc/spark/HTTP%E8%B0%83%E7%94%A8%E6%96%87%E6%A1%A3.html>

*Checked Nov 20, 2026.*

### [AIHubMix](https://aihubmix.com/models/free)

Gateway with **76 free models**, no credit card. Every free model speaks Chat Completions, Messages, and Responses at
`https://aihubmix.com/v1` (model IDs end in `-free`).

Free: 10 trial calls at signup (never expire). A **one-time top-up of $1+** permanently unlocks
**100 req/day, 10 req/min, 1M tokens/day** on the free catalogue (resets daily).

Free models include coding-glm-5.3(-flash), coding-kimi-k3, kimi-for-coding, coding-minimax-m3, xiaomi-mimo-v2.6-pro/flash,
gpt-5.5, gemini-3.8-flash, qwen3.8-max, qwen3.8-flash, hy3, nemotron-3-ultra/super, gemma-4-31b-it, gpt-oss-20b, glm-4.7-flash.

Source: <https://aihubmix.com/models/free>

*Checked Nov 20, 2026.*

### [OVHcloud AI Endpoints](https://www.ovhcloud.com/en/public-cloud/ai-endpoints/catalog/)

EU-hosted (France). **Anonymous free tier — no API key, no signup**: 2 RPM per IP per model
(with a key: 400 RPM per project per model, pay-per-token). OpenAI SDK-compatible at
`https://oai.endpoints.kepler.ai.cloud.ovh.net/v1`.

Models: Qwen3.5-397B-A17B, DeepSeek-V4.1-Flash, Qwen3.8-27B, Qwen3.6-27B, Qwen3.6-35B-A3B, gpt-oss-120b/20b, Gemma 4 26B-A4B,
Llama 3.3 70B, Mistral Small 3.2, Nemotron 3 Nano, Qwen2.5-VL-72B, Qwen3-VL-30B, plus Whisper, embeddings, TTS and SDXL.

Source: <https://docs.ovhcloud.com/en/guides/public-cloud/ai-machine-learning/ai-endpoints-getting-started>

*Checked Nov 20, 2026.*

### [LLM7.io](https://llm7.io)

Pay-as-you-go gateway (top up from $5). Keyless calls to `https://api.llm7.io/v1` still answered on Nov 20, 2026
(the `fast` selector routed to codestral-latest), but **LLM7 no longer publishes free-tier terms**: the old limits page
is gone and the docs now ask for an API key from `dash.llm7.io`.

Low-cost `turbo`-tier models: codestral-latest, gemma-3-27b, gpt-oss:20b, Mistral Nemo. Everything else is `pro`.

**Warning:** undocumented free access can disappear without notice — don't depend on it.

Source: <https://docs.llm7.io/guides/models-api>, <https://api.llm7.io/v1/models>

*Checked Nov 20, 2026.*

### [Token Harbor](https://tokenharbor.ai/pricing)

Small gateway. **Free tier $0/month**, no card: a free allowance that resets on a **rolling 7-day period** (amount unpublished).
Agent Pass **$1.99/month** ($0.99 first month) adds $10 of included usage on top of the free allowance. OpenAI-compatible at `https://tokenharbor.ai/v1`.

Free models: DeepSeek V4.1 Flash, MiMo V2.6 Flash, TH-Rudder ("promotional models added over time").

**Warning:** free models are opt-in; while enabled, Token Harbor may retain free-route prompts/responses, its staff may read
them, and the serving providers may train on them. Some regions are unavailable.

Source: <https://tokenharbor.ai/pricing>

*Checked Nov 20, 2026.*

### [Aion Labs](https://www.aionlabs.ai/app/api-keys/)

Permanent free tier, no credit card. **15 RPM, 20K tokens/day**. OpenAI-compatible at `https://api.aionlabs.ai/v1`.

Models: aion-3.5 / aion-3.5-mini (256K ctx), aion-3.0 / aion-3.0-mini, aion-2.0 (128K ctx, reasoning),
aion-rp-llama-3.1-8b. Tuned for roleplay/storytelling rather than coding.

Source: <https://www.aionlabs.ai/docs/rate-limits>

*Checked Nov 20, 2026.*

### [Experiential Labs](https://platform.experientiallabs.ai)

"Open-source OpenRouter" gateway (1,000+ models). Free and promotional models need a one-time **card verification**
(a temporary $1 hold, released, not charged). Promo models draw from their own allowance, not your wallet. Your first purchase
is matched up to 2,500 credits ($25). OpenAI-compatible (Chat + Responses) and Anthropic-compatible at `https://api.experientiallabs.ai/v1`.

$0 at the Free tier right now: DeepSeek V4.1 Flash, DeepSeek V4.1 Flash 1017 (ZDR), GPT-6 Luna, Claude Haiku 5.5 (100% off),
DeepSeek V4 Flash (100% off), Qwen3.8 27B (100% off), Jev, Clef. Promos rotate.

**Warning:** prompt/response capture is one org-wide switch — turn it off or require ZDR routes for private code. Prototyping only.

Source: <https://platform.experientiallabs.ai/docs/billing>, <https://platform.experientiallabs.ai/models>

*Checked Nov 20, 2026.*

### [Tencent TokenHub](https://cloud.tencent.com/document/product/1823/130053)

Tencent Cloud's model platform.

- **Free trial:** **every language model and every multimodal-understanding model gets 1M tokens**, once per main account per
  model, valid **1 year** from claim. Claim from Model Square ("新用户福利免费体验") or let it auto-claim on your first call.
  This round runs until **Dec 31, 2026**. Without post-paid billing enabled, the service simply stops when the quota is used up.
- **Token Plan (monthly):** Hy plan **¥28** (Lite, 560 pts) to ¥468; universal plan ¥39 (780 pts) to ¥599. Universal models: Auto,
  DeepSeek-V4.1-Flash-1017, DeepSeek-V4-Pro / V4-Flash, GLM-5.3 / 5.3-Flash / 5.2, Kimi K3, Kimi K2.7 Code, MiniMax-M3,
  MiMo-V2.6-Flash, Hy4 / Hy4 flash (Hy4 preview retires Dec 7, 2026). The international USD plan is listed under Providers with Coding Plans.
- Plan endpoints: OpenAI `https://tokenhub.tencentmaas.com/plan/v3`, Anthropic `https://tokenhub.tencentmaas.com/plan/anthropic`.
  Plan keys are for AI tools only (Claude Code, OpenClaw, etc.); scripted or backend API use is banned. No refunds.

Source: <https://cloud.tencent.com/document/product/1823/130053>, <https://cloud.tencent.com/document/product/1823/130060>

*Checked Nov 20, 2026.*

### [Alibaba Cloud Model Studio — free quota](https://www.alibabacloud.com/help/en/model-studio/new-free-quota)

New users get **1,000,000 free tokens per model** (typical), valid **90 days** from activation (or model release /
approval, whichever is later). Singapore region, international deployment scope only; real-time inference only
(no batch/fine-tune). Each model — and each dated snapshot — has its own quota; RAM users share the account's pool.
You must complete your account information before activating. Usage past the quota is billed pay-as-you-go
automatically — turn on **Free Quota Only** in the console to stop at zero instead.
OpenAI-compatible at `https://dashscope-intl.aliyuncs.com/compatible-mode/v1`.

Source: <https://www.alibabacloud.com/help/en/model-studio/new-free-quota>

*Checked Nov 20, 2026.*

### [Z.ai API — free Flash models](https://docs.z.ai/guides/overview/pricing)

Zhipu's international platform (no mainland ID needed). **GLM-4.7-Flash**, **GLM-4.5-Flash** (text) and **GLM-4.6V-Flash** (vision) are priced
**Free** for input, cached input, and output. OpenAI-compatible at `https://api.z.ai/api/paas/v4`.

Rate/concurrency limits for free models are shown only in the console (not published).

Source: <https://docs.z.ai/guides/overview/pricing>

*Checked Nov 20, 2026.*

### [Nebius Token Factory](https://tokenfactory.nebius.com/)

Formerly Nebius AI Studio; EU-based open-model inference (60+ models). No sign-up credit is documented any more; joining the free
**Nebius AI Builder Program** (sign up, verify email) gives a **$25 Token Factory credit**, plus $25 Tavily and $50 Toloka credit.
OpenAI-compatible at `https://api.tokenfactory.nebius.com/v1`.

**Warning:** setting up a billing account (bank card) is mandatory to finish onboarding.

Source: <https://docs.tokenfactory.nebius.com/other-capabilities/billing-new>, <https://dev.nebius.com/builders>

*Checked Nov 20, 2026.*

### [GonkaRouter](https://gonkarouter.io/pricing)

Gateway onto the Gonka decentralized inference network. **1M free tokens for new users** (email or Google sign-in, no credit card),
used before any paid balance. After that, one flat rate for every model: **~$0.006 per 1M tokens** in and out (floats with the
Gonka network price). Top up by card, Alipay or USDT.

Models: GLM-5.3-Flash, DeepSeek-V4-Flash-0731, MiniMax-M2.7. In practice prompts are capped near 200K tokens per request.

OpenAI-compatible at `https://api.gonkarouter.io/v1`; Anthropic-compatible with base URL `https://api.gonkarouter.io`.

**Warning:** young service on a decentralized network — check its privacy policy before sending private code.

Source: <https://gonkarouter.io/pricing>, <https://gonkarouter.io/docs>

*Checked Nov 20, 2026.*

### [Baidu Qianfan — new-user free quota](https://cloud.baidu.cn/doc/qianfan/s/Imi2rpirg)

百度千帆. On first activation, **1M free tokens on each of 17 preset models**, valid **3 months**, granted automatically.
Online inference only (not batch). Models: ERNIE-4.5-Turbo-128K / 32K / VL, ERNIE-X1-Turbo-32K, DeepSeek-R1 (+0528),
DeepSeek-V3-0324, DeepSeek-V3.1 (+Think), Kimi-K2-Instruct, Qwen3-235B-A22B-Instruct-2507, Qwen3-30B-A3B-Instruct-2507,
Qwen3-Coder-30B-A3B / 480B-A35B, plus bge embeddings and qianfan-sug-8k. Remaining quota is shown per model in Model Square.
OpenAI-compatible at `https://qianfan.baidubce.com/v2`.

Source: <https://cloud.baidu.cn/doc/qianfan/s/Imi2rpirg>

*Checked Nov 20, 2026.*

---

## License

Apache 2.0
