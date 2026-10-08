# AGENTS.md --- NewSDDDemoProject

## Project Overview
NewSDDDemoProject is a lightweight static web application built with HTML, CSS, and JavaScript modules. It is designed for maintainability, simple local development, and predictable UI behavior without heavy framework overhead.

## Tech Stack
- HTML5
- CSS3
- JavaScript (ES modules)
- Vite
- Jest or Vitest

## Key Modules
- src/pages/ → Top-level pages or views. Each owns its own DOM state and initialization logic.
- src/components/ → Shared UI elements. Keep them reusable and free of business logic.
- src/services/ → API clients and external integrations. All network calls go through services/.
- src/utils/ → Shared helper functions and reusable logic.
- src/styles/ → Global styling, design tokens, and shared CSS modules.
- public/ → Static assets such as images, icons, and favicon files.

## Team Conventions
- Keep code organized by feature and responsibility.
- Prefer semantic HTML and accessible interactions over custom hacks.
- Use a shared service layer for API access instead of network logic scattered across pages.
- Keep module boundaries clear so pages, components, services, and utilities do not mix responsibilities.
- Use descriptive, consistent naming and keep functions focused on a single task.
- Favor small, reviewable changes over broad refactors.

## Project Context
- This project is intentionally lightweight and modular, with a static HTML and JavaScript structure.
- The application is designed to stay maintainable without introducing unnecessary framework overhead.
- Team work should remain focused on small, reviewable changes and predictable UI behavior.
- The project should remain easy to understand for new contributors and easy to test for regression coverage.

## Common Workflows
- New page: add the page structure and script, connect it to the app flow, and validate the user journey.
- New API call: implement it in the service layer, add test fixtures if needed, and verify behavior with coverage.
- New utility: place it under src/utils/, keep it reusable, and add a focused test when behavior matters.
- Deploy: merge to the main branch, let CI validate the build, and deploy through the existing hosting or release flow.

## Warm Context — Always Attach When Working On
- Auth: src/services/auth.js, src/utils/auth.js
- Routing: src/app.js or src/router.js
- Global state: src/store/index.js or src/state/store.js

## Testing Expectations
- Add or update tests whenever behavior changes.
- Prefer real behavior over mock-only assertions.
- Validate the critical user flows and accessibility basics before merging.
- Never weaken a test to get a green build.

## Quality and Safety Guardrails
- Never modify node_modules or .env files.
- Never commit secrets or API keys.
- Never change unrelated files outside the active task scope.
- Never add debug logs to production code without a valid reason.
- Keep modifications aligned with the project structure and design principles.

## Decision Log
2024-03-15: Chose vanilla JavaScript with modular structure over a heavier framework for simpler maintenance and faster startup.
2024-05-02: Adopted Vite for local development and build tooling to improve performance and DX.
