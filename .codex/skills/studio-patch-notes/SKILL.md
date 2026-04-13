---
name: studio-patch-notes
description: Codex-native production workflow for patch notes in the game studio template
---

# Studio Patch Notes

Use this when the user wants the patch notes workflow to produce a concrete operational artifact or decision.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-patch-notes/SKILL.md`
4. Relevant production artifacts, QA evidence, release notes, sprint files, design docs, and implementation context for the selected scope

## Goal

Produce a concrete patch notes artifact or verdict that reflects the current repo state, dependencies, and open risks.

## Workflow

1. Resolve the selected scope, timeframe, or target artifact from the user request and repo state.
2. Gather the minimum supporting evidence from production files, QA outputs, implementation artifacts, and design/architecture context.
3. Draft or update the primary artifact in the appropriate repo location with explicit statuses, assumptions, and dependencies.
4. Surface blockers, missing evidence, and unresolved cross-team dependencies instead of smoothing them over.
5. Cross-check the output against any linked stories, release criteria, QA results, or architectural constraints.
6. End with a concise recommendation for the next workflow or escalation path.

## Codex Adaptation Rules

- Prefer concrete dates, statuses, and evidence paths over narrative filler.
- Do not invent progress, approvals, or test coverage that the repo does not support.
- When the workflow is report-oriented, write the report artifact instead of only summarizing it in chat.

## Handoff

Recommend the next step, usually `$studio-sprint-status`, `$studio-story-done`, `$studio-release-checklist`, `$studio-launch-checklist`, or a focused bug/fix workflow.

## Completion

Complete when the selected production artifact or verdict exists in the repo and accurately reflects the current state of the scoped work.
