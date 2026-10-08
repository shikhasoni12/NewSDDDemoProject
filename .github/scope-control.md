# Scope Control

## Core rule
Only modify files named in the active specification or task. Flag any deviation immediately.

## Mandatory guardrails
- Do not edit unrelated files just because they are nearby or easy to touch.
- Do not broaden the task by refactoring outside the requested scope.
- Do not change configuration, infrastructure, or generated files unless the active spec explicitly requires it.
- Do not add unrelated cleanup, formatting, or incidental fixes during the same task.
- Do not make opportunistic improvements that are not part of the requested work.

## Required behavior
- Confirm the affected files before making a change.
- Keep the patch limited to the exact files required for the task.
- If a required fix appears to depend on a change outside scope, stop and flag the dependency explicitly.
- If a file is modified unexpectedly, call it out immediately and justify the exception.

## Review standard
Any change outside the active spec is a scope deviation and must be flagged before proceeding.
A narrow, reviewable task is more correct and safer than a broad cleanup disguised as a fix.
