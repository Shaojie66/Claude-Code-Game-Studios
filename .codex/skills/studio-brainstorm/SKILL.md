---
name: studio-brainstorm
description: Codex-native concept ideation workflow for the game studio template
---

# Studio Brainstorm

Use this to go from no idea or a vague theme to a concrete game concept artifact.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-brainstorm/SKILL.md`
4. Existing concept docs in `design/gdd/` if they already exist

## Goal

Produce or advance concept direction without forcing legacy multi-step approval choreography.

## Workflow

1. Inspect whether `design/gdd/game-concept.md` or `design/gdd/game-pillars.md` already exists.
2. If concept docs exist, resume and refine instead of restarting ideation from zero.
3. If the user provided a hint, use it; otherwise guide from open exploration.
4. Ask only the minimum high-value plain-language questions needed to shape:
   - target fantasy
   - emotional experience
   - scope/timeline
   - rough genre or mechanic direction
5. Synthesize 2-3 viable concept directions with tradeoffs, then recommend one.
6. Write or update:
   - `design/gdd/game-concept.md`
   - `design/gdd/game-pillars.md` when the concept is concrete enough

## Codex Adaptation Rules

- Replace `ask_user_dictation` with concise conversational questions.
- Do not over-interview if enough direction already exists in repo files or user input.
- Prefer creating durable concept artifacts over leaving the result only in chat.

## Handoff

Recommend the next best follow-up, usually `$studio-setup-engine`, `$studio-map-systems`, or `$studio-design-review`.

## Completion

Complete when the concept has been materially advanced in repo artifacts and the user has one clear next step.
