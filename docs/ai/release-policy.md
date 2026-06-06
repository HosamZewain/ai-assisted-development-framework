# Release Policy

Use this file for production-impacting changes and release validation.

## Release Readiness Checklist

- [ ] Scope is clear
- [ ] Risk level is identified
- [ ] Required tests passed
- [ ] Migrations reviewed, if any
- [ ] Config/env changes documented, if any
- [ ] Rollback notes documented
- [ ] Monitoring/logging impact reviewed
- [ ] Release notes prepared

## Risk Levels

### Low Risk

- Small UI copy/style changes
- Internal-only documentation
- Isolated non-critical bug fixes

### Medium Risk

- API behavior changes
- Business logic changes
- Admin feature changes
- Background job changes

### High Risk

- Authentication/authorization changes
- Data isolation changes
- Database migrations
- Payment/billing changes
- Release/deployment scripts
- External integration changes
- Large refactors

## Rollback Notes

Every production-impacting change should explain:

- How to revert the code
- Whether database rollback is needed
- Whether config rollback is needed
- How to validate rollback success

## Post-Release Monitoring

Document what to monitor:

- Error rate
- Logs
- Background jobs
- API latency
- Critical user flows
- Business metrics impacted by the release
