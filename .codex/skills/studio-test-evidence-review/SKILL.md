---
name: studio-test-evidence-review
description: Codex-native review of automated test quality and manual evidence completeness
---

# Studio Test Evidence Review

Use this to judge whether story-level test files and manual evidence are actually good enough, not merely present.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/test-evidence-review/SKILL.md`
4. In-scope stories
5. Referenced test files and manual evidence artifacts
6. Related QA evidence directories under `production/qa/`

## Goal

Produce an evidence-quality review with per-story verdicts (`ADEQUATE`, `INCOMPLETE`, `MISSING`) and clear blocking vs advisory issues.

## Workflow

1. Resolve scope:
   - single story
   - current sprint
   - system or epic
2. Load the stories in scope and extract:
   - story type
   - acceptance criteria
   - declared test evidence
3. Locate the actual evidence:
   - unit tests
   - integration tests
   - manual evidence docs
   - smoke artifacts
4. Review automated tests for quality:
   - assertion coverage
   - edge-case coverage
   - naming quality
   - formula traceability when relevant
5. Review manual evidence for quality:
   - criterion linkage
   - required sign-offs
   - attached artefacts
   - freshness relative to implementation
6. Produce a review report with:
   - per-story verdicts
   - blocking issues
   - advisory issues
   - overall scope verdict
7. Optionally write a persistent evidence-review report under `production/qa/`.

## Codex Adaptation Rules

- Review quality; do not silently edit tests or evidence in this workflow.
- `ADEQUATE` means ship-worthy confidence, not perfect polish.
- Reserve blocking findings for genuinely unverified acceptance criteria or missing required sign-offs.
- Prefer direct file-backed evidence over test-file existence alone.
- Recommend the exact next verification or fix workflow when evidence is weak.

## Handoff

Recommend the next step, usually `$studio-team-qa`, `$studio-story-done`, or a focused test/evidence repair pass.

## Completion

Complete when the evidence review is clearly reported and the user has an explicit adequacy verdict for the scope.
