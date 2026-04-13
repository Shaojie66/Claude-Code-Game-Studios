---
name: studio-architecture-review
description: Codex-native architecture audit for coverage, consistency, engine fit, and traceability
---

# Studio Architecture Review

Use this to validate whether the architecture body actually covers the GDDs, stays internally consistent, and targets the pinned engine correctly.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-architecture-review/SKILL.md`
4. In-scope GDDs under `design/gdd/`
5. ADRs and architecture files under `docs/architecture/`
6. Engine reference docs under `docs/engine-reference/<engine>/`
7. `docs/studio/technical-preferences.md`

## Goal

Produce an architecture review result with a clear `PASS`, `CONCERNS`, or `FAIL` verdict backed by requirement coverage, conflict detection, and engine compatibility evidence.

## Workflow

1. Resolve scope from:
   - `full`
   - `coverage`
   - `consistency`
   - `engine`
   - `single-gdd <path>`
   - `rtm`
2. Load only the documents needed for the requested mode, but fully read all in-scope GDDs and ADRs before concluding.
3. Extract or reuse technical requirements from the GDDs and map them to ADR coverage:
   - `covered`
   - `partial`
   - `gap`
4. Detect cross-ADR conflicts:
   - ownership conflicts
   - interface contradictions
   - dependency cycles
   - budget or initialization conflicts
5. Audit engine compatibility across architecture artifacts:
   - version consistency
   - deprecated API references
   - stale or missing engine compatibility sections
   - post-cutoff API assumptions
6. In `rtm` mode, extend the traceability chain to stories and tests when those artifacts exist.
7. Write a review artifact under `docs/architecture/` that names findings, unresolved gaps, and the final gate verdict.

## Codex Adaptation Rules

- Prefer evidence tables and written review artifacts over interactive Claude review choreography.
- Do not mark architecture healthy when gaps, contradictions, or engine blind spots remain unresolved.
- Reuse existing TR registries or traceability docs when present instead of renumbering requirements casually.
- Treat engine-reference docs as the source of truth for post-cutoff behavior.
- Recommend concrete next actions like `$studio-architecture-decision` or `$studio-create-control-manifest` based on the verdict.

## Handoff

Recommend the next step, usually `$studio-architecture-decision`, `$studio-create-control-manifest`, or a focused fix pass before story planning proceeds.

## Completion

Complete when the review artifact exists, findings are traceable to repo evidence, and the user has a clear architecture gate verdict.
