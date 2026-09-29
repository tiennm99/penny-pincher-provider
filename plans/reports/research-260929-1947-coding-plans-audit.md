# Coding-plan sections audit (Sep 29, 2026)

Scope: README sections "Claude Code Guest Passes", "Claude AI Ecosystem" (AgentKit), and every entry under
"Providers with Coding Plans". README.md was not modified. Every claim below was checked against a live page on
2026-09-29 using curl or WebFetch; no browser was used. Where a price only loads through JavaScript, I name the
fallback source used, such as a docs markdown export, embedded page state, a JS bundle default, or a media report.

## Summary

| Entry | Status | Headline change |
|---|---|---|
| Claude Code Guest Passes | CURRENT | Program still live (`/passes`, Max-plan only). The user's own pass remains out of stock. |
| AgentKit | UPDATE | Desktop app now ships at $49/yr (1 device) or $99/yr (3 devices), no longer a waitlist. Runtime list changed. |
| Z.ai | UPDATE | Credit-based plans since Jul 30, 2026. Now $18 / $80 / $168. Models are now GLM-5.3 and GLM-5.3-Flash. |
| MiniMax | UPDATE | Now $22 / $55 / $132. Plus is 3-4 agents and Max is 4-5 agents. Usage-based deduction. The README's referral end date (Jul 1) has passed, but the program is still documented. |
| Kimi Code | UPDATE | Tiers renamed to Go / Plus / Pro / Max (¥49 / ¥99 / ¥199 / ¥699). The ¥49 Go tier has no Kimi Code. New K3 model. Weekly cap removed for new members. |
| Alibaba Token Plan | UPDATE | New Personal Edition (Lite $6 to Pro $68, promo prices). Team seats also discounted. Model list fully refreshed. |
| Alibaba Coding Plan | UPDATE | Still $50 Pro and still limited stock. Model list changed (qwen3.7-plus added). |
| opencode Go | UPDATE | $10 Go plus a new $40 Go Plus. **Referral program has ended.** The $5 first month is no longer shown. Dollar-based limits. |
| Synthetic | UPDATE | $30/mo per "pack", 500 req/5h. Model list changed. Now has an Anthropic endpoint. |
| BigModel.cn GLM Coding Plan | UPDATE | New prices ¥118 / ¥538 / ¥1,078 (from media reports). The ¥49 / ¥149 / ¥469 prices are now legacy-only. Models are GLM-5.3 and GLM-5.3-Flash. |
| BytePlus ModelArk | UPDATE | **README prices are wrong:** list price is $10 Lite and $50 Pro. **Referral campaign ends Sep 30, 2026.** |
| Xiaomi MiMo | UPDATE | USD prices are now listed ($6 / $16 / $50 / $100). Credit amounts changed (4.1B to 82B). Models are now MiMo-V2.6. |
| GitHub Copilot Pro | UPDATE | Premium requests replaced by GitHub AI Credits (Pro gets 1,500/mo). A new $100 Max tier. Pro+ now 7,000 credits. |

---

## Claude Code Guest Passes

**Status: CURRENT.** The program exists. The user's own link is still out of stock, and the README already says so.

Proposed block (unchanged apart from the rules text and the date):

```markdown
## Claude Code Guest Passes

One week of free Claude Pro (includes Claude Code). Eligible subscribers (currently Max plans) get three passes via
the `/passes` command in Claude Code. New users only; requires payment info but can be cancelled before the trial
ends.

**My passes:**

- ~~<https://claude.ai/referral/ZkoAngod1A>~~ — out of stock as of 2026-04-30

Have a spare pass? Open a PR adding your link, or open an issue.

*Checked Sep 29, 2026.*
```

