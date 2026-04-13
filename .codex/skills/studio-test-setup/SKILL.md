---
name: studio-test-setup
description: Codex-native test infrastructure setup workflow for the selected engine
---

# Studio Test Setup

Use this to scaffold or validate test infrastructure for the chosen engine.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-test-setup/SKILL.md`
4. `docs/studio/technical-preferences.md`
5. Existing `tests/` and `.github/workflows/` state

## Workflow

1. Detect the configured engine and current test infrastructure.
2. Stop only if the engine is still unconfigured.
3. Otherwise create missing, engine-appropriate test scaffolding and CI artifacts without overwriting existing good files unnecessarily.
4. Document what was created and what remains manual.

## Codex Adaptation Rules

- Do not block on Claude-style confirmation prompts for straightforward scaffolding.
- Prefer additive creation over destructive replacement.
- Keep the result aligned with the engine choice in `docs/studio/technical-preferences.md`.

## Handoff

Recommend the next step, usually `$studio-qa-plan`, `$studio-dev-story`, or focused engine setup work.

## Completion

Complete when the required test directories/config are in place or the missing prerequisite is clearly stated.
