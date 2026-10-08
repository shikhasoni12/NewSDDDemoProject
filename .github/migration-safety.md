# Migration Safety

## Core rule
Every migration requires a paired rollback migration. Test against a staging copy only.

## Mandatory requirements
- Each schema or data migration must include a matching rollback migration that can reverse the change safely.
- Never apply a migration directly to production data without validating it on a staging copy first.
- Review migration order, dependencies, and data impact before execution.
- Validate that both forward and rollback paths are realistic and tested.

## Guardrails
- Do not assume a migration is reversible without confirming the rollback steps.
- Do not run destructive or irreversible operations against production data without explicit approval and staging validation.
- Do not use production data for migration testing.
- Do not leave a migration in place without an identified rollback path.

## Required practice
- Test the migration against a staging copy that mirrors production conditions as closely as possible.
- Verify data integrity, application compatibility, and rollback behavior before merge or deployment.
- Keep rollback steps documented and easy to execute in an incident.

## Review standard
A migration is not considered safe unless it has a paired rollback, has been tested on staging, and presents no unacceptable data risk.
