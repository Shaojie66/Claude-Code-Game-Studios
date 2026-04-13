---
name: studio-create-epics
description: Codex-native workflow for translating GDD and architecture into epic files
---

# Studio Create Epics

Use this to create bounded epic definitions from approved GDD and architecture material.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-create-epics/SKILL.md`
4. `design/gdd/systems-index.md`
5. Relevant GDDs, architecture docs, ADRs, control manifest, and TR registry

## Goal

Produce epic-level scope documents that map systems to architectural modules without jumping ahead into story decomposition.

## Workflow

1. Resolve scope from:
   - one system
   - one layer
   - `all`
2. Load only the in-scope GDDs and matching architecture/ADR material.
3. For each system, define:
   - architectural module ownership
   - governing ADRs
   - engine risk
   - traced vs untraced requirements
4. Write:
   - `production/epics/<epic>/EPIC.md`
   - `production/epics/index.md`

## Codex Adaptation Rules

- Do not preserve legacy approval choreography.
- Warn clearly when requirements are untraced or ADR coverage is missing.
- Stop at epic scope; do not also create stories in this workflow.

## Handoff

Recommend the next step, usually `$studio-create-stories <epic>` or `$studio-architecture-decision` when epic coverage gaps remain.

## Completion

Complete when in-scope epics exist with clear scope, ADR mapping, and next-step handoff.
