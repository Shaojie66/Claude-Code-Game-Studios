---
name: studio-setup-engine
description: Codex-native engine selection and configuration workflow for the game studio template
---

# Studio Setup Engine

Use this to choose and configure Godot, Unity, or Unreal for the project.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-setup-engine/SKILL.md`
4. `docs/studio/technical-preferences.md`
5. `design/gdd/game-concept.md` if present

## Goal

Move the project from unconfigured or ambiguous engine state to an explicit engine choice documented in repo files.

## Workflow

1. Detect whether an engine is already configured.
2. If configured, validate whether the current choice still matches the concept and user intent.
3. If not configured, recommend an engine based on:
   - project scope
   - target platform
   - team experience
   - concept needs
4. Ask only for missing preference signals that materially affect the engine choice.
5. Update `docs/studio/technical-preferences.md` with the chosen engine and associated language/tooling details.
6. Point to engine-specific specialists or next setup steps.

## Codex Adaptation Rules

- Replace long interactive Claude questionnaires with a compact recommendation plus 1-3 decisive questions at most.
- Write the engine configuration directly once the choice is clear.
- Prefer concrete downstream recommendations like `$studio-test-setup` and engine specialist prompts.

## Completion

Complete when the engine choice is explicit in repo docs and the user has the next setup step.
