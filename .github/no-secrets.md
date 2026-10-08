# No Secrets

## Core rule
NEVER hardcode API keys, tokens, credentials, or other sensitive values. Use environment variables or a secure secret-management mechanism instead.

## Mandatory guardrails
- Do not commit secrets to source control.
- Do not place credentials in config files, sample files, docs, or test fixtures unless they are clearly redacted.
- Do not paste tokens into code comments, logs, or debugging output.
- Do not use local environment values as permanent defaults in committed code.
- Do not store production secrets in .env files that are tracked by git.

## Required practice
- Read secrets from environment variables when the app runs.
- Keep example values clearly marked as placeholders, not real credentials.
- Validate that no sensitive data is included before submitting code.

## Review standard
Any hardcoded secret or accidental credential exposure is a blocking issue and must be removed before merge.
