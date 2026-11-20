# README refresh review (Nov 20, 2026)

Scope: uncommitted `README.md` diff (273 insertions, 249 deletions). I spot-checked 27 entries against official pages,
checked structure and style, and looked for private details and prompt-injection text. README.md was not edited.

## Findings

| # | Entry | Severity | Problem | Evidence | Suggested exact fix |
|---|---|---|---|---|---|
| 1 | Alibaba Token Plan, Personal | Medium | `- Yearly: $65 / $100 / $195 / $490` has no current source. The official Personal overview lists no yearly prices. The campaign page has $65 / $100 / $195 / **$770**, but it still shows the pre-Nov 9 quotas (11,500 / 25,500 / 45,000 / 180,000) and Pro at $68, so it is out of date. The $490 figure appears in neither source. | https://www.alibabacloud.com/help/en/model-studio/token-plan-personal-overview, https://www.alibabacloud.com/campaign/ai-landing-page-token | Replace the line with `- Yearly billing also available (prices shown at checkout)`, or delete it. |
| 2 | Alibaba Token Plan, Personal | Low | The text calls it a "first month" price. The doc says it is a *new-user price* for accounts that have never bought a Personal Edition plan, valid until 23:59:59 Nov 30, 2026 (UTC+8). It also expires 10 days after the check date. | same overview | `- Lite: **$6/month** — 20,000 Credits (new-user price **$3** for accounts that never bought a Personal plan, until Nov 30, 2026 UTC+8)`. Change Essential the same way with `$5`. |
| 3 | Alibaba Token Plan, Team | Low | The Team overview lists Standard $20, Advanced $75 and Premium $180 with no list prices. The `(list $30)`, `(list $100)` and `(list $200)` figures come from the stale campaign page, which still uses the old tier names Pro and Max and says Max is $200. | https://www.alibabacloud.com/help/en/model-studio/token-plan-team-overview | Drop the three `(list …)` notes. |
| 4 | Synthetic | Medium | The text implies every plan has Fast and Infinite mode. The pricing page says: "Fast mode and Infinite mode are included with the Big or Bigger plan." | https://synthetic.new/pricing | `Big and Bigger plans add Fast mode (2× speed, 2× credits) and Infinite mode (slow, never counts against the limit; DeepSeek V4.1 Flash only).` |
| 5 | Synthetic | Medium | "regenerates 2% every ~3.4 h", "no 5-hour or monthly caps" and "extra usage bills at API pricing" are not on the pricing page, the home page or the API docs overview. Those pages only say "Credits regenerate over the week and apply at discounted model rates." | https://synthetic.new/pricing, https://synthetic.new/, https://dev.synthetic.new/docs/api/overview | Cite the source for these three claims, or reduce the text to `One weekly credit quota that regenerates over the week; models draw credits at discounted rates.` |
| 6 | Synthetic referral (blockquote) | Low | The blockquote changed from "$10.00 in subscription credit" to "up to $10.00 off your first month". I could not check this on a public page. The memory rule allows a blockquote edit only when it was refreshed from the source. | the referral link landing page (not publicly readable) | Keep the edit only if it was copied from the live referral page. Otherwise restore the old blockquote. |
| 7 | MiniMax M Plan | Low/Medium | Prices `Go $22 / Explore $55 / Build $132` could not be checked: the page renders them with JavaScript, and the docs link back to that page. The multiples (1× / 3× / 7.5×), the windows, the annual "pay 10 months, 2 free", the tier models and the one-year Credits validity are verified. The referral blockquote still links to `/subscribe/token-plan?...`, but "Token Plan is no longer available for new purchases." | https://www.minimax.io/m-plan, https://platform.minimax.io/docs/m-plan/token-plan-notice | Open the referral link and confirm it lands on M Plan checkout. If it does not, say so in a note under the blockquote (the blockquote itself stays verbatim). Check the prices in a real browser. |
| 8 | StepFun Step Plan | Low | `(since Jul 24, 2026; ...)` is not in the cited overview. The overview does confirm "no time-window or request-frequency limits" and that monthly credits are cleared at month end. | https://platform.stepfun.ai/docs/en/step-plan/overview.md | Delete `since Jul 24, 2026; ` or add the source that gives the date. You could also add `credits clear at month end`. |
| 9 | GonkaRouter | Low | The docs give the Anthropic base URL as `https://api.gonkarouter.io` (Claude Code adds `/v1` itself). The README gives the full messages URL as the base, which differs from the ModelScope and SenseNova entries. | https://gonkarouter.io/docs | `Anthropic-compatible at `https://api.gonkarouter.io` (`/v1/messages`).` |
| 10 | Google Cloud Vertex AI | Low | "This is the only no-cost path for new users" overstates it. The $300 trial still covers other GCP services; it is only Gemini platform services it no longer pays for. | https://docs.cloud.google.com/free/docs/free-cloud-features | `For Gemini on this platform, this is the only no-cost path for new sign-ups.` |
| 11 | opencode Go | Low | Go docs list `https://opencode.ai/inference/go` and the models list URL. The per-API URLs `.../inference/go/anthropic/v1` and `.../inference/go/openai/v1` are on the `/console/harnesses` page, which I did not open. | https://opencode.ai/docs/console/go/ | Check both URLs against the "Base URLs" section of the harnesses docs page before committing. |
| 12 | OpenCode Console | Low | The free table leaves out `jev-1.13-free`. It uses the System One endpoint rather than chat, so leaving it out may be deliberate. | https://opencode.ai/docs/console/models/ | Optional: add `| Jev 1.13 Free | `jev-1.13-free` | Not a chat model (System One endpoint) |`, or leave it out on purpose. |
| 13 | Z.ai GLM Coding Plan | Low | The Oct 16, 2026 key split is verified. "(ZCode and AutoClaw at 1.5× usage)" is not on the devpack overview. | https://docs.z.ai/devpack/notice/api-key-management, https://docs.z.ai/devpack/overview | Cite the page that states 1.5×, or remove the parenthetical. |
| 14 | Mistral Studio (removed) | Info | The removal is defensible: the official pricing page gives the Free plan no API credits, so the old $10/month claim is gone. The admin docs still say "Free mode is the default state for new accounts", and I could not tell from public pages whether a rate-limited free API allowance remains. | https://mistral.ai/pricing, https://docs.mistral.ai/admin/user-management-finops/subscriptions | No change needed. Re-add the entry only if a free API allowance is confirmed in the console. |

