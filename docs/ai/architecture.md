# Architecture

This file documents the actual technical architecture of the project.

Do not write generic architecture here. Base it on the codebase.

## Technology Stack

- Backend language/framework: `TBD - needs team confirmation`
- Frontend language/framework: `TBD - needs team confirmation`
- Database: `TBD - needs team confirmation`
- Cache: `TBD - needs team confirmation`
- Queues/background jobs: `TBD - needs team confirmation`
- Search/analytics: `TBD - needs team confirmation`
- File storage: `TBD - needs team confirmation`
- Deployment/runtime: `TBD - needs team confirmation`
- Testing tools: `TBD - needs team confirmation`

## Codebase Structure

Update with real paths.

```txt
src/                 # TBD
app/                 # TBD
tests/               # TBD
config/              # TBD
```

## Main Modules

For each real module, document:

```md
### Module Name

Purpose:
Key paths:
Main responsibilities:
Important dependencies:
Risks when modifying:
```

## Important Data Flows

Document only flows found or inferred from the codebase.

Examples:

- User login
- Permission validation
- Main business transaction
- Background processing
- Notification flow
- Reporting flow
- External integration flow

## Deployment / Runtime

Document what exists:

- Docker: `Not found in current codebase scan`
- Kubernetes: `Not found in current codebase scan`
- CI/CD: `Not found in current codebase scan`
- Environment variables: `TBD - needs team confirmation`
- Scheduled jobs: `TBD - needs team confirmation`
- Monitoring: `TBD - needs team confirmation`

## Architecture Rules For AI

- Do not change module boundaries without explicit approval.
- Do not introduce new architectural patterns unless requested.
- Prefer existing service/repository/controller patterns.
- Keep changes local to the impacted module.
- Mark uncertain assumptions as `TBD - needs team confirmation`.