What changed:
- Added how passes are issued. The official docs list `/passes` as "Share a free week of Claude Code with friends. Only visible if your account is eligible."
- The "Max plans only, three passes" detail comes from third-party guides, not from an Anthropic page.
- `claude.ai/referral/ZkoAngod1A` returns HTTP 403 to curl. That is a bot block, not proof the link is dead or alive, so the strikethrough stays.
- Added a checked-date line, which this section did not have before.

Sources:
- https://code.claude.com/docs/en/commands.md (official, the `/passes` row)
- https://madrobot.blog/2026/09/27/claude-referral-link-guest-passes-how-to-refer/ (third party, dated Sep 27, 2026)
- https://growsurf.com/blog/anthropic-claude-referral-program/ (third party)

## AgentKit

**Status: UPDATE.**

```markdown
### [AgentKit](https://agentkit.best/)

AgentKit (formerly **ClaudeKit**, `claudekit.cc`) sells production-ready kits of skills, slash
commands, subagents, and workflows for coding agents — native support for Claude Code, Codex, Antigravity, Pi, and
Oh My Pi; Cursor and DeepSeek Harness in beta; OpenCode, Grok, and GitHub Copilot in preview. **Engineer** ($99)
covers frontend, backend, database, DevOps, code review, and debugging; **Marketing** ($99) adds research, SEO,
competitor-intelligence, and copywriting agents; the bundle is **$149** (108+ skills, 95+ commands, 45 subagents).
The **AgentKit App** desktop cockpit (macOS/Windows) is sold separately at **$49/yr** (1 device) or **$99/yr**
(3 devices).

> Referral: **20% off** your first purchase via <https://agentkit.best/?ref=BWA910UK> (code: `BWA910UK`).

*Checked Sep 29, 2026.*
```

What changed:
- The desktop app is no longer on a waitlist. It is sold at $49/yr for one device or $99/yr for three devices.
- The runtime support list now has three levels: native, beta, and preview. GitHub Copilot is only at the "preview" level.
- Kit prices, skill counts, and command and subagent counts are unchanged.
- The referral program still exists. The leaderboard page shows referrer commission tiers from 20% to 40%.
- I could not verify the 20% buyer discount for `?ref=` links. The page shows a timer-based "30% special offer" banner, which may be separate from referrals.

Sources:
- https://agentkit.best/
- https://agentkit.best/leaderboard
- `https://claudekit.cc` now redirects to agentkit.best (checked with curl)

## Z.ai

**Status: UPDATE.** On Jul 30, 2026 the plans moved to a credit system. Legacy plans are no longer sold to new users.

```markdown
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
```

What changed:
- Plans are now credit-based. Prices rose from "$18+" to $18 / $80 / $168 per month. Quarterly costs are $43.20 / $192 / $403.20 and yearly $151.20 / $672 / $1,411.20.
- The model lineup changed from GLM-5.1 / 5-Turbo / 4.7 / 4.5-Air to GLM-5.3 and GLM-5.3-Flash.
- Plan quota may only be used in the supported tools.
- The invite program is still active: the invitee gets 10% off the first order, and the inviter gets 10% of that payment in credits once 3 friends have paid.
- A temporary promo runs to Oct 7: all-day off-peak rates, plus unlimited GLM-5.3-Flash overnight in ZCode and AutoClaw. It is left out of the block because it expires.
- Prices came from the defaults in the z.ai subscribe page's JS bundle (the `codePlansV3` table). Third-party guides report the same $18 / $80 / $168.

Sources:
- https://docs.z.ai/devpack/overview.md
- https://docs.z.ai/devpack/notice/usage-revision.md
- https://docs.z.ai/devpack/quick-start.md
- https://docs.z.ai/devpack/credit-campaign-rules.md
- https://z.ai/subscribe (JS chunk defaults)
- https://www.aipricing.guru/z-ai-subscription-pricing/ (third party)

## MiniMax

**Status: UPDATE.**

