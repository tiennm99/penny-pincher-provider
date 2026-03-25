---
name: Project-local memory
description: Always save memories inside the project, not user global location
type: feedback
---

Always save memory files to the project's `.claude/memory/` directory, not to the user's global memory location (`~/.claude/projects/`).

**Why:** Keeps project-specific knowledge alongside the codebase for portability and version control.

**How to apply:** When creating or updating memories, always write to `.claude/memory/` within the project root.
