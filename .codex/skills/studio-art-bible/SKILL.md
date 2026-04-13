---
name: studio-art-bible
description: Codex-native workflow for art bible in the game studio template
---

# Studio Art Bible

Use this when the user wants to run the art bible workflow in Codex terms and leave behind a concrete artifact, verdict, or next-step package.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-art-bible/SKILL.md`
4. The in-scope design docs, content assets, QA evidence, production files, or implementation context required by the selected workflow

## Goal

Produce a Codex-native art bible outcome that is explicit, repo-grounded, and ready for downstream workflows.

## Workflow

1. Resolve the target scope, artifact, and expected output from the user request and current repo context.
2. Read the minimal supporting design, production, QA, or implementation artifacts needed to do the work safely.
3. Identify missing prerequisites or dependency gaps before drafting or changing anything.
4. Create or update the primary artifact, report, or decision package in the appropriate repository area.
5. Surface downstream dependencies, verification needs, and follow-up workflows explicitly.
6. Finish with the narrowest next action that keeps the workflow moving.

## Codex Adaptation Rules

- Ask only brief confirm-or-correct questions when a branching decision cannot be inferred from repo evidence.
- Prefer writing or updating repo artifacts over leaving the result only in chat.
- Keep the output anchored to the selected scope; do not broaden into unrelated redesign work.

## Handoff

Recommend the next step, usually another `$studio-*` workflow that consumes the artifact or verdict you just produced.

## Completion

Complete when the selected workflow leaves behind a concrete artifact, report, or decision package that is ready for downstream use.