```markdown
### [MiniMax](https://platform.minimax.io)

Token Plan — usage-based deduction from one shared quota (5-hour rolling + weekly windows). $22–$132/month.

- Plus ($22): 3-4 agents
- Max ($55): 4-5 agents
- Ultra ($132): 6-7 agents

Covers the full MiniMax lineup (M3 / M2.7 / image / speech); MiniMax H3 video, voice design, and rapid voice
cloning are excluded. Top-up Credits: 1,000 credits = $1, valid 365 days.
OpenAI- and Anthropic-compatible. Tools: Claude Code, Codex, Cursor, TRAE, Hermes Agent, OpenClaw, Pi.

> Referral (10% off) until **Jul 1, 2026** — **For Referred Users:** 10% off subscription + become a dev ambassador. **For Referrers:** 10% back in API voucher per paid referral, usable across all MiniMax models, plus priority access to events and model previews. [View details](https://platform.minimax.io/subscribe/token-plan?code=CAQ5sxHAq6&source=link)

*Checked Sep 29, 2026.*
```

What changed:
- Prices changed from $20 / $50 / $120 to $22 / $55 / $132.
- Agent counts changed. Plus went from 4-5 to 3-4 agents and Max from 6-7 to 4-5 agents. Ultra is unchanged at 6-7.
- Quota changed from per-call counting to deduction based on actual usage.
- The model list changed. The official docs now list M3 / M2.7 / image / speech. Hailuo 2.3 and Music-2.6 are not mentioned, and H3 video is excluded.
- I found no official mention of a yearly "~17% off" discount, so it was dropped.
- The referral program is still documented in the official FAQ, with no end date given. The invitee gets 10% off (all plans and upgrades) and "Builder" status. The referrer gets credits worth 10% of the payment, valid 90 days.
- The README's "until Jul 1, 2026" date has passed, but the blockquote is kept verbatim as instructed. The user should decide whether to edit their own wording.

Sources:
- https://platform.minimax.io/docs/guides/pricing-token-plan.md
- https://platform.minimax.io/docs/token-plan/intro.md
- https://platform.minimax.io/docs/token-plan/faq.md
- https://platform.minimax.io/docs/llms.txt

## Kimi Code

**Status: UPDATE.**

```markdown
### [Kimi Code](https://www.kimi.com/code)

Moonshot's coding perk bundled with Kimi membership (desktop app, CLI, VS Code; Claude Code, OpenCode, Codex,
Hermes Agent via API key). New plans: Go ¥49 (no Kimi Code), **Plus ¥99**, **Pro ¥199**, **Max ¥699** per month;
annual billing saves up to ¥1,680. Rolling 5-hour window plus a monthly total (weekly cap removed for new members).

Models: `k3` (K3, up to 1M context on Pro+), `k3-256k`, `kimi-for-coding` (K2.8 Preview), `kimi-for-coding-highspeed`
(K2.7 Code, Pro+). OpenAI- and Anthropic-compatible (`https://api.kimi.ai/coding/`). Pay-as-you-go also at
`platform.moonshot.ai`.

> Referral (code: `C8CJ6F`) — sign up or subscribe via my link and we each get a guaranteed benefit, up to **1-Year Membership Credits**:
> - Sign up: <https://kimi-bot.com/activities/viral-referral/share?scenario=invite&from=share_poster&invitation_code=C8CJ6F>
> - Subscribe: <https://kimi-bot.com/activities/viral-referral/share?scenario=subscribe&from=share_poster&invitation_code=C8CJ6F>

