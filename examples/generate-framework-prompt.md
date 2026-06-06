# Generate AI Development Framework Prompt

Use this prompt inside your project repository with an AI coding tool.

---

You are working inside an existing software project repository.

Your task is to generate a complete AI Development Framework for this repository.

This framework will help developers use AI coding tools consistently and safely across the project.

This is a documentation and AI-framework task only.

Do NOT change application behavior.
Do NOT refactor production code.
Do NOT fix bugs.
Do NOT rename production files.
Do NOT change dependencies.
Do NOT create migrations.
Do NOT change database schemas.
Do NOT modify business logic.
Do NOT include secrets, credentials, tokens, private keys, or sensitive production data.

---

## Main Objective

Create a repo-based AI Development Framework that gives AI coding assistants enough context to safely work on this project.

The framework must help AI tools understand:

- What the product does
- The main modules of the system
- How the codebase is organized
- The architecture and technology stack
- How backend changes should be done
- How frontend changes should be done
- How bug fixes should be done
- How code reviews should be done
- How releases should be validated
- Security rules
- Data isolation / multi-tenancy rules, if applicable
- Testing expectations
- Common risk areas
- Forbidden AI behaviors
- Required validation before finishing any task

Avoid generic documentation.
Base the output on the actual codebase.

---

## Discovery Phase

Before creating files, inspect the codebase carefully.

Review, where available:

- Root project structure
- README files
- package.json / composer.json / pyproject.toml / requirements files / lock files
- Backend source folders
- Frontend source folders
- Config files
- Environment example files
- Routes
- Controllers
- Services
- Models/entities/schemas
- Middlewares/guards/interceptors
- Authentication and authorization logic
- Tenant/customer/organization scoping logic
- Database migrations or schemas
- Background jobs / queues / workers
- Integrations
- API clients
- Logging and monitoring code
- Test folders
- CI/CD files
- Docker/Kubernetes/Helm/Argo/deployment files if available
- Playwright or E2E test setup if available
- Release-related scripts or docs

Do not assume anything without evidence.

If something is clearly found in the codebase, document it normally.

If something is inferred from code structure, write:

`Inferred from codebase: ...`

If something is important but unclear, write:

`TBD - needs team confirmation`

If something is not found, write:

`Not found in current codebase scan`

---

## Required Structure

Create this exact structure:

```txt
AGENTS.md
CLAUDE.md

docs/
└── ai/
    ├── context.md
    ├── architecture.md
    ├── coding-standards.md
    ├── testing-policy.md
    ├── security-policy.md
    ├── release-policy.md
    ├── code-review.md
    └── glossary.md

.agents/
└── skills/
    ├── backend-change/
    │   └── SKILL.md
    ├── frontend-change/
    │   └── SKILL.md
    ├── bug-fix/
    │   └── SKILL.md
    ├── code-review/
    │   └── SKILL.md
    └── release-check/
        └── SKILL.md
```

---

## Token-Efficiency Requirement

The framework must avoid wasting tokens.

Use this principle:

> Small always-on context. Task-based documentation. Skill-based workflows. No full repo scan unless explicitly needed.

Rules:

- `docs/ai/context.md` is the only default required read.
- Do not instruct AI tools to read all docs before every task.
- Do not instruct AI tools to load all skills before every task.
- Extra docs should be read only when relevant.
- Only the relevant skill should be used.
- Full codebase scans should happen only when explicitly requested or required for safety.
- Normal tasks should inspect only impacted modules and nearby related files.

---

## AGENTS.md Requirements

Create a short, strict, operational `AGENTS.md`.

It should include:

### Default reading

Always read only:

- `docs/ai/context.md`

### Conditional reading

- Architecture / modules / data flow / deployment → `docs/ai/architecture.md`
- Behavior changes / validation / tests → `docs/ai/testing-policy.md`
- Auth / permissions / data isolation / logs / PII / admin / integrations → `docs/ai/security-policy.md`
- Release / production-impacting changes → `docs/ai/release-policy.md`
- Code review tasks → `docs/ai/code-review.md`
- Unclear domain terms → `docs/ai/glossary.md`

### Skill usage

Use only the relevant skill:

- Backend change → `.agents/skills/backend-change/SKILL.md`
- Frontend change → `.agents/skills/frontend-change/SKILL.md`
- Bug fix → `.agents/skills/bug-fix/SKILL.md`
- Code review → `.agents/skills/code-review/SKILL.md`
- Release check → `.agents/skills/release-check/SKILL.md`

### Work rules

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

### Final response

Always include:

- Changed files
- What changed
- Tests run
- Tests not run, if any
- Risks
- Rollback notes

---

## CLAUDE.md Requirements

