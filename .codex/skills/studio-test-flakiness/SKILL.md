---
name: studio-test-flakiness
description: Codex-native workflow for detecting flaky tests and updating quarantine guidance
---

# Studio Test Flakiness

Use this when CI failures start looking intermittent or when quarantined tests need diagnosis.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/test-flakiness/SKILL.md`
4. Available CI logs or test result artifacts
5. `tests/regression-suite.md` if present
6. Relevant test files under `tests/`

## Goal

Detect confirmed or suspected flaky tests, classify likely causes, and update the project’s quarantine/reporting artifacts with concrete remediation guidance.

## Workflow

1. Resolve mode:
   - specific CI log path
   - `scan`
   - `registry`
2. Locate and load test-result history from CI logs, XML results, or existing registry state.
3. Parse pass/fail outcomes per test across runs.
4. Classify flakiness:
   - high
   - moderate
   - suspected
5. Inspect the implicated test files for likely causes:
   - timing or async issues
   - order dependency
   - RNG usage
   - resource leaks
   - external state coupling
   - float comparison problems
6. Produce a flakiness summary and, when approved, update:
   - quarantine entries in `tests/regression-suite.md`
   - a persistent flakiness report under `production/qa/`

## Codex Adaptation Rules

- Treat fewer than three runs as weak evidence; prefer `suspected` over `confirmed` in that case.
- Never delete tests in this workflow; quarantine is a tracking decision, not a removal.
- Always recommend a likely fix direction even when quarantine is advised.
- Prefer actual run history over anecdotal “probably flaky” claims.
- Keep quarantine updates explicit and source-backed.

## Handoff

Recommend the next step, usually a targeted test fix, `$studio-regression-suite`, or `$studio-gate-check` after flaky tests are controlled.

## Completion

Complete when the flakiness findings are clearly reported and any approved quarantine/report artifacts are updated.