*Checked Sep 29, 2026.*
```

What changed:
- The tier names Adagio / Andante / Presto are stale.
- Kimi renamed its tiers to Go / Plus / Pro / Max around Sep 18 and kept prices the same. The help center still shows the legacy names at those prices: Andante ¥49, Moderato ¥99, Allegretto ¥199, Allegro ¥699.
- For new members, the ¥49 Go tier does not include Kimi Code.
- The model lineup is new: K3, K2.8 Preview, and K2.7 Code HighSpeed.
- The weekly quota was removed for new members. The 5-hour window and a monthly total remain.
- Extra Usage top-ups are available (¥25 minimum).
- The referral link still resolves. It redirects to `kimi-bot.com/activities/invite/share?...`, which is titled "Kimi 登月同行计划 - 邀请好友赢好礼". The reward details render only with JavaScript and could not be verified.
- USD prices for the international site were not verified.

Sources:
- https://www.kimi.com/code/docs/en/kimi-code/membership.html
- https://www.kimi.com/code/docs/ (models and endpoints, Chinese)
- https://www.kimi.com/en/help/membership/membership-pricing
- https://www.kucoin.com/news/flash/kimi-launches-new-subscription-tiers-after-two-month-pause-kimi-code-not-sold-separately (media)
- https://codingplan.org/en/plans/kimi (third party)

## Alibaba Cloud Model Studio

### Token Plan

**Status: UPDATE.** A Personal Edition was added and Team prices changed. Both docs pages were last updated Sep 28, 2026.

```markdown
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
```

What changed:
- The Personal Edition is new.
- Team Standard and Pro now have limited-time prices of $20 and $75 (list $30 and $100). "Premium" is now called "Max".
- The model list was replaced. qwen3.6-plus, glm-5, and MiniMax-M2.5 are now Team-only.
- On the account referral: the campaign page still loads with the code (HTTP 200) and shows an "Invite & Earn Plan". I could not find the "$1,700" figure on the page, only "$90 ECS credits" and "free tokens". The blockquote is kept verbatim, and the amount is marked unverified.

### Coding Plan

**Status: UPDATE.** The product is still listed, the Pro tier is still sold in limited quantities, and Lite is discontinued.

```markdown
#### [Coding Plan](https://www.alibabacloud.com/help/en/model-studio/coding-plan)

Pro plan: **$50/month** — 6,000 req/5-hour, 45,000 req/week, 90,000 req/month.

Models: qwen3.7-plus, qwen3.6-plus, kimi-k2.5, glm-5, MiniMax-M2.5 (recommended); qwen3.5-plus, qwen3-max-2026-01-23,
qwen3-coder-next, qwen3-coder-plus, glm-4.7.
Endpoints: OpenAI `https://coding-intl.dashscope.aliyuncs.com/v1`, Anthropic `.../apps/anthropic`.
Tools: Claude Code, Cursor, Cline, Codex, OpenCode, Qwen Code, Qoder, Kilo CLI, OpenClaw, Hermes Agent, and more.
Lite closed to new subscribers (Mar 20, 2026) and to renewals/upgrades (Apr 13, 2026).

**Note:** limited slots, restocked daily at 00:00 UTC+8 (first come, first served); Alibaba now recommends Token Plan
instead. As of Jun 5, 2026 it was effectively unbuyable.

*Checked Sep 29, 2026.*
```

What changed:
- The model list changed. qwen3.7-plus and qwen3.6-plus are new and are the recommended models.
- Alibaba now officially confirms the stock limit ("limited-quantity offering and is no longer available once sold out").
- I could not test whether a purchase goes through, because that needs a logged-in console.

Sources:
- https://www.alibabacloud.com/help/en/model-studio/token-plan-overview
- https://www.alibabacloud.com/help/en/model-studio/token-plan-personal-overview
- https://www.alibabacloud.com/help/en/model-studio/token-plan-team-overview
- https://www.alibabacloud.com/help/en/model-studio/coding-plan
- https://www.alibabacloud.com/campaign/benefits?referral_code=A92LU5

## opencode — Go

**Status: UPDATE.** The referral program has ended.

```markdown
### [opencode — Go](https://opencode.ai/go)

OpenCode subscription for curated open models. **Go $10/month**, **Go Plus $40/month** (higher limits). Limits are
monthly dollar amounts per model (5-hour = 20%, weekly = 50% of the monthly limit); e.g. Go allows ~220 GLM-5.3 or
~3,200 MiniMax M3 requests per 5 h. Falls back to Zen balance when enabled.

