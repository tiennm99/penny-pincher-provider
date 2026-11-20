# Coding-plan sections audit (Nov 20, 2026)

Scope: README sections "Claude AI Ecosystem" (AgentKit) and every entry under "Providers with Coding Plans", plus a
search for new coding-plan subscriptions. README.md was not modified. Every figure below was read on 2026-11-20 from
an official page, mostly with curl. I used raw HTML, docs markdown exports (`.md` / `llms.txt`), embedded doc state
(`MDContent`), public model-list APIs, or JS bundle defaults, and I name the fallback where one was used. Z.ai, BytePlus
and Volcengine were also rendered in a headless browser (agent-browser). Exceptions are named where they occur: the
Baidu and DeepSeek notes under "Checked and not recommended" come from search summaries, not official pages. Prices
that did not render even in the browser are marked UNVERIFIED.

Verdict key: **KEEP** means only the checked date changes. **UPDATE** means the block needs edits (replacement below).
**STALE-remove** means the plan no longer exists. **NEW** means a proposed addition.

## Verdict table

| Entry | Verdict | Reason |
|---|---|---|
| AgentKit | UPDATE | Now 7 runtimes (Grok added, Antigravity moved to preview). The $149 Bundle now includes the Desktop App (3 devices, 12 months). Skill/command counts are no longer published. The 20% buyer discount is now confirmed. |
| Z.ai | UPDATE | Prices, credits and models are unchanged. The supported-tool list grew (Codex, Pi, TRAE, Qoder, Droid, Hermes and more). For keys created from Oct 16, 2026, only a Coding Plan key draws plan quota. |
| MiniMax | UPDATE | Token Plan is closed to new buyers and replaced by **M Plan** (Go $22 / Explore $55 / Build $132). Text model is M3.1 Flash; H3 video only on Explore/Build. Referral terms page now 404s. |
| Kimi Code | UPDATE | New **Ultra ¥1,399** tier; annual billing now saves up to ¥3,360. New K3.1 Pro / K3.1 Pro Highspeed models. Pay-as-you-go **Extra Usage** added. |
| Alibaba Token Plan | UPDATE | Quotas raised Nov 9: Lite $6 / 20k, Essential $10 / 45k, Standard $18 / 80k, Pro **$43** / 200k Credits. New-user $3/$5 offer ends Nov 30, 2026. Team top seat now $180. Qwen4 Max added. |
| Alibaba Coding Plan | UPDATE | Still $50 Pro with the same limits and daily restock. Model list trimmed to 6. The page no longer points to Token Plan. |
| Alibaba referral blockquote | KEEP (flagged) | "$1,700" is still not on the campaign page, as the Sep 29 audit already found. Kept verbatim; alternative wording is in unresolved question 1. |
| opencode Go | UPDATE | New **Go Teams $20/member** (2-member minimum). Docs now give `https://opencode.ai/inference/go` base URLs (the old `/zen/go` path still answers). Model list changed to 32 models. |
| Synthetic | UPDATE | Packs replaced by 4 tiers (Go $9 / Standard $30 / Big $90 / Bigger $300). Weekly credit limit regenerates 2% every ~3.4 h. New model list. The live referral page says "up to $10 off first month". |
| BytePlus ModelArk | UPDATE | Prices and limits unchanged. Models trimmed (Kimi, GLM-5.1, GPT-OSS, Seed-Code gone). Referral still advertised on the live page, but its doc still says it ended Sep 30, 2026. |
| Volcengine Ark | UPDATE | The ¥40/¥200 figures are no longer on any Volcengine page I could read: UNVERIFIED. Pro limits are 6,000 / 45,000 / 90,000. New **Agent Plan**. Invite campaign doc ran May 19 to Nov 19, 2026. |
| Atlas Cloud | UPDATE | New Ultra $200 and Enterprise $500 tiers. Monthly cap alongside the weekly one. Pay-per-use packs. |
| NanoGPT | UPDATE | Still $12 / 60M input tokens/week. Adds 100 images/day and free output on included models; resets Monday 00:00 UTC. Model list refreshed. |
| Xiaomi MiMo | UPDATE | Prices unchanged. MiMo-V2.5 text models retired Oct 21, 2026. New mimo-v2.6-pro-ultraspeed on Pro/Max. The "$2 credits on signup" text is not in the current referral terms. |
| GitHub Copilot Pro | UPDATE | Prices and credits unchanged (1,000 base + 500 flex). Pro model list changed (Haiku 5.5, Gemini 4 Hydrogen, GPT-6.1 Terra and MAI Code added; GPT-5.4 moved to Pro+/Max). |
| StepFun Step Plan | NEW | Official credit-based plan, $6.99 to $99/month. Anthropic-compatible endpoint for Claude Code. |
| Tencent Cloud Token Plan (international) | NEW | USD plan on tencentcloud.com: $7 / $17 / $51 / $103 per month. Claude Code, Cursor, Cline and Codex supported. Overlaps the mainland TokenHub entry in Free Providers. |

