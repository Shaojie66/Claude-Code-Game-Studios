---
name: studio-story-done
description: Codex-native story closure and verification workflow
---

# Studio Story Done

Use this to close a story after implementation and review.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-story-done/SKILL.md`
4. The target story file
5. Any linked TR/ADR/context needed to verify closure

## Workflow

1. Resolve the story from the argument or session-state context.
2. Read the story acceptance criteria and referenced implementation files.
3. Verify completion using direct evidence:
   - file existence
   - current code shape
   - test presence for logic/integration stories
   - review status or outstanding findings
4. If evidence is incomplete, report what is missing instead of marking the story done.
5. If closure is justified, update the story status and note the result in `production/session-state/active.md`.

## Codex Adaptation Rules

- Do not use Claude-style question trees unless a real ambiguity blocks closure.
- Prefer evidence-backed closure over ceremony.
- Do not mark a story complete when review or required test evidence is still missing.

## Handoff

Recommend the next story or the next pipeline step after closure.

## Completion

Complete when the story status is accurately updated and the user has a clear next move.