Models: GLM-5.3/5.3-Flash/5.2, Kimi K3/K2.7 Code/K2.6, MiniMax M3/M2.7, Qwen3.8 Max/Flash, Qwen3.7 Plus,
DeepSeek V4.1 Flash/V4 Pro/V4 Flash, MiMo-V2.6(-Pro/-Flash)/V2.5(-Pro), LongCat-2.0, Hy4 preview, Hy3, Grok 4.7/4.6,
GPT 6 Luna/5.6 Luna, plus limited-time free models.
Endpoints: `https://opencode.ai/zen/go/v1/{chat/completions,messages,responses}`. Validated clients: Claude Code,
Codex, Hermes, ZCode, Pi, jcode, Kilo Code CLI. Model format: `opencode-go/<model-id>`.

My referral:

> Invite friends to OpenCode Go. Earn $5 when a friend subscribes, and they'll get $5 too. Share your referral link; your friend joins and subscribes to Go; you both get a $5 usage credit to apply toward your Go usage limits.
>
> Referral link: <https://opencode.ai/go?ref=HE42WGS8BM>

*Checked Sep 29, 2026.*
```

What changed:
- **The referral program has ended.** `opencode.ai/go?ref=HE42WGS8BM` shows a warning: "The referral program has ended. Referral links no longer earn credit for you or the person who shared them." The blockquote is kept verbatim as instructed, but the user will probably want to strike it through or remove it.
- The "$5 first month" offer is no longer on the Go page, so it was dropped.
- Go Plus ($40/month) is new.
- Limits changed from per-request counts ("200–10,200 req") to dollar budgets for each model.
- The model list grew a lot.
- Claude Code now works natively, because Go has an Anthropic `/messages` endpoint and recognises Claude Code's session header. The LiteLLM or `oc-go-cc` workaround is no longer needed.

Sources:
- https://opencode.ai/docs/go/
- https://opencode.ai/go
- https://opencode.ai/go?ref=HE42WGS8BM (referral-ended notice in the HTML)

## Synthetic

**Status: UPDATE.**

```markdown
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
```

What changed:
- The $30/month price is now explained as one "pack" with 500 requests per 5 hours.
- The model list changed. Kimi K2.6, MiniMax M2.5, and GLM 5.1 are gone. Kimi-K3, GLM-5.3-Flash, DeepSeek-V4.1-Flash, and Qwen3.8-27B are new.
- An Anthropic-compatible endpoint now exists.
- The referral still works. The referred landing page shows "Subscribe today and get $10.00 off your first month!" The README's wording ("subscription credit") is close enough and was kept verbatim.

Sources:
- https://synthetic.new/pricing
- https://dev.synthetic.new/docs/api/overview
- https://synthetic.new/?referral=CNBFyw28zF0dZoj

## BigModel.cn — GLM Coding Plan

**Status: UPDATE.** The plans changed on Jul 30, 2026, the same day as Z.ai's change.

```markdown
### [BigModel.cn — GLM Coding Plan](https://www.bigmodel.cn/glm-coding)

The Chinese (mainland) counterpart of Z.ai's GLM Coding Plan — same underlying Zhipu AI models, but billed in CNY through bigmodel.cn. Suited for users who can pay via Alipay / WeChat Pay or already have a 智谱 AI account.

Credit-based plans since Jul 30, 2026 (monthly list price): **Lite ¥118**, **Pro ¥538**, **Max ¥1,078**.
Credits per 5 h / per week: Lite 2,000 / 10,000 · Pro 12,000 / 60,000 · Max 28,000 / 140,000; off-peak usage
(outside Mon–Fri 14:00–18:00 UTC+8) costs 50% fewer credits. Legacy V1/V2 subscribers keep ¥49 / ¥149 / ¥469.

