---
name: Preserve markdown quotes
description: Do not edit quoted content in markdown unless explicitly requested
type: feedback
---

When editing markdown files, never modify content in blockquotes (lines starting with `>`) unless:
1. The user explicitly requests changes to that content in the prompt, OR
2. The content is being updated from a website the user wants crawled for fresh information

**Why:** Quoted content often represents exact citations or official documentation that should remain verbatim.

**How to apply:** When tuning/editing markdown, skip over any blockquote sections and leave them unchanged. Only modify quotes if the user specifically asks or when fetching updated info from a source URL.
