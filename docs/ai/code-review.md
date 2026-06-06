# Code Review Checklist

Use this for AI-assisted code reviews.

## Correctness

- Does the change solve the requested problem?
- Does it preserve existing behavior?
- Are edge cases handled?
- Are error states handled?

## Security

- Authentication preserved?
- Authorization preserved?
- Sensitive data protected?
- Secrets not exposed?
- Admin access protected?

## Data Isolation

- Queries scoped correctly?
- No cross-tenant/customer leakage?
- No hardcoded scope IDs?
- Exports/logs/API responses safe?

## Performance

- No obvious N+1 queries?
- Expensive queries limited/paginated?
- Background jobs used where needed?
- Caching not broken?

## Database

- Migration required?
- Migration backward-compatible?
- Rollback notes included?
- Existing data preserved?

## API

- Contract compatible?
- Response shape changed intentionally?
- Error handling consistent?
- Validation preserved?

## Frontend

- Existing UX patterns preserved?
- Responsive behavior preserved?
- Loading/error/empty states handled?
- Permissions reflected correctly?

## Tests

- Regression tests added?
- Relevant tests run?
- Missing tests explained?

## Review Output Format

```md
## Summary
## Blockers
## Suggestions
## Questions
## Required Tests
## Risk Level
```