All tiers support GLM-5.3 and GLM-5.3-Flash (GLM-5.2/5.1 route to GLM-5.3; GLM-5-Turbo/4.7 route to GLM-5.3-Flash).
Anthropic endpoint `https://open.bigmodel.cn/api/anthropic`, OpenAI endpoint `https://open.bigmodel.cn/api/coding/paas/v4`.
Tools: Claude Code, Kilo Code, OpenClaw (lower priority), OpenCode, TRAE, CodeBuddy, and others on the supported list.

Referral program (challenge-based, resets every 30 invitees):
- Invited friend gets **5% off** their first GLM Coding Plan order.
- Referrer gets **10% cashback** once 3 friends subscribe, plus an **additional 10%** of the total paid amount for every 30 invitees.
- Rebate credit is usable for resource packs, API calls, and subscription renewals on the BigModel platform.

Source: <https://www.bigmodel.cn/glm-coding>, <https://docs.bigmodel.cn/cn/coding-plan/overview> [^bigmodel]

Homepage: <https://www.bigmodel.cn/glm-coding>

My referral:

>🚀 Join the GLM Coding Plan via my link — get 5% off your first order. Subscribe at https://www.bigmodel.cn/glm-coding?ic=VGRZKHKNKW (invitation code: `VGRZKHKNKW`).

[^bigmodel]: Checked on Sep 29, 2026
```

What changed:
- The ¥49 / ¥149 / ¥469 prices are now legacy-only. The official "老用户权益说明" notice lists them as the V2 prices that V1 and V2 holders keep.
- The new list prices, ¥118 / ¥538 / ¥1,078, come from Sina Finance and a Tencent Cloud developer article. IT之家 separately confirms "每月 118 元起". The official price page renders only with JavaScript, so I could not read it directly.
- The models changed to GLM-5.3 and GLM-5.3-Flash.
- The block keeps the entry's existing footnote style (`[^bigmodel]`) instead of `*Checked ...*` so its structure stays the same.
- I could not verify the referral terms on the current page. The README says 5% for the invitee, while Z.ai's version of the program gives 10%.

Sources:
- https://docs.bigmodel.cn/cn/coding-plan/overview.md
- https://docs.bigmodel.cn/cn/coding-plan/notice/usage-revision.md
- https://docs.bigmodel.cn/cn/coding-plan/quick-start.md
- https://finance.sina.com.cn/stock/t/2026-07-31/doc-iniksxpi1210399.shtml (media)
- https://cloud.tencent.com/developer/article/2718987 (media)
- https://www.ithome.com/0/983/934.htm (media)

## BytePlus ModelArk — Coding Plan

**Status: UPDATE.** The prices in the README are wrong, and the referral campaign ends tomorrow.

```markdown
### [BytePlus ModelArk — Coding Plan](https://www.byteplus.com/en/activity/codingplan)

ByteDance. Lite: **$10/month** ($30/quarter), Pro: **$50/month** ($150/quarter). New-user first-purchase promo
($5/$25) suspended since Mar 17, 2026.
Limits: Lite ~1,900 req/5 h, ~12,000/week, ~24,000/month; Pro 5× Lite (~9,500 / ~60,000 / ~120,000).

Models: Auto, Dola-Seed-2.0-Pro/Lite/Code, ByteDance-Seed-Code, GLM-5.3-Flash, GLM-5.2, GLM-5.1, Kimi-K2.5,
DeepSeek-V4.1-Flash, DeepSeek-V4-Pro/Flash, GPT-OSS-120b.
Endpoints: OpenAI `https://ark.ap-southeast.bytepluses.com/api/coding/v3`, Anthropic `.../api/coding`.
Tools: Claude Code, Cursor, Cline, Codex, Roo Code, Kilo Code, OpenCode, OpenClaw, TraeCode, Hermes Agent.

