---
name: studio-create-stories
description: Codex-native workflow for breaking an epic into implementation stories
---

# Studio Create Stories

Use this to decompose one epic into story files that are ready for `$studio-story-readiness`.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/create-stories/SKILL.md`
4. The target `production/epics/<epic>/EPIC.md`
5. Linked GDD, ADRs, control manifest, and TR registry

## Goal

Produce implementation-sized stories with explicit traceability, test expectations, and dependency order.

## Workflow

1. Resolve the target epic from an explicit slug/path or by scanning `production/epics/*/EPIC.md`.
2. Validate that referenced ADR files actually exist before story generation.
3. Load the epic, source GDD, governing ADRs, control manifest, and TR registry.
4. Break the epic into story-sized units by:
   - grouping related acceptance criteria
   - preserving dependency order
   - assigning a story type (`Logic`, `Integration`, `Visual/Feel`, `UI`, `Config/Data`)
   - attaching a concrete test-evidence path
5. Write story files under `production/epics/<epic>/` and update the epic story table in `EPIC.md`.

## Codex Adaptation Rules

- Do not preserve Claude approval choreography.
- Prefer direct file generation once the epic decomposition is clear.
- Keep stories small enough for one focused implementation pass.
- Make story files concrete enough that `$studio-story-readiness` can judge them without guesswork.

## Handoff

Recommend the next step, usually `$studio-story-readiness <story>` or `$studio-sprint-plan new`.

## Completion

Complete when the epic has concrete story files plus an updated story table in its `EPIC.md`.
