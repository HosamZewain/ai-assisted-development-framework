# Coding Standards

This file should reflect actual project patterns.

## Existing Patterns

- Architecture pattern: `TBD - needs team confirmation`
- Backend pattern: `TBD - needs team confirmation`
- Frontend pattern: `TBD - needs team confirmation`
- Database access pattern: `TBD - needs team confirmation`
- Validation pattern: `TBD - needs team confirmation`
- Error handling pattern: `TBD - needs team confirmation`
- Logging pattern: `TBD - needs team confirmation`

## General Rules

- Follow existing file and naming conventions.
- Keep changes minimal and localized.
- Prefer readable code over clever abstractions.
- Avoid duplicated business logic.
- Avoid silent error handling.
- Preserve backward compatibility.
- Do not mix refactoring with feature work unless requested.

## Backend Rules

- Reuse existing services/helpers when available.
- Validate inputs at the same layer used by the codebase.
- Preserve permission and data-scope checks.
- Keep API response shapes backward-compatible unless explicitly changed.

## Frontend Rules

- Reuse existing components and UI patterns.
- Preserve responsive behavior.
- Preserve loading, empty, and error states.
- Do not hide backend permission problems only in the UI.
- Do not assume API contract changes without checking backend code.

## Database Rules

- Do not change schema without migration and rollback notes.
- Avoid expensive queries without pagination or limits.
- Preserve existing indexes and query scopes.
- Do not remove existing data fields without explicit approval.
