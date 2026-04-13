---
name: studio-scope-check
description: Codex-native review workflow for scope check in the game studio template
---

# Studio Scope Check

Use this when the user wants a grounded scope check pass over a story, feature, system, or release scope.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-scope-check/SKILL.md`
4. In-scope design docs, code, data, ADRs, QA evidence, or release artifacts relevant to the review target

## Goal

Produce an evidence-backed scope check verdict with exact findings, risks, and recommended follow-up actions.

## Workflow

1. Resolve the review target from explicit paths, current diff, active sprint/story context, or the user request.
2. Read the in-scope artifacts fully rather than relying on summaries.
3. Evaluate the target against the workflow-specific concerns, governing GDDs, ADRs, manifests, and test evidence when present.
4. Record findings with exact file references or artifact references, separating blocking issues from advisories.
5. If the workflow naturally produces a report artifact, write or update it in the repo; otherwise return a concise review verdict grounded in the files you read.
6. Recommend the narrowest next step that resolves the highest-signal issue or advances the validated work.

## Codex Adaptation Rules

- Do not invent findings; report `no issues found` explicitly when the target is sound.
- Flag missing evidence, missing formulas, or missing traceability instead of guessing.
- Keep the review scoped to the selected target unless correctness requires widening it.

## Handoff

Recommend the next step, usually a focused fix pass, `$studio-dev-story`, `$studio-gate-check`, or another validation workflow.

## Completion

Complete when the user has an actionable review artifact or verdict with concrete findings and next actions.
