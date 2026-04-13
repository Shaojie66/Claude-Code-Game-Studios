---
name: studio-regression-suite
description: Codex-native workflow for maintaining the regression test manifest and spotting coverage drift
---

# Studio Regression Suite

Use this after bug fixes, before gates, or at sprint close to keep the regression suite honest and current.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-regression-suite/SKILL.md`
4. Existing tests under `tests/`
5. `tests/regression-suite.md` if present
6. Relevant GDDs, stories, and closed bug reports

## Goal

Write or refresh `tests/regression-suite.md` so the project has a curated registry of tests covering critical paths, bug regressions, and newly introduced coverage gaps.

## Workflow

1. Resolve mode:
   - `update`
   - `audit`
   - `report`
2. Load the current regression-suite manifest if it exists.
3. Inventory test files and relevant story/bug context:
   - unit tests
   - integration tests
   - regression-specific tests
   - closed bugs
   - critical-path GDD acceptance criteria or current sprint scope
4. Map coverage:
   - critical path coverage
   - fixed bugs without regression tests
   - drift from new systems or stories
5. Produce a report summarizing:
   - covered paths
   - partial coverage
   - missing regression tests
   - stale or quarantined tests
6. In write modes, update `tests/regression-suite.md` with registered tests, known gaps, and quarantine notes.

## Codex Adaptation Rules

- Treat the regression suite as a registry of existing tests, not a place to invent fake coverage.
- Never silently remove registered regression tests from the manifest.
- Distinguish advisory gaps from actual release blockers.
- Prefer repo evidence over assumptions about what a test probably covers.
- Recommend test-scaffolding or flakiness workflows when gaps are found, rather than trying to fix them here.

## Handoff

Recommend the next step, usually `$studio-test-evidence-review`, `$studio-gate-check`, or a focused test-writing pass.

## Completion

Complete when the regression-suite report is grounded and, in write modes, `tests/regression-suite.md` is updated with current coverage status.
