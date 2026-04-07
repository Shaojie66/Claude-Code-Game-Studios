---
name: studio-test-helpers
description: Codex-native workflow for generating engine-aware shared test helper libraries
---

# Studio Test Helpers

Use this when the project needs shared factories, assertions, or helper scaffolding to reduce repetitive test boilerplate.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/test-helpers/SKILL.md`
4. `.claude/docs/technical-preferences.md`
5. Existing tests under `tests/`
6. `design/gdd/systems-index.md` and in-scope GDDs

## Goal

Create or refresh `tests/helpers/` with engine- and project-specific helper utilities that match the existing test style and system needs.

## Workflow

1. Resolve mode:
   - one system
   - `all`
   - `scaffold`
2. Detect the configured engine, language, and test framework.
3. Sample existing tests to learn the project’s current setup, assertion, factory, and mocking patterns.
4. Generate base helper utilities for the engine/framework in `tests/helpers/`.
5. In system-specific modes, generate helper files tailored to the selected systems using their GDD data, formulas, and common test scenarios.
6. Keep helper naming and style aligned with the existing suite rather than inventing a conflicting mini-framework.

## Codex Adaptation Rules

- Prefer matching the project’s current testing idioms over generic helper templates.
- Stop cleanly if the engine is not configured; route to `$studio-setup-engine` when necessary.
- Treat helpers as support code, not a substitute for writing real assertions in tests.
- Avoid generating unused layers of abstraction when the project has only lightweight needs.
- Keep the output engine-aware and system-aware.

## Handoff

Recommend the next step, usually `$studio-regression-suite`, `$studio-test-evidence-review`, or a focused test-writing pass that uses the new helpers.

## Completion

Complete when the intended helper files exist under `tests/helpers/` and are aligned with the project’s engine and test style.