Create `CLAUDE.md` for Claude Code.

It should:

- Import only `@docs/ai/context.md` by default.
- Conditionally reference other docs only when relevant.
- Reference relevant skills only when needed.
- Repeat the same work rules as `AGENTS.md`.
- Make clear that `docs/ai` is the source of truth.

Do not import all docs by default.

---

## docs/ai/context.md Requirements

This is the most important shared context file.

It must be concise and include:

- Product summary
- Core modules
- Architecture summary
- Critical rules
- Data isolation / multi-tenancy rules, if applicable
- Common risk areas
- AI working policy
- Token-efficient reading policy

Add this section:

```md
## Token-Efficient Reading Policy

Always read this file first.

Then read other docs only when relevant:

- Architecture changes → `docs/ai/architecture.md`
- Behavior/test changes → `docs/ai/testing-policy.md`
- Auth/security/data-scope/admin/logging changes → `docs/ai/security-policy.md`
- Release validation → `docs/ai/release-policy.md`
- Code review → `docs/ai/code-review.md`
- Unclear domain terms → `docs/ai/glossary.md`
```

---

## docs/ai/architecture.md Requirements

Document the actual technical architecture:

- Technology stack
- Codebase structure
- Main services/modules
- Important data flows
- Deployment/runtime
- Architecture rules for AI

Use actual paths from the repo.
Mark uncertain items as `TBD - needs team confirmation`.

---

## docs/ai/coding-standards.md Requirements

Document coding standards based on actual code:

- Existing patterns
- Backend conventions
- Frontend conventions
- API conventions
- Error handling
- Logging
- Validation
- Database access
- Permission checks
- Data scoping
- Rules for safe changes

---

## docs/ai/testing-policy.md Requirements

Document:

- Test frameworks found
- Test folders
- Unit test commands
- Integration test commands
- E2E/UI test commands
- Lint/typecheck commands
- When to add tests
- What to do if tests cannot be run
- Minimum validation checklist

---

## docs/ai/security-policy.md Requirements

Document:

- Authentication rules
- Authorization rules
- Data isolation / tenant rules
- Sensitive data handling
- Logging restrictions
- Secrets handling
- API security
- Admin permissions
- Common mistakes AI must avoid

---

## docs/ai/release-policy.md Requirements

Document:

- Release readiness checklist
- Risk levels
- Migration/config checklist
- Monitoring checklist
- Rollback notes expectations
- Release notes expectations
- Post-release validation

---

## docs/ai/code-review.md Requirements

Create a practical review checklist covering:

- Correctness
- Security
- Data isolation
- Performance
- Database changes
- API changes
- Frontend impact
- Tests
- Release risk

Use this output format:

```md
## Summary
## Blockers
## Suggestions
## Questions
## Required Tests
## Risk Level
```

---

## docs/ai/glossary.md Requirements

Create concise definitions for project-specific terms found in the codebase.

For each term:

```md
## Term
Definition:
Where used:
Related modules:
Notes:
```

Do not invent definitions. Use `TBD - needs team confirmation` when unclear.

---

## Skills Requirements

Each skill file must start with metadata:

```md
---
name: skill-name
description: Use this skill only for ...
---
```

Each skill must include:

- Purpose
- When to use
- Required docs to read
- Step-by-step workflow
- Validation checklist
- Forbidden actions
- Final response format

Create these skills:

1. `.agents/skills/backend-change/SKILL.md`
2. `.agents/skills/frontend-change/SKILL.md`
3. `.agents/skills/bug-fix/SKILL.md`
4. `.agents/skills/code-review/SKILL.md`
5. `.agents/skills/release-check/SKILL.md`

Every skill should say:

- Read only the required docs for this task.
- Inspect only impacted modules.
- Do not scan the full repo unless needed.
- Keep changes minimal.
- Report if more context is needed.

---

## Clean Unwanted Files

Remove if present:

```txt
.DS_Store
__MACOSX/
```

Add to `.gitignore` if not already present:

```gitignore
.DS_Store
__MACOSX/
```

---

## Final Output Required

After creating the files, respond with:

## Files Created
List all created framework files.

## Codebase Areas Inspected
Summarize what parts of the repo you inspected.

## Key Findings
Summarize the main architecture, modules, and patterns found.

## Assumptions / Inferred Items
List anything inferred from the codebase.

## TBD Items
List all important items marked as `TBD - needs team confirmation`.

## Risks / Gaps
List missing or unclear areas in the current repo documentation, tests, or architecture.

## Recommended Review Process
Suggest how the Tech Lead and dev team should review and approve these files.

Remember:
Do not change production code.
Only create the AI Development Framework documentation and skill files.