These claims were not verified because the pages render with JavaScript, so treat them as unchecked rather than wrong:
Kimi Code Ultra ¥1,399 and the ¥3,360/year saving; the two OrcaRouter deposit-match cards (DeepSeek V4.1 Flash
"Unlimited" and Fable 5.2: minimums, caps, dates); ModelScope Magicube figures; Volcengine Agent Plan.

## Structure, style, privacy, injection

- 49 `###` entries and 49 `*Checked Nov 20, 2026.*` lines. Every entry has a heading, a body and one Checked line.
  The Alibaba `####` subsections share one Checked line, as before the change.
- The `---` separators around the three sections and License are intact. I found no orphaned or duplicated
  paragraphs, no malformed `[...](...)` or `<...>` links, and no Liquid `{{`/`{%` (README is included into the
  Jekyll `index.md`, so Liquid tags would break the build).
- Style matches the rest of the README: bold prices, inline-code endpoints, `Source:` lines, and `**Warning:**`
  callouts.
- No private details were added: no local paths and no personal email. `@gmail.com` is Google's eligibility rule.
- No instruction-like text was copied from provider sites. The old first-person Xiaomi promo text ("I'm on Xiaomi MiMo
  ... Sign up with my code") was replaced with a neutral description, which is an improvement.
- Changed blockquotes: Synthetic referral and BytePlus referral. Both are allowed only if refreshed from the source;
  see finding 6. The BytePlus referral terms were not checked.

## Verified as correct

- **Hugging Face Inference Providers (removed):** free users now get "None" monthly credits; PRO gets $2.00. The removal is correct.
- **Ollama Cloud (removed):** the only $0 tier is per-token pay-as-you-go, with no starter credits. The removal is correct.
- **Novita AI (removed):** no $0/$0 models on the pricing page. The removal is correct.
- **StepFun Step Plan:** tiers, prices and credits, ~$1 ≈ 7M Credits, booster packs with a 30-day cycle, models, both
  endpoints, tools, Stripe or balance payment.
- **GonkaRouter:** 1M free tokens with no card, used before paid balance; $0.006/1M flat and floating; card, Alipay or USDT;
  the three models; ~200K-token practical prompt cap; OpenAI base URL.
- **Baidu Qianfan:** 1M tokens on each of 17 models, 3 months, auto-granted, online inference only; the model list matches.
- **Google Cloud Vertex AI:** the Nov 16, 2026 rule that the $300 credit cannot pay for Gemini platform; "card or other
  payment method"; the Gemini platform rename; express mode (90 days, no billing info, `@gmail.com`, new to GCP).
- **Alibaba Token Plan Personal:** monthly prices $6/$10/$18/$43, credits 20k/45k/80k/200k, quotas raised Nov 9,
  2026, new-user $3/$5 until Nov 30, extra bundle terms, no weekly cap, model list (qwen4-max-preview omitted, minor).
- **Alibaba Token Plan Team:** Standard/Advanced/Premium at $20/$75/$180 with 25k/100k/250k credits; $700 pack for 625k credits;
  the Team-only models.
- **OpenCode Console:** all ten listed free models and their retention notes; OpenAI and Anthropic inference URLs;
  "Free-tier chat models require OpenCode".
- **opencode Go:** $10 / $40 / Teams $20 per member with a 2-member minimum; 5-hour = 20% and weekly = 50% of monthly; ~3,210 MiniMax-M3 and
  ~994 Kimi K2.7 Code requests per 5 h; 32 models; `opencode-go/<model-id>`; Extra Usage falls back to Console credit.
- **Synthetic:** Go $9 / Standard $30 / Big $90 / Bigger $300; the model list; the privacy quote (home page); Infinite mode
  DeepSeek V4.1 Flash only.
- **OrcaRouter:** the always-free model IDs, including the new `deepseek/deepseek-v4.1-flash-free` (public `/v1/models`); the
  GitHub-history or paid-purchase requirement.
- **Z.ai GLM Coding Plan:** from Oct 16, 2026, Personal Coding Plan keys draw plan quota, Standard keys bill pay-as-you-go,
  and older keys keep working as Compatible.
- **Cerebras:** free-trial limits table, including the temporary 750K total TPM for qwen-3.8-27b.
- **Tencent TokenHub:** Hy plan ¥28–¥468 and universal plan ¥39 (780 pts) to ¥599; universal models; new `tokenhub.tencentmaas.com`
  endpoints; tools only with scripted or backend use banned; no refunds; Hy4 preview retires Dec 7, 2026.
- **LLM7.io:** the old limits page returns 404; the turbo tier is codestral-latest, gemma-3-27b, gpt-oss:20b and Mistral Nemo.
- **Nebius:** Builder Program gives $25 Token Factory, $25 Tavily and $50 Toloka credit after email verification.
- **Kilo Code Gateway:** new base URL `https://ai-gateway.kilo.ai/api/v1`. The 5% fee and Kilo Pass prices were not checked.
- **AgentKit:** 7 runtimes and 3 in preview; Engineer and Marketing $99 one-time; Bundle $149 with 12 months of the 3-device app;
  app $49/$99 per year on macOS, Windows and Linux.
- **MiniMax M Plan (partial):** tiers and multiples, windows, annual terms, tier models, Credits valid one year, tools
  list, and "Token Plan is no longer available for new purchases".

## Unresolved questions

1. Synthetic: where do the 2%/~3.4 h regeneration figure and the referral wording come from?
2. MiniMax: does the `token-plan` referral link still work now that Token Plan is closed to new buyers?
3. Mistral: is there still any free, rate-limited API allowance in Free mode? (This affects whether removing the entry is right.)
