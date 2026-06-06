# Claude Code Instructions

This repository uses a repo-based AI Development Framework.

Default project context:

@docs/ai/context.md

Do not import all documentation by default. Read additional docs only when the task requires them.

Conditional docs:

- Architecture / modules / data flow / deployment → `@docs/ai/architecture.md`
- Behavior changes / validation / tests → `@docs/ai/testing-policy.md`
- Auth / permissions / tenant data / logs / PII / admin / integrations → `@docs/ai/security-policy.md`
- Release / production-impacting changes → `@docs/ai/release-policy.md`
- Code review tasks → `@docs/ai/code-review.md`
- Unclear domain terms → `@docs/ai/glossary.md`

Use only the relevant workflow:

- Backend change → `@.agents/skills/backend-change/SKILL.md`
- Frontend change → `@.agents/skills/frontend-change/SKILL.md`
- Bug fix → `@.agents/skills/bug-fix/SKILL.md`
- Code review → `@.agents/skills/code-review/SKILL.md`
- Release check → `@.agents/skills/release-check/SKILL.md`

Rules:

- Do not perform a full codebase scan unless explicitly required.
- Inspect only impacted modules and nearby related files.
- Make the smallest safe change.
- Follow existing project patterns.
- Do not perform broad refactors unless explicitly requested.
- Do not remove existing behavior unless explicitly requested.
- Do not bypass permissions, audit logs, or security checks.
- Do not expose secrets, tokens, credentials, or sensitive data.

Final response must include changed files, tests run, risks, and rollback notes.
