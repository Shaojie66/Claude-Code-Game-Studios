---
name: studio-story-readiness
description: Codex-native readiness check for implementation stories
---

# Studio Story Readiness

Use this before implementation to decide whether a story is actually ready to hand to `$studio-dev-story`.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/story-readiness/SKILL.md`
4. The target story file or story set
5. Supporting references such as TR registry, ADRs, control manifest, and sprint file when relevant

## Goal

Return a clear verdict for each story:

- `READY`
- `NEEDS WORK`
- `BLOCKED`

## Workflow

1. Resolve scope from:
   - a specific story path
   - `sprint`
   - `all`
   - active session-state context when no argument is given
2. Load shared supporting context once:
   - `design/gdd/systems-index.md`
   - `docs/architecture/control-manifest.md` if present
   - `docs/architecture/tr-registry.yaml` if present
   - referenced ADR statuses
3. For each story, check:
   - specific GDD requirement traceability
   - testable acceptance criteria
   - ADR/TR/manifest completeness
   - dependencies and blocker state
   - asset reference existence when assets are named
   - story type and test-evidence expectations
4. Produce a concise per-story gap list with exact fixes.

## Codex Adaptation Rules

- Keep this workflow read-only.
- Do not simulate Claude `AskUserQuestion`; if scope is ambiguous, infer from repo state or ask one short question.
- Prefer evidence-backed verdicts over checklist theater.

## Handoff

- If `READY` → recommend `$studio-dev-story`
- If `NEEDS WORK` → recommend the specific doc/setup workflow that closes the gap
- If `BLOCKED` → name the blocking dependency or missing architecture artifact

## Completion

Complete when the user has explicit verdicts and concrete fixes or next actions for the evaluated stories.