No entry is STALE-remove: every plan is still sold.

---

## AgentKit — UPDATE

```markdown
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
```

What changed:
- The homepage now says "7 runtimes today: Claude Code, Codex, Cursor, Pi, Oh My Pi, DeepSeek Harness, Grok" and "In preview: Antigravity, OpenCode, and GitHub Copilot".
  - Certified on macOS, Windows and Linux: Claude Code, Pi, Oh My Pi and DeepSeek Harness.
  - Codex is certified on some operating systems only.
  - Cursor and Grok are shipped but not yet certified.
- The Bundle is now "Engineer + Marketing + Desktop", with the Desktop App for 3 devices for 12 months.
- The Desktop App is listed as "Native macOS, Windows and Linux apps".
- I dropped the "108+ skills, 95+ commands, 45 subagents" counts, because the homepage no longer states any counts.
- The kit descriptions now follow the homepage text ("skills and slash commands"; Marketing "For research, content and growth", with commands such as `/ak-marketing-research` and `/ak-competit…`). The page text I extracted no longer mentions subagents, SEO or copywriting.
- The referral program page says "Friends who buy through it save 20%". This settles the open question from the last audit, and the blockquote stays as it is.

Sources: https://agentkit.best/, https://agentkit.best/referral-program

## Z.ai — UPDATE

```markdown
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
Roo Code, Crush, Goose, OpenClaw, Hermes Agent, and more (ZCode and AutoClaw at 1.5× usage).

> Referral: <https://z.ai/subscribe?ic=PLKIAYEIPW>

*Checked Nov 20, 2026.*
```

What changed:
- Tool list updated from the official supported-tools page. ZCode and AutoClaw are marked "(1.5× Usage)".
- The Oct 16, 2026 key-separation notice was added. Keys created before that date keep working as "Compatible" keys.
- Prices are unchanged.
  - The `codePlansV3` defaults in the subscribe page's JS bundle give 18 / 80 / 168, quarterly −20%, yearly −30%.
  - The page rendered in agent-browser shows the same list prices ($18 / $80 / $168 struck through next to the yearly-discounted $12.6 / $56 / $117.6), with "10,000 Credits / week" on Lite and "6×" / "14× Lite usage" on Pro / Max.
