# AI Development Framework Template

A practical repo-based framework for using AI coding tools consistently across a software team.

This template helps teams standardize how developers use tools like Codex, Claude Code, Cursor, Antigravity, or any AI coding assistant while working on the same codebase.

The main idea is simple:

> Do not depend on chat memory. Put the project context, engineering rules, and AI workflows inside the repository.

---

## What This Folder Contains

```txt
.
├── AGENTS.md
├── CLAUDE.md
├── docs/
│   └── ai/
│       ├── context.md
│       ├── architecture.md
│       ├── coding-standards.md
│       ├── testing-policy.md
│       ├── security-policy.md
│       ├── release-policy.md
│       ├── code-review.md
│       └── glossary.md
├── .agents/
│   └── skills/
│       ├── backend-change/SKILL.md
│       ├── frontend-change/SKILL.md
│       ├── bug-fix/SKILL.md
│       ├── code-review/SKILL.md
│       └── release-check/SKILL.md
└── examples/
    └── generate-framework-prompt.md
```

---

## Purpose

This framework gives AI tools a shared operating model for your project.

It helps AI tools understand:

- What the product does
- How the codebase is structured
- Which rules must never be broken
- How to safely make backend changes
- How to safely make frontend changes
- How to fix bugs with minimal risk
- How to review code
- How to validate releases
- How to avoid wasting tokens by reading unnecessary files

---

## Core Concept

Use a small always-read context file, then read extra docs only when needed.

```txt
Always read:
- AGENTS.md
- docs/ai/context.md

Read conditionally:
- architecture.md       → architecture, modules, data flow, infra
- testing-policy.md     → behavior changes and validation
- security-policy.md    → auth, permissions, tenant data, PII, logs
- release-policy.md     → production/release work
- code-review.md        → PR/code review tasks
- glossary.md           → unclear product/domain terms

Use one relevant skill:
- backend-change
- frontend-change
- bug-fix
- code-review
- release-check
```

---

## How To Use This Template

### Option 1: Copy this template manually

Copy these files into the root of your project repository:

```txt
AGENTS.md
CLAUDE.md
docs/ai/
.agents/skills/
```

Then edit the files to match your real project.

### Option 2: Ask an AI coding tool to generate your project-specific version

Open your project in Codex, Claude Code, Cursor, Antigravity, or a similar tool.

Then use the prompt in:

```txt
examples/generate-framework-prompt.md
```

The AI should inspect your codebase and generate project-specific framework files.

---

## Recommended Team Adoption Flow

1. Generate the first framework draft.
2. Open a Draft PR.
3. Ask the Tech Lead and senior developers to review it.
4. Fix inaccurate architecture, security, and testing assumptions.
5. Approve it as the official AI-assisted development framework.
6. Require all AI-assisted work to follow it.
7. Keep the framework updated after major architecture or process changes.

---

## Important Rules

This framework should not become huge.

Bad approach:

```txt
Before every task, read every document and scan the whole repository.
```

Good approach:

```txt
Read the minimum required context.
Inspect only impacted modules.
Use the relevant skill.
Run the smallest useful validation.
```

---

## Customization Checklist

Before using this in production, update:

- Product name
- Tech stack
- Main modules
- Architecture folders
- Testing commands
- Security and permission model
- Tenant isolation rules, if applicable
- CI/CD and release process
- Monitoring tools
- Known risk areas
- Glossary terms

---

## What Not To Put In These Files

Do not include:

- Secrets
- API keys
- Passwords
- Private tokens
- Customer data
- Production credentials
- Long logs
- Large copied requirements documents
- Temporary task-specific instructions

---

## Suggested PR Title

```txt
Add AI Development Framework
```

---

## Suggested Commit Message

```txt
docs: add AI development framework
```