> Referral: <https://www.byteplus.com/activity/codingplan?ac=MMAUCIS9NT1S&rc=2739UWRE>

*Checked Sep 29, 2026.*
```

What changed:
- The prices were wrong. The README said $15 / $35, but the official list price is $10 / $50 per month.
- The README's promo note is also wrong. The first-purchase promo was $5 / $25 and was suspended on Mar 17, 2026, not "early 2026".
- Added the request quotas.
- The model list changed. ByteDance-Seed-2.0 is now listed as Dola-Seed-2.0, and GLM-5.3-Flash and DeepSeek-V4 are new.
- **The referral campaign runs from 2026-01-13 to 2026-09-30.** The invitee gets 10% off the first order, and the referrer gets a 10% voucher, valid 90 days. After tomorrow the user's link may stop giving a discount. Re-check on or after Oct 1.

Sources:
- https://docs.byteplus.com/en/docs/ModelArk/1925114 (subscription overview, updated Sep 28, 2026, read from embedded `MDContent`)
- https://docs.byteplus.com/en/docs/modelark/1928265 (offer notice and prices)
- https://docs.byteplus.com/en/docs/modelark/2165246 (referral campaign period)
- https://www.byteplus.com/en/activity/codingplan

## Xiaomi MiMo Open Platform

**Status: UPDATE.**

```markdown
### [Xiaomi MiMo Open Platform](https://platform.xiaomimimo.com)

I'm on Xiaomi MiMo Open Platform — running Xiaomi's flagship MiMo V2.5 and the rest of the lineup. Sign up with my code and you'll instantly get $2 in API credits.

After signup, enter the code at the bottom-left of the console. Credits valid 40 days.

**Token Plan** (monthly): Lite $6 / ¥39 (4.1B credits), Standard $16 / ¥99 (11B), Pro $50 / ¥329 (38B),
Max $100 / ¥659 (82B). Annual plans 12% off; 12% off first Individual purchase; 0.8× consumption 00:00–08:00
Beijing time. Team Edition from $16/seat. Models: mimo-v2.6-pro, mimo-v2.6-flash, ASR/TTS (mimo-v2.5 and
mimo-v2.5-pro retire Oct 21, 2026). Works with OpenCode, OpenClaw, Claude Code.

> Referral: Code `T8ESAY` · <https://platform.xiaomimimo.com?ref=T8ESAY>

