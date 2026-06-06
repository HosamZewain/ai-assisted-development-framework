# Project Context

Replace this file with project-specific context generated from your real codebase.

This is the only shared context file that AI tools should read by default.

## Product Summary

- Product name: `TBD - needs team confirmation`
- Product type: `TBD - needs team confirmation`
- Primary users: `TBD - needs team confirmation`
- Main business problem: `TBD - needs team confirmation`

## Core Modules

Document only modules that exist in the codebase.

Example:

- Authentication
- Users and roles
- Admin panel
- Customer management
- Orders / tickets / interactions
- Reporting
- Notifications
- Integrations

## Architecture Summary

- Backend: `TBD - needs team confirmation`
- Frontend: `TBD - needs team confirmation`
- Database: `TBD - needs team confirmation`
- Cache / queues: `TBD - needs team confirmation`
- Search / analytics: `TBD - needs team confirmation`
- Deployment: `TBD - needs team confirmation`

## Critical Rules

- Follow existing code patterns.
- Make minimal, localized changes.
- Preserve backward compatibility.
- Do not remove existing behavior unless explicitly requested.
- Do not bypass permissions, audit logs, or security checks.
- Do not expose secrets or sensitive data.
- Do not perform broad refactors unless explicitly requested.

## Data Isolation Rules

If the system is multi-tenant or customer-scoped:

- Every data query must preserve the correct scope.
- Do not hardcode tenant, customer, branch, organization, or environment-specific logic.
- Do not expose data across scopes.
- Scope exceptions must be configuration-driven and reviewed.

If the system is not multi-tenant, replace this section with the real data isolation model.

## Common Risk Areas

Update this list based on the project:

- Authentication and authorization
- Role and permission checks
- Data scoping
- Database migrations
- Background jobs
- External integrations
- Payment / billing logic
- Admin settings
- Reporting calculations
- Release scripts

## AI Working Policy

Before editing:

1. Read this file.
2. Understand the user request.
3. Inspect only impacted modules and nearby related files.
4. Do not scan the full repo unless explicitly required.
5. Make the smallest safe change.
6. Add/update tests when behavior changes.
7. Run the smallest relevant validation.
8. Report changed files, tests, risks, and rollback notes.

## Token-Efficient Reading Policy

Always read this file first.

Then read other docs only when relevant:

- Architecture changes → `docs/ai/architecture.md`
- Behavior/test changes → `docs/ai/testing-policy.md`
- Auth/security/data-scope/admin/logging changes → `docs/ai/security-policy.md`
- Release validation → `docs/ai/release-policy.md`
- Code review → `docs/ai/code-review.md`
- Unclear domain terms → `docs/ai/glossary.md`
