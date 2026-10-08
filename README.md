# NewSDDDemoProject

A lightweight static web application built with HTML, CSS, and JavaScript modules. The project is designed to keep the frontend simple, modular, and maintainable without introducing unnecessary framework overhead.

## Overview

This project follows a structured front-end layout with clear separation between pages, shared UI, services, utilities, and styles. It is intended to be easy to extend, review, and deploy while staying fast to run locally.

## Tech Stack

- HTML5
- CSS3
- JavaScript (ES modules)
- Vite
- Jest or Vitest

## Project Structure

- src/pages/ — top-level pages or views
- src/components/ — reusable UI elements without business logic
- src/services/ — API and external integrations
- src/utils/ — shared helper functions
- src/styles/ — global styling and design tokens
- public/ — static assets such as images, icons, and favicon files

## Goals

- Keep the frontend modular and easy to reason about
- Favor semantic HTML and accessible patterns
- Centralize API work in service modules
- Maintain a small, reviewable codebase
- Support predictable local development and deployment workflows

## Getting Started

Prerequisites:

- Node.js 18 or newer
- npm

Install dependencies:

npm install

Start the development server:

npm run dev

Build for production:

npm run build

Run tests:

npm test

## Development Workflow

1. Create or update the page and its script logic.
2. Keep UI and business logic separated where possible.
3. Use service modules for API calls.
4. Add or update tests for behavior changes.
5. Validate accessibility and critical flows before merging.

## Testing

The project is intended to use Jest or Vitest with Testing Library for browser and unit-style verification. Tests should validate real behavior and critical user journeys instead of mock-only assertions.

## Security and Quality Rules

- Never commit secrets or API keys
- Never modify environment files or dependency folders directly
- Never weaken tests to get a green build
- Keep changes within the active task scope
- Prefer clear, small, maintainable code changes

## Notes

This repository currently serves as a project foundation and documentation scaffold for a modular HTML and JavaScript application. As the app grows, the structure and implementation details should be updated to match the actual feature set and deployment flow.
