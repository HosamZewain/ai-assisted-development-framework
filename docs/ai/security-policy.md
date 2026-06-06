# Security Policy

This file documents security rules AI tools must follow.

## Authentication

- Current auth model: `TBD - needs team confirmation`
- Important auth files: `TBD - needs team confirmation`
- Do not bypass authentication checks.
- Do not weaken login/session/token validation.

## Authorization / Permissions

- Current permission model: `TBD - needs team confirmation`
- Important permission files: `TBD - needs team confirmation`
- Preserve role-based and permission-based access checks.
- Admin features must keep server-side permission validation.

## Data Isolation

If the system is multi-tenant or customer-scoped:

- Keep every data query scoped correctly.
- Do not remove tenant/customer/organization/branch filters.
- Do not hardcode scope IDs.
- Do not expose cross-scope data in APIs, logs, exports, or UI.

## Sensitive Data

Never expose or log unnecessarily:

- Passwords
- Tokens
- API keys
- Private keys
- Secrets
- Personal data
- Customer confidential data
- Payment data

## API Security

- Validate user-controlled input.
- Preserve existing request validation.
- Preserve rate limiting if present.
- Preserve webhook signature validation if present.
- Do not expose internal errors to end users.

## AI Must Never

- Log secrets
- Bypass permissions
- Remove data-scope filters
- Hardcode tenant/customer IDs
- Weaken validation
- Return sensitive data across scopes
- Disable audit logs
- Change security behavior without explicit approval
