---
name: studio-design-system
description: Codex-native GDD authoring workflow for a single game system
---

# Studio Design System

Use this to author or retrofit one system GDD under `design/gdd/`.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/design-system/SKILL.md`
4. `design/gdd/game-concept.md`
5. `design/gdd/systems-index.md`
6. Related GDDs for dependencies when relevant

## Goal

Create or complete a system design doc with enough specificity that downstream architecture and story work can rely on it.

## Workflow

1. Resolve the target system from the user request or from the systems index.
2. Detect retrofit mode when the target file already exists.
3. Read existing content first and preserve good sections instead of rewriting them.
4. Ensure the resulting system doc covers at least:
   - overview
   - player fantasy
   - detailed rules
   - formulas/data model
   - edge cases
   - dependencies
   - tuning knobs
   - acceptance criteria
5. Ask only for missing design decisions that cannot be inferred from existing docs.
6. Write or update `design/gdd/<system>.md`.

## Codex Adaptation Rules

- Do not preserve upstream “ask before edit” gates.
- Do not mimic multi-tab `AskUserQuestion`; use concise text questions only for true design branches.
- Prefer incremental retrofits over wholesale replacement when a partial GDD already exists.

## Handoff

Recommend the next best step, usually `$studio-review-all-gdds`, `$studio-create-architecture`, or another `$studio-design-system` for the next system.

## Completion

Complete when the target GDD exists and is materially more implementation-ready than before.
