# Research Report: Additional Budget/Free LLM Providers for README

Date: 2026-09-21 09:32 (Asia/Saigon)

## Executive Summary

Goal: find free / budget LLM API providers and coding plans not yet in README.md. Two actively maintained
curated lists (mnfst/awesome-free-llm-apis, pushed 2026-08-21; peter123023/awesome-free-llm-api, pushed
2026-09-20, entries individually re-verified Aug 31–Sep 20) plus two official-doc fetches yielded **13 new
free-tier providers**. No new request-based coding-plan subscription survived verification.

Added to README (Free Providers): LongCat, SenseNova Token Plan, AMD Token Factory, Volcengine Ark,
Baidu Qianfan, iFlytek Spark, AIHubMix, OVHcloud AI Endpoints, LLM7.io, Token Harbor, Aion Labs,
Experiential Labs, Empero.

## Methodology

- Tool budget: 5 research calls (1 WebFetch 404, 2 WebSearch, 2 WebFetch). READMEs of 2 lists pulled via `gh api`.
- Sources: 2 GitHub lists, LongCat official docs, AMD Radeon Cloud page (support page only, no pricing), ~12 search-result blogs (secondary, used only for candidate discovery).
- Criteria: callable via API key + endpoint; free tier or ≤ ~$2/mo; source link available; not already in README.

## Rejected candidates

| Candidate | Reason |
|---|---|
| Chutes | No free endpoint since ~Sep 2026; all models priced (list re-checked 2026-09-12) |
| B.AI | Free tier ended 2026-09-16 17:00 SGT |
| Tencent Hunyuan | Old platform shuts 2026-09-30; new platform has no free models |
| AtomCode CodingPlan Lite | Client-only 7-day trial, 500 claims/day, no public endpoint |
| Together AI ($5), Nebius ($1), Novita ($0.50) | Trial-credit claims only from secondary blogs; no primary source within call budget |
| Gemini CLI / Antigravity CLI, Qwen Code | CLI tools, not API providers; Qwen Code free OAuth ended 2026-04-15 |
| Amazon Bedrock, Azure AI Foundry | Expiring cloud credits, no standing free tier |
| DeepInfra | Charges from first token |

## Flags on existing entries (not changed — out of scope)

- **Mistral La Plateforme**: README says "~1B tokens/month". mnfst (Aug 2026) says Free plan = **$10/month API credits**, training opt-out needed, numeric rate limits no longer published. peter123023 (Sep 2026) marks the free API tier as **cancelled**. Needs re-verification against <https://mistral.ai/pricing>.
- **TokenRouter**: Kimi K3 free promo expired 2026-08-12; current $0 models are qwen3.8-max-free, deepseek-v4-pro-0813-free, nemotron-3-nano-omni-free.
- **OrcaRouter**: all dated offers (Aug 6/21/24) have passed.
- **Kilo Code**: free pool now nvidia/nemotron-3-*, stepfun/step-3.7-flash, poolside/laguna-*, tencent/hy3 at 200 req/hr per IP, no key required.
- **Cerebras**: mnfst lists gpt-oss-120b/20b, qwen3.6-27b at 30 RPM / 1,000 RPD.

## References

- <https://github.com/mnfst/awesome-free-llm-apis>
- <https://github.com/peter123023/awesome-free-llm-api>
- <https://longcat.chat/platform/docs/zh/>
- <https://openrouter.ai/blog/tutorials/free-llm-apis-compared/>

## Unresolved questions

1. Mistral free tier: which of the three conflicting descriptions is current?
2. LongCat exact daily quota — only visible in console after signup.
3. AMD Token Factory: is `developer.amd.com.cn` reachable / usable outside mainland China?
