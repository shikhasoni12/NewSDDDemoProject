# PR Review

## Required PR checklist
Every pull request must be reviewed against the following items before merge:

- Spec compliance: confirm the PR fulfills the active requirement or ticket and does not broaden scope.
- Test evidence: verify the relevant tests were run and the results are included or available for review.
- Rollback steps: confirm there is a clear rollback or recovery path if the change causes issues after deployment.
- Security scan: check for exposed secrets, unsafe defaults, unsafe input handling, or privilege escalation risks.

## Review expectations
- Confirm the change is limited to the files and behavior described by the task.
- Check that the implementation is correct, readable, and maintainable.
- Validate that tests cover the changed behavior and that no assertions were weakened.
- Ensure log, error handling, and environment usage follow project policy.

## Blocking issues
A PR should be rejected or returned for changes when any of the following are present:
- missing or weak test evidence,
- scope drift beyond the active specification,
- possible security exposure or secret leakage,
- unclear rollback strategy,
- or a mismatch with the stated requirement.

## Merge standard
A PR is merge-ready only when the checklist is satisfied, the relevant verification has been completed, and the risk level is acceptable for deployment.
