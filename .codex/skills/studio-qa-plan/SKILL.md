---
name: studio-qa-plan
description: Codex-native workflow for generating QA plans for stories, features, or sprints
---

# Studio QA Plan

Use this before implementation or QA handoff to turn stories into a concrete test plan.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-qa-plan/SKILL.md`
4. In-scope story files plus referenced GDD sections and formulas

## Goal

Generate a QA plan that tells the team what to automate, what to verify manually, and what evidence is required.

## Workflow

1. Resolve scope from:
   - `sprint`
   - `feature:<name>`
   - `story:<path>`
2. Load full story files plus the minimal supporting GDD/manifest context needed for testing.
3. Classify stories by primary test type:
   - `Logic`
   - `Integration`
   - `Visual/Feel`
   - `UI`
   - `Config/Data`
4. Write a QA plan under `production/qa/` covering:
   - automated tests required
   - manual checks
   - smoke scope
   - playtest/sign-off requirements

## Codex Adaptation Rules

- Do not preserve legacy approval choreography.
- Prefer concrete evidence paths and test file expectations over generic QA advice.
- Flag missing GDD formulas or traceability gaps instead of inventing tests.

## Handoff

Recommend the next step, usually `$studio-smoke-check`, `$studio-dev-story`, or `$studio-story-done` depending on timing.

## Completion

Complete when the QA plan file exists and gives the team a concrete testing contract for the selected scope.