- The bundle also carries a "50% off 1st Month" tag on each tier, but the rendered page shows no such tag, so it is left out.
- The invite terms (10% off the friend's first order) are still documented.

Sources: https://docs.z.ai/devpack/overview.md, https://docs.z.ai/devpack/quick-start.md,
https://docs.z.ai/devpack/tool/others.md, https://docs.z.ai/devpack/notice/api-key-management.md,
https://docs.z.ai/devpack/credit-campaign-rules.md, https://z.ai/subscribe (JS chunk defaults)

## MiniMax — UPDATE

```markdown
### [MiniMax](https://www.minimax.io/m-plan)

**M Plan** (replaced Token Plan for new buyers) — one shared quota with 5-hour and weekly windows (image and video only
the weekly window). **Go $22 / Explore $55 / Build $132 per month**; usage 1× / 3× / 7.5× of Go. Annual billing:
pay 10 months, get 2 free.

All tiers: MiniMax M3.1 Flash text, H3 Image, speech, web search, and image understanding; Explore and Build add H3
video. Overflow draws from purchased Credits (valid one year). Separate M Plan API key; OpenAI- and Anthropic-compatible
(`https://api.minimax.io/anthropic`). Tools: MiniMax Code, Claude Code, Codex, Cursor, OpenCode, Pi, Hermes Agent,
OpenClaw.

> Referral (10% off) — **For Referred Users:** 10% off subscription + become a dev ambassador. **For Referrers:** 10% back in API voucher per paid referral, usable across all MiniMax models, plus priority access to events and model previews. [View details](https://platform.minimax.io/subscribe/token-plan?code=CAQ5sxHAq6&source=link)

*Checked Nov 20, 2026.*
```

What changed:
- The "Token Plan updates" page says that "With the launch of M Plan, Token Plan is no longer available for new purchases". Existing Token Plan subscribers keep their price.
- Tier names changed: Plus, Max and Ultra became Go, Explore and Build. The regular prices of $22, $55 and $132 come from the "Monthly offer" page.
- The 50% first-month launch offer "ended on October 14, 2026", so it is left out.
- The "N agents" descriptions are gone. Tiers are now described as 1× / 3× / 7.5× of Go.
- The FAQ says "with annual billing, you pay for 10 months and get 2 months free".
- The homepage link now points to the M Plan page.
- **Blockquote kept verbatim, but flagged:**
  - The referral link now redirects to `https://www.minimax.io/m-plan?code=CAQ5sxHAq6&source=link`.
  - The page's strings still include "Scan the QR code to get 10% off your subscription!" and "Applies to all M Plan packages".
  - Its terms link (`platform.minimax.io/docs/token-plan/promotion`) now returns 404.
  - So the referrer-side "10% back in API voucher" is UNVERIFIED.

Sources: https://platform.minimax.io/docs/m-plan/intro.md, https://platform.minimax.io/docs/m-plan/faq.md,
https://platform.minimax.io/docs/m-plan/token-plan-notice.md, https://platform.minimax.io/docs/m-plan/monthly-offer.md,
https://platform.minimax.io/docs/m-plan/quickstart.md, https://www.minimax.io/m-plan

## Kimi Code — UPDATE

```markdown
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
```

What changed:
- The help center lists "Go, Plus, Pro, Max, and Ultra", with Ultra at ¥1,399/month or ¥13,428/year, and says "Save up to ¥3,360/year with annual billing". The prices were captured on October 19, 2026.
- The model page lists six IDs, including the new `k3.1-pro` and `k3.1-pro-highspeed`.
- Extra Usage terms: subscribers only, minimum ¥25 per top-up, the balance does not expire, and it is shared with Kimi web.
- The blockquote was kept verbatim. The invite link still resolves to `kimi-bot.com/activities/invite/share?...`, but its reward values render only through JS (UNVERIFIED).

Sources: https://www.kimi.com/code/docs/en/kimi-code/membership.html,
https://www.kimi.com/code/docs/en/kimi-code/models.html, https://www.kimi.com/en/help/membership/membership-pricing

## Alibaba Cloud Model Studio — UPDATE (Token Plan, Coding Plan; referral kept)

```markdown
### Alibaba Cloud Model Studio

> Referral: Up to **$1,700** in free trial credits via <https://www.alibabacloud.com/campaign/benefits?referral_code=A92LU5> (code: `A92LU5`).

#### [Token Plan](https://www.alibabacloud.com/help/en/model-studio/token-plan-overview)

Credit-based subscription (Singapore region only), monthly quota, no weekly cap. Tools: Claude Code, Cursor, Codex,
Qwen Code, Qoder, OpenClaw, Hermes Agent, TRAE, DeepSeek Harness.

**Personal Edition** (quotas raised Nov 9, 2026):
- Lite: **$6/month** — 20,000 Credits (new users **$3** first month until Nov 30, 2026)
- Essential: **$10/month** — 45,000 Credits (new users **$5** first month until Nov 30, 2026)
- Standard: **$18/month** — 80,000 Credits
- Pro: **$43/month** — 200,000 Credits
- Yearly: $65 / $100 / $195 / $490
- Extra bundle: $15 — 20,000 Credits (up to 5, needs an active plan)

**Team Edition** (per seat, no training on your data):
- Standard: **$20/seat/month** (list $30) — 25,000 Credits
- Advanced: **$75/seat/month** (list $100) — 100,000 Credits
- Premium: **$180/seat/month** (list $200) — 250,000 Credits
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
```

What changed:
- **Referral blockquote kept verbatim.**
  - The campaign page still does not show "$1,700". The Sep 29 audit found the same, and the line was kept then.
  - The page now leads with "Unlock Up to $150K in Credits for Your AI + Cloud Workloads. Start with $200 instantly — no minimum spend."
  - Possible wording is in unresolved question 1.
- **Token Plan:**
  - Personal prices and quotas come from the Personal Edition doc (updated Nov 16, 2026). The new-user price "is available until 23:59:59 on November 30, 2026 (UTC+8)".
  - Yearly prices come from the campaign page's plan cards.
  - Pro dropped from $68 to $43 in the Nov 9 price reduction.
  - The previous "list $8 / $16 / $25 / $80" comparison prices are gone.
  - Team seats are named Standard / Advanced / Premium in the docs. The campaign page calls them Standard / Pro / Max Seat.
  - Short-lived promos are left out: the qwen4-max-preview runs until Nov 25, and there are night discounts.
- **Coding Plan:**
  - qwen3-max-2026-01-23, qwen3-coder-next, qwen3-coder-plus and glm-4.7 are removed. The page says "Only the following exact model versions are supported".
  - The "Alibaba now recommends Token Plan" sentence is dropped, because the current Coding Plan page no longer says it.

Sources: https://www.alibabacloud.com/help/en/model-studio/token-plan-overview,
https://www.alibabacloud.com/help/en/model-studio/token-plan-personal-overview,
https://www.alibabacloud.com/help/en/model-studio/token-plan-team-overview,
https://www.alibabacloud.com/help/en/model-studio/coding-plan,
https://www.alibabacloud.com/campaign/benefits?referral_code=A92LU5

## opencode — Go — UPDATE

```markdown
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
```

What changed:
- New Go Teams tier. The docs say "$20/member/month, 2-member minimum … $5/month higher than Go on every model".
- The docs now give `https://opencode.ai/inference/go` as the base. The models API lists per-protocol base URLs (`.../anthropic/v1`, `.../openai/v1`, `.../google/v1beta`).
  - The old `https://opencode.ai/zen/go/v1/messages` still answers: an empty POST returns a Go `MissingSessionID` error, not a 404.
  - So the block gives the new URLs without claiming the old ones are dead.
- The model list comes from the live `https://opencode.ai/inference/go/v1/models` endpoint plus the landing-page table ("32 models").
  - Added: Kimi K3.1 Pro, MiniMax M3.1 Flash, Qwen4 Max, Hy4, Step 5 Preview, Claude Haiku 5.5, Gemini 4 Argon, and Muse Spark contributor models (which train on data and are off by default).
  - Gone: Kimi K2.6, MiniMax M2.7, DeepSeek V4 Flash, MiMo-V2.5, Grok 4.6.
- The GLM-5.3 request example was replaced. Its current figure (6,600 per 5 h) is a temporary boost that applies "through November 22, 2026".
- The "Gemini 4 Argon 50% discount through Nov 30" promo is left out because it expires.
- The referral program stays ended. There is no blockquote.

Sources: https://opencode.ai/docs/go/, https://opencode.ai/go, https://opencode.ai/inference/go/v1/models

## Synthetic — UPDATE

```markdown
### [Synthetic](https://synthetic.new/)

Privacy-first inference ("we never train on your data, and we never store API prompts or completions"). Plans:
**Go $9**, **Standard $30**, **Big $90**, **Bigger $300** per month. One weekly credit limit (no 5-hour or monthly
caps) that regenerates 2% every ~3.4 h; models draw credits at discounted rates, and extra usage bills at API pricing.
Fast mode (2× speed, 2× credits) and Infinite mode (slow, never counts against the limit; DeepSeek V4.1 Flash only).

Models: Kimi-K3.1-Pro, GLM-5.3 (beta), GLM-5.3-Flash, GLM-4.7-Flash, DeepSeek-V4.1-Flash-1017, Qwen3.8-27B,
gpt-oss-120b.
OpenAI-compatible (`https://api.synthetic.new/openai/v1`) and Anthropic-compatible
(`https://api.synthetic.new/anthropic/v1`) — guides for Claude Code, Crush, OpenCode, GitHub Copilot, OpenClaw,
Xcode, Octofriend.

> Referral: up to **$10.00 off** your first month via <https://synthetic.new/?referral=CNBFyw28zF0dZoj>

*Checked Nov 20, 2026.*
```

What changed:
- The "$30 per pack, 500 req/5 h, 1 concurrent request" model is gone. The site now has four tiers with a single weekly credit limit, per the pricing and rate-limits pages.
- The model list comes from the model pricing page. Kimi-K3, DeepSeek-V4.1-Flash, Nemotron-3-Super and nomic embeddings are no longer listed there.
- The guides list dropped Roo and KiloCode.
- Fast mode and Infinite mode are labelled "Beta". The pricing page says both are included on Big and Bigger, and also shows them on Go and Standard. That tier mapping is ambiguous, so the block does not tie the modes to tiers.
- **Blockquote differs from the live referral page:** the page now says "You've been referred! Subscribe today and get up to $10.00 off your first month!". I have no record of the earlier page text, so I cannot say when it changed. The replacement quotes the live page.

Sources: https://synthetic.new/pricing, https://synthetic.new/rate-limits, https://synthetic.new/pricing/models,
https://dev.synthetic.new/docs/api/overview, https://synthetic.new/?referral=CNBFyw28zF0dZoj

## BytePlus ModelArk — Coding Plan — UPDATE

```markdown
### [BytePlus ModelArk — Coding Plan](https://www.byteplus.com/en/activity/codingplan)

ByteDance. Lite: **$10/month** ($30/quarter), Pro: **$50/month** ($150/quarter). New-user first-purchase promo
($5/$25) suspended since Mar 17, 2026.
Limits: Lite ~1,900 req/5 h, ~12,000/week, ~24,000/month; Pro 5× Lite (~9,500 / ~60,000 / ~120,000). Coding tools only,
not for raw API calls.

Models: Auto, Dola-Seed-2.0-Pro/Lite/Code, GLM-5.2, GLM-5.3-Flash, DeepSeek-V4.1-Flash, DeepSeek-V4-Pro/Flash
(GLM and DeepSeek models with 1M context).
Endpoints: OpenAI `https://ark.ap-southeast.bytepluses.com/api/coding/v3`, Anthropic `.../api/coding`.
Tools: Claude Code, Cursor, Cline, Codex, Roo Code, Kilo Code, OpenCode, OpenClaw, TraeCode, Hermes Agent.

> Referral: <https://www.byteplus.com/activity/codingplan?ac=MMAUCIS9NT1S&rc=2739UWRE> — friends get 10% off their first
> subscription; referrers earn a 10% voucher per order, uncapped.

*Checked Nov 20, 2026.*
```

What changed:
- Prices and limits are unchanged.
- The model table in the subscription overview now lists Auto, Dola-Seed-2.0-Pro/Lite/Code, GLM-5.2, GLM-5.3-Flash, DeepSeek-V4-Flash, DeepSeek-V4-Pro and DeepSeek-V4.1-Flash.
  - Dropped: ByteDance-Seed-Code, GLM-5.1, Kimi-K2.5 and GPT-OSS-120b.
  - The activity page headline reads "now with GLM-5.3-Flash and DeepSeek-V4 Series".
- **Blockquote changed at the source:**
  - The old text said the campaign "is scheduled to end Sep 30, 2026". That date has passed.
  - The live activity page still says "Earn a 10% voucher for every friend's order uncapped. Your friends get 10% off their first subscription", with no end date.
  - The referral-campaign doc (2165246) still states "Campaign period 2026.01.13 - 2026.09.30". So whether new referrals still earn rewards is UNVERIFIED.
  - The replacement drops the past date and quotes the live page.
- The live price widget shows "Loading pricing…" even when rendered in agent-browser. The $10 / $50 table comes from doc 1928265, under an "Offer period 2026.01.13-2026.07.13" heading. The same doc's Mar 17 notice says both new and existing users pay "the standard list price", so the $10 / $50 figures are read as list prices; the live widget could not confirm them.

Sources: https://docs.byteplus.com/en/docs/ModelArk/1925114 (embedded `MDContent`),
https://docs.byteplus.com/en/docs/modelark/1928265, https://docs.byteplus.com/en/docs/modelark/2165246,
https://www.byteplus.com/en/activity/codingplan

## Volcengine Ark — Coding Plan — UPDATE

```markdown
### [Volcengine Ark — Coding Plan](https://www.volcengine.com/activity/codingplan)

ByteDance's mainland-China sibling of the BytePlus plan (火山引擎方舟 Coding Plan), billed in CNY. Lite and Pro tiers
(monthly, quarterly, yearly); current prices render only with JavaScript. Lite ~1,200 req/5 h, ~9,000/week,
~18,000/month; Pro ~6,000 / ~45,000 / ~90,000. Coding tools only.

Models: DeepSeek-V4.1-Flash-1017, GLM-5.3 series, Doubao-Seed-Evolving, Kimi-K3.1-pro, and more (Doubao Seed 2.0,
MiniMax, Kimi, DeepSeek series), or Auto. Tools: Claude Code, Codex CLI, Cursor, TRAE, OpenCode, OpenClaw, Hermes Agent.
A separate **Agent Plan** (Small / Medium / Large / Max, "限时 9.9 元起") adds multimodal models and web-search harness.

Source: <https://www.volcengine.com/activity/codingplan>, <https://www.volcengine.com/docs/82379/2165245>

*Checked Nov 20, 2026.*
```

What changed:
- **Prices:** ¥40 and ¥200 no longer appear in Volcengine article 37898 or in any doc I could read. The widget shows "价格查询中…" (still loading) both in raw HTML and after rendering in agent-browser, probably because it needs a login.
  - A Volcengine FAQ example mentions a friend paying "9.9元" for a Lite monthly plan. That looks like a first-purchase price, but the current list price is UNVERIFIED, so the block names no CNY figure.
- **Limits:** Pro is now stated explicitly as ~6,000 / ~45,000 / ~90,000 in doc 2165245, measured on Doubao Seed 2.0 Lite in Claude Code.
- **Models:** updated from the activity page (now Kimi-K3.1-pro).
- **Agent Plan:** this new product now carries the "限时 9.9 元起" banner.
- **Invite program:** a 5% voucher for the referrer and 9.5折 for the friend. The program doc (2479140) gives the period as "2026.05.19 - 2026.11.19", which ended yesterday. The activity page still shows the invite block, so the sentence was dropped as uncertain.

Sources: https://www.volcengine.com/activity/codingplan, https://www.volcengine.com/docs/82379/1925114,
https://www.volcengine.com/docs/82379/2165245, https://www.volcengine.com/docs/82379/2479140,
https://www.volcengine.com/article/37898

## Atlas Cloud — Coding Plan — UPDATE

```markdown
### [Atlas Cloud — Coding Plan](https://www.atlascloud.ai/coding-plan)

Third-party aggregator plan with **full API access** (rare among coding plans). Starter **$10**, Lite **$20**, Plus **$50**,
Max **$100**, Ultra **$200**, Enterprise **$500** per month — 16.5M / 33M / 82.5M / 165M / 330M / 825M points per week,
plus a monthly cap (whichever hits first; weekly resets Monday 00:00 UTC). Pay-per-use packs: $99 / $299 / $599
(280M / 850M / 1,700M points, valid 90 days).

Models: 18 LLMs incl. DeepSeek V4.1 Flash / V4 Pro, GLM-5.3-Flash / 5.2, Kimi K2.7 Code, Qwen3.8 Max, Doubao Seed 2.1,
MiniMax M2.5. Tools: Claude Code, Codex, Cursor, OpenClaw (20+ supported).

Source: <https://www.atlascloud.ai/coding-plan>

*Checked Nov 20, 2026.*
```

What changed:
- New Ultra ($200, 330M/week) and Enterprise ($500, 825M/week) tiers.
- The plan page now describes a "dual-limit system (e.g. 120M / month and 60M / week)". It does not publish the per-tier monthly totals, so none are quoted.
- Pay-per-use packs were added.
- The model multiplier table lists 18 models.
- A site banner reads "35% off — ends Nov 30". It does not say it applies to the Coding Plan, so it is left out.

Source: https://www.atlascloud.ai/coding-plan

## NanoGPT — UPDATE

```markdown
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
```

What changed:
- The 100 images/day allowance, free output, Monday reset and the "not included" list come from the pricing page.
- The model list was checked against the live `https://nano-gpt.com/api/subscription/v1/models` (280 IDs). The list now includes MiniMax M3.1 Flash, DeepSeek V4.1 Flash, MiMo-V2.6 and Qwen3.8 Flash.
- MiMo-V2.5 IDs are still served there, but the block now names V2.6.

Sources: https://nano-gpt.com/pricing, https://nano-gpt.com/api/subscription/v1/models,
https://docs.nano-gpt.com/api-reference/endpoint/subscription-usage

## Xiaomi MiMo Open Platform — UPDATE

```markdown
### [Xiaomi MiMo Open Platform](https://platform.xiaomimimo.com)

Refer & earn (long-term, no end date): new accounts (≤ 3 days old) that redeem my code get **10% off** their first
Token Plan order (within 30 days of binding); the inviter gets 10% back in API credits, valid 40 days.

**Token Plan** (monthly): Lite $6 / ¥39 (4.1B credits), Standard $16 / ¥99 (11B), Pro $50 / ¥329 (38B),
Max $100 / ¥659 (82B). Annual plans 12% off; 12% off first Individual purchase; 0.8× consumption 00:00–08:00
Beijing time. Team Edition from $16/seat. Models: mimo-v2.6-pro, mimo-v2.6-flash, ASR/TTS (TTS free for a limited
time); Pro and Max add mimo-v2.6-pro-ultraspeed. Works with OpenCode, OpenClaw, Claude Code.

> Referral: Code `T8ESAY` · <https://platform.xiaomimimo.com?ref=T8ESAY>

*Checked Nov 20, 2026.*
```

What changed:
- **Intro paragraph:**
  - The old intro was first-person promo text ("instantly get $2 in API credits … valid 40 days").
  - The current Refer & earn terms describe something else: 10% off the friend's first Token Plan order, and 10% back to the inviter in credits valid 40 days. Credits cannot be used to buy a Token Plan.
  - I found no "$2 on signup" in any current MiMo doc, so the paragraph is replaced. It is prose, not a blockquote.
  - The blockquote is unchanged.
- **Retired models:** the deprecation page lists mimo-v2.5-pro and mimo-v2.5 as deprecated at "10:00, October 21, 2026 (UTC+8)", replaced by mimo-v2.6-pro / -flash. The block no longer mentions V2.5.
- **ultraspeed:** the Token Plan doc (updated Nov 19, 2026) says "Pro and Max also support mimo-v2.6-pro-ultraspeed".
- **Prices:** unchanged.

Sources: https://mimo.mi.com/docs/en-US/price/token-plan, https://mimo.mi.com/static/docs/quick-start/promotions/refer.md,
https://mimo.mi.com/static/docs/updates/deprecate.md, https://mimo.mi.com/llms.txt

## GitHub Copilot Pro — UPDATE

```markdown
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
```

What changed:
- **Model list only**, taken from the plans doc's model matrix (Pro column):
  - Added: Claude Haiku 5.5, GPT-5.3-Codex, GPT-6.1 Terra, Gemini 4 Hydrogen, and MAI Code models (MAI-Code-1.1-Flash, MAI Code 2, MAI Code 2 Flash).
  - GPT-5.4 is now only GPT-5.4 nano, and only on Pro+/Max.
- **Unchanged:** prices, credits (Pro 1,000 + 500, Pro+ 3,900 + 3,100, Max 10,000 + 10,000), the free tier's 2,000 completions, and free Pro for teachers and maintainers.

Sources: https://docs.github.com/en/copilot/get-started/plans (via `docs.github.com/api/article/body`),
https://docs.github.com/en/copilot/concepts/billing-and-usage/individuals/billing,
https://docs.github.com/en/copilot/how-tos/manage-your-account/get-free-access-to-copilot-pro

---

## Proposed additions (ranked)

I found no reputable coding plan that launched in Sep–Nov 2026. Both proposals below are older plans that the README
does not list yet. Neither name appears in README history (`git log -i -G 'stepfun|step plan'` is empty), and
Tencent's existing README entry covers only the mainland CNY plan.

### 1. StepFun Step Plan — NEW

The best fit for this list. It has an official English docs page with prices and allowances, an Anthropic endpoint for
Claude Code, a $6.99 entry tier, and no 5-hour or weekly windows.

```markdown
### [StepFun — Step Plan](https://platform.stepfun.ai/step-plan)

Credit-based monthly allowance (since Jul 24, 2026; ~$1 ≈ 7M Credits), no 5-hour or weekly windows. **Flash Mini
$6.99** (400M Credits), **Flash Plus $9.99** (1,600M), **Flash Pro $29** (8,000M), **Flash Max $99** (40,000M) per
month; quarterly and yearly prepay cheaper. Booster packs $6.99 / 400M and $9.99 / 1,600M (30-day validity).

Models: step-5-preview, step-3.7-flash, step-3.5-flash, step-3.5-flash-2603, plus StepAudio 2.5 TTS/ASR.
Endpoints: Anthropic `https://api.stepfun.ai/step_plan` (Claude Code), OpenAI `https://api.stepfun.ai/step_plan/v1`.
Tools: Claude Code, Cursor, Trae, OpenClaw, and others. Pay by Stripe or account balance.

Source: <https://platform.stepfun.ai/docs/en/step-plan/overview.md>

*Checked Nov 20, 2026.*
```

Sources: https://platform.stepfun.ai/docs/en/step-plan/overview.md,
https://platform.stepfun.ai/docs/en/step-plan/upgrade-notice.md, https://platform.stepfun.ai/step-plan

Caveat: StepFun's own models only. The plan was relaunched on Jul 24, 2026, not in Sep–Nov, but it is not in the README
yet.

### 2. Tencent Cloud Token Plan (international, USD) — NEW

```markdown
### [Tencent Cloud — Token Plan](https://www.tencentcloud.com/document/product/1300/81315)

International (Singapore region) Personal Edition of Tencent's TokenHub plan, credit-based monthly quota. **Lite $7**
(1,000 credits), **Standard $17** (2,600), **Pro $51** (7,900), **Max $103** (15,900) per month; one plan per account.
Coding tools only (no scripted API use).

Models: Hy4, Hy4 flash, GLM-5.3-Flash, GLM-5.2, Kimi K3, Kimi-K2.6, DeepSeek-V4.1-Flash-1017, DeepSeek-V4-Pro/Flash,
MiniMax-M3, MiMo-V2.6-Flash, Auto.
Endpoints: OpenAI `https://tokenhub-intl.tencentcloudmaas.com/plan/v3`, Anthropic
`https://tokenhub-intl.tencentcloudmaas.com/plan/anthropic` (dedicated `sk-tp-` key).
Tools: Claude Code, Cursor, Cline, Codex CLI, OpenCode, Kilo Code, OpenClaw.

Source: <https://www.tencentcloud.com/document/product/1300/81315>

*Checked Nov 20, 2026.*
```

Sources: https://www-sg.tencentcloud.com/document/product/1300/81315 (last updated 2026-11-16),
https://www-sg.tencentcloud.com/document/product/1300/81471

Caveats:
- It overlaps the mainland "Tencent TokenHub" entry under Free Providers, which lists the CNY Token Plan. Folding the USD tiers into that entry would avoid two Tencent blocks. That is the maintainer's call.
- The launch date is not stated on the page.
- Hy4 preview is listed as "to be discontinued on 2026-12-07", so it is left out.

### Checked and not recommended

- **Cerebras Code** (Pro $50, Max $200, GLM-4.7): both tiers still show "sold out" on https://www.cerebras.ai/code.
- **DeepSeek:** still no official coding subscription. Search results show third-party resellers only.
- **Baidu Qianfan Coding Plan:** media reports say renewals stopped in June 2026 and the plan was replaced by a pay-as-you-go Token Plan. I did not verify this on an official page.
- **Huawei Cloud Token Plan:** surfaced in search, but `huaweicloud.com/agentorchard/tokenplan.html` returns 404. No official page was verified.

---

## Limitations

- **Prices that never rendered:** Volcengine (not found) and BytePlus (taken from the docs) still showed loading placeholders in agent-browser. Z.ai rendered fine.
- **Purchases not tested:** I did not buy or log in anywhere, so stock (Alibaba Coding Plan) and referral payouts are untested.
- **Narrow new-plan search:** the search was limited to a handful of web queries plus official pages for the candidates found. Western providers (Mistral, Together, Groq, Fireworks) were not re-checked for new subscription products.
- **Model names:** recorded exactly as the vendor pages print them. None were checked against model cards.

## Unresolved questions

1. **Alibaba referral blockquote:** "$1,700" is still not on the campaign page. It could become: `> Referral: Up to **$150K** in credits, starting with **$200** instantly (no minimum spend) via <link> (code: A92LU5).` That $200 needs an approved business use case ("Receive $200 instantly if approved"), so it may not suit individual readers.
2. **MiniMax referral:**
   - The blockquote link redirects to the M Plan page, and the terms page now 404s.
   - Keep the blockquote verbatim, or drop the referrer-side "10% back" claim until MiniMax republishes terms?
3. **BytePlus and Volcengine referrals:** both live pages still advertise invites, but their campaign docs show end dates that have passed (Sep 30 and Nov 19, 2026). Re-check later, or remove the invite text?
4. **Volcengine CNY prices:** no current list price was found, even with a rendered page (the widget likely needs a login). Keep the entry without prices?
5. **Tencent:** add the international USD plan as its own coding-plan entry, or fold it into the existing Free Providers TokenHub entry?

Status: DONE_WITH_CONCERNS
Summary: Of the 13 coding-plan entries plus AgentKit, every one needs an update (the biggest changes are MiniMax's move to M Plan, Synthetic's new tiers, Alibaba's price cut, opencode Go Teams and its new endpoints, and AgentKit's Bundle). None are stale. Two additions are proposed: StepFun Step Plan and Tencent Cloud's international Token Plan.
Concerns/Blockers: Volcengine prices did not render even in a headless browser, and BytePlus prices rest on its docs. Referral terms for MiniMax, BytePlus and Volcengine are uncertain. The proposed Synthetic and BytePlus blockquote edits need the user's sign-off, and so does any change to the Alibaba $1,700 line, which is kept verbatim.
