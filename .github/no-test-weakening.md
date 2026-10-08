# No Test Weakening

## Core rule
NEVER remove, skip, or weaken a test assertion. A green build does not mean the code is correct.

## Mandatory guardrails
- Never delete a test to make a failing suite pass.
- Never comment out or disable a real assertion.
- Never replace a strong assertion with a weaker one.
- Never use .skip, .only, or equivalent bypasses to hide failing behavior.
- Never modify a test to match broken implementation instead of fixing the implementation.
- Never weaken validation for edge cases, error states, or regressions.

## Required mindset
- Tests are a correctness check, not a checklist to be satisfied by reducing strictness.
- If a test fails, the implementation must be fixed unless the test itself is demonstrably wrong.
- If a test appears incorrect, escalate for review instead of changing it silently.

## Review standard
Any change that removes assertions, bypasses checks, or reduces the strength of a test is not acceptable.
A passing build is only meaningful when the expected behavior remains fully enforced.
