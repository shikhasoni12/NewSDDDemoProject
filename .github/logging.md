# Logging

## Core rule
Every new code path must emit a structured log entry at entry and exit.

## Mandatory requirements
- Log at the start of a function, method, request handler, or workflow entry point.
- Log again when the code path completes successfully or exits through a terminal branch.
- Include enough structured context to understand what happened, such as operation name, status, and relevant identifiers.
- Keep log payloads consistent and machine-readable.
- Do not log raw secrets, tokens, passwords, or other sensitive values.

## Guardrails
- Do not add noisy or duplicate log statements in every internal helper unless it is required for tracing.
- Do not log sensitive data even when it appears in request or response payloads.
- Do not leave debug logging in production code after the issue is resolved.

## Review standard
A code path is incomplete if it does not emit a clear start and end log record for the main execution flow.
