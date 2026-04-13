---
name: studio-code-review
description: Codex-native review workflow for implementation changes in the game studio template
---

# Studio Code Review

Use this for architectural and quality review of a changed file set or story implementation.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-code-review/SKILL.md`
4. Relevant story, ADR, or GDD files when the change is tied to them

## Workflow

1. Resolve the review target from explicit file paths, current diff, or session-state context.
2. Read the changed files, not just summaries.
3. Cross-check against:
   - governing story acceptance criteria if present
   - ADR constraints if present
   - control-manifest expectations if present
4. Review for:
   - correctness
   - scope drift
   - maintainability
   - missing tests or evidence
   - violations of design or architecture intent
5. Produce a concise review verdict with concrete findings and exact file references.

## Codex Adaptation Rules

- Prefer direct Codex review output or `::code-comment` findings when needed.
- Do not recreate legacy approval choreography.
- Report “no issues found” explicitly when the change is sound.

## Handoff

Recommend the next command, usually `$studio-story-done` or a focused fix pass.

## Completion

Complete when the user has an actionable review verdict grounded in the actual changed files.
