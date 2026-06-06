# Project AI Instructions

This repository uses a repo-based AI Development Framework.

AI tools must keep changes safe, minimal, and consistent with the existing codebase.

## Default Reading

Before any code change, read:

- `docs/ai/context.md`

Do not read all AI docs by default.

Read extra docs only when relevant:

- Architecture / modules / data flow / deployment → `docs/ai/architecture.md`
- Behavior changes / validation / tests → `docs/ai/testing-policy.md`
- Auth / permissions / tenant data / logs / PII / admin / integrations → `docs/ai/security-policy.md`
- Release / production-impacting changes → `docs/ai/release-policy.md`
- Code review tasks → `docs/ai/code-review.md`
- Unclear domain terms → `docs/ai/glossary.md`

## Skills

Use only the relevant skill:

- Backend change → `.agents/skills/backend-change/SKILL.md`
- Frontend change → `.agents/skills/frontend-change/SKILL.md`
- Bug fix → `.agents/skills/bug-fix/SKILL.md`
- Code review → `.agents/skills/code-review/SKILL.md`
- Release check → `.agents/skills/release-check/SKILL.md`

## Work Rules

- Do not perform a full codebase scan unless explicitly required.
- Inspect only impacted modules and nearby related files.
- Make the smallest safe change.
- Follow existing patterns.
- Do not perform broad refactors unless explicitly requested.
- Do not remove existing behavior unless explicitly requested.
- Do not hardcode customer-specific, tenant-specific, or environment-specific behavior.
- Do not bypass permissions, audit logs, or security checks.
- Do not expose secrets, tokens, credentials, or sensitive data.
- Do not change database schema without migration and rollback notes.

## Testing

When behavior changes:

- Add or update relevant tests when possible.
- Run the smallest relevant test set.
- Run lint/typecheck if available and relevant.
- If tests cannot be run, clearly say why.

## Final Response

Always include:

- Changed files
- What changed
- Tests run
- Tests not run, if any
- Risks
- Rollback notes
