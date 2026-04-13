---
name: studio-propagate-design-change
description: Codex-native workflow for tracing a GDD revision into affected ADRs and architecture artifacts
---

# Studio Propagate Design Change

Use this when a GDD changed and you need to find which architecture decisions or traceability artifacts may now be stale.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-propagate-design-change/SKILL.md`
4. The changed GDD under `design/gdd/`
5. ADRs and traceability files under `docs/architecture/`
6. Git history for the changed GDD

## Goal

Write a change-impact report that compares the current GDD with its previous committed version, identifies affected ADRs, and recommends whether each decision stays valid, needs review, or is likely superseded.

## Workflow

1. Require a concrete changed GDD path and verify it exists.
2. Read the current GDD and load the previous committed revision from git.
3. Produce a conceptual change summary:
   - changed sections
   - unchanged sections
   - architecture-relevant deltas
4. Load all ADRs plus any architecture traceability index that references the changed GDD.
5. For each impacted ADR, compare what it assumed against the current GDD and classify it as:
   - `Still Valid`
   - `Needs Review`
   - `Likely Superseded`
6. Write a change-impact report under `docs/architecture/` and list recommended follow-up actions for each affected ADR.
7. If traceability artifacts exist, update or flag them consistently with the impact report.

## Codex Adaptation Rules

- Prefer a written impact report over Claude-style multi-step approval choreography.
- Treat missing git history as a real “new file, not a revision” case and stop cleanly.
- Keep the workflow non-destructive: do not rewrite ADR content unless the task explicitly includes the follow-up edit.
- Surface cascading architecture risk clearly when many ADRs reference the changed GDD.
- Recommend concrete next actions like `$studio-architecture-decision` or `$studio-architecture-review` based on impact severity.

## Handoff

Recommend the next step, usually `$studio-architecture-decision`, `$studio-architecture-review`, or a focused ADR update pass.

## Completion

Complete when the change-impact report exists and the affected architecture decisions have a clear follow-up classification.