*Checked Sep 29, 2026.*
```

What changed:
- USD prices are now published.
- Credit amounts changed from 60M / 200M / 700M / 1,600M to 4.1B / 11B / 38B / 82B. The CNY prices are unchanged.
- The models moved to MiMo-V2.6, and V2.5 retires on Oct 21, 2026.
- A Team Edition is new.
- The first paragraph is the user's own referral copy and was kept verbatim. It still says "MiMo V2.5", which the user may want to change to V2.6.
- The referral program still appears on the official site as an "Invite friends" page, but that page renders only with JavaScript. Search snippets of the official page say each side gets $2, the credits are valid 40 days, the invitee must have registered within 3 days, and there is 10% off the first plan within 30 days. I could not confirm this in the page body.
- Docs on `platform.xiaomimimo.com/docs/*` now redirect (302) to `mimo.mi.com`.

Sources:
- https://mimo.mi.com/docs/en-US/price/token-plan (updated Sep 21, 2026)
- https://mimo.mi.com/docs/en-US/promotions/refer
- https://platform.xiaomimimo.com

## GitHub Copilot Pro

**Status: UPDATE.** Premium requests were replaced by usage-based GitHub AI Credits.

```markdown
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
```

What changed:
- The allowance changed from "1,500 premium requests" to 1,500 AI credits, which are usage-based.
- Pro+ went from 6,000 premium requests to 7,000 AI credits.
- A new Max tier costs $100/month.
- The Free tier's "50 premium requests" became an unspecified AI-credit allowance.
- Claude Opus-class models are no longer on Pro.
- I could not verify the "$100/year" annual price on the current docs or plans page, so it was dropped. Add it back only if the user confirms it.

Sources:
- https://docs.github.com/en/copilot/get-started/plans (via `docs.github.com/api/article/body`)
- https://docs.github.com/en/copilot/concepts/billing-and-usage/individuals/billing
- https://github.com/features/copilot/plans

---

## Proposed additions

These are ranked by how well they fit this list: a cheap subscription that works in Claude Code or Cursor, with a
live official page.

1. **Volcengine Ark — Coding Plan (方舟 Coding Plan, mainland China)**
   - The official activity page is live. It lists Lite and Pro plans with models DeepSeek-V4.1-Flash, the GLM-5.3 series, Doubao-Seed-Evolving, Kimi-K3, and Kimi-K2.8-Preview. It supports Claude Code and Cursor, and advertises "限时 9.9 元起".
   - The invite terms are a 5% voucher for the referrer and 9.5折 (5% off) for the friend.
   - Volcengine's own marketing articles give ¥40/month for Lite and ¥200/month for Pro. Lite allows about 1,200 requests per 5 hours, 9,000 per week, and 18,000 per month. Pro is 5× Lite.
   - The live price widget renders only with JavaScript, so re-check prices before adding. It is the mainland sibling of BytePlus.
   - Sources: https://www.volcengine.com/activity/codingplan, https://www.volcengine.com/article/37898
2. **Atlas Cloud — Coding Plan**
   - A third-party aggregator with four tiers: Starter $10, Lite $20, Plus $50, and Max $100 per month. They give 16.5M, 33M, 82.5M, and 165M points per week.
   - It covers 18 LLMs, including DeepSeek, GLM, Kimi, and MiniMax, and works with Claude Code, Codex, Cursor, and OpenClaw.
   - It advertises "Full API access", which is rare for coding plans.
   - Source: https://www.atlascloud.ai/coding-plan
3. **Alibaba Token Plan Personal Edition**
   - Not a separate entry. It is already folded into the Alibaba block above. At $6/month it is now the cheapest Alibaba route.

Checked and not recommended:
- **Cerebras Code** (Pro $50, Max $200, GLM-4.7): both tiers show "sold out" on https://www.cerebras.ai/code.
- **DeepSeek**: has no official coding plan. Only a prepaid API exists (https://qcode.cc/en/deepseek-code-plan, third party).
- **Tencent Cloud Coding Plan**: exists according to third-party trackers, but `cloud.tencent.com/act/pro/codingplan` returns 404. I found no verified official URL.
- **Mistral, Together, NVIDIA**: I did not verify any coding-subscription product for them.

## Unresolved questions

1. **opencode Go referral**: the program has officially ended. Should the blockquote be struck through or removed? That is the user's decision.
2. **BytePlus referral**: it ends Sep 30, 2026. Re-check on Oct 1 whether BytePlus extends it.
3. **MiniMax referral**: the "until Jul 1, 2026" text in the user's blockquote is stale, but the program is still documented. Should the user reword it?
4. **BigModel.cn prices** (¥118 / ¥538 / ¥1,078) come from media reports because the official price page needs JavaScript. The current referral percentages (5% vs 10%) are also unverified.
5. **Alibaba "$1,700" trial credits**: this figure was not found on the campaign page.
6. **Kimi USD pricing** and the current value of the Kimi referral rewards (the page needs JavaScript) are unverified.
7. **Copilot Pro annual price** ($100/year) is no longer on the official pages.
8. **Endpoints**: I did not verify the Alibaba Token Plan endpoints or the MiniMax annual discount.
9. **AgentKit**: the 20% buyer discount for `?ref=` links is unverified. Only the referrer commission tiers are visible.
10. **Claude guest passes**: only third parties confirm that they are "Max-only, three passes". Anthropic's docs say only "if your account is eligible".
