---
name: studio-design-review
description: Codex-native single-GDD review for completeness, implementability, and design fit
---

# Studio Design Review

Use this before handing one design document to architecture or implementation work.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/design-review/SKILL.md`
4. The target GDD
5. `CLAUDE.md`
6. Related GDDs, concept docs, and narrative context if referenced
7. Prior review logs for the target GDD if present

## Goal

Review a single design document for completeness, internal consistency, implementability, and alignment with the project’s pillars and related systems.

## Workflow

1. Resolve the target design document path and review depth:
   - `full`
   - `lean`
   - `solo`
2. Read the document completely, plus directly related context and prior review history.
3. Check structural completeness:
   - overview
   - player fantasy
   - rules
   - formulas
   - edge cases
   - dependencies
   - tuning knobs
   - acceptance criteria
4. Review implementability and consistency:
   - precise rules vs hand-waving
   - formula/rule agreement
   - dependency validity
   - cross-system conflicts
   - pillar or lore contradictions
5. In deeper review modes, bring in specialist criticism only when it materially sharpens the verdict.
6. Produce a written review result with:
   - blockers before implementation
   - recommended revisions
   - scope signal
   - final verdict
7. If requested, update review logs or adjacent tracking files after the review is grounded.

## Codex Adaptation Rules

- Prefer evidence-backed review output over heavy interactive decision trees.
- Keep specialist delegation bounded and useful; do not simulate specialist opinions when actual review is needed.
- Treat broken dependency references and vague acceptance criteria as real blockers.
- Distinguish blocking implementation gaps from optional polish.
- Recommend `$studio-review-all-gdds` or `$studio-propagate-design-change` when the issue is wider than one document.

## Handoff

Recommend the next step, usually a GDD revision pass, `$studio-review-all-gdds`, or `$studio-create-architecture` if the document is ready.

## Completion

Complete when the review findings are written or clearly reported and the user has an explicit approval/revision verdict for the target GDD.
