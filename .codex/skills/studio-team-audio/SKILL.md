---
name: studio-team-audio
description: Codex-native team workflow for team audio in the game studio template
---

# Studio Team Audio

Use this when the user wants to run the team audio workflow as a coordinated Codex-native team pass.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.codex/skills/studio-team-audio/SKILL.md`
4. In-scope stories, feature specs, or sprint artifacts plus the relevant design, code, and QA evidence

## Goal

Produce a coordinated team audio package with clear lanes, concrete outputs, blockers, and a grounded handoff.

## Workflow

1. Resolve scope from the explicit story, feature, sprint, or active repo context.
2. Read the minimal set of in-scope artifacts needed to understand objectives, constraints, and current blockers.
3. Split the work into explicit lanes with owners, expected outputs, and verification checks before starting any parallel work.
4. Use Codex-native subagents only for bounded parallel lanes where it materially improves throughput.
5. Consolidate outputs into repo artifacts or a decision package with statuses, unresolved blockers, and next-step guidance.
6. End with a concrete verdict for the selected scope: ready to proceed, ready with conditions, or blocked.

## Codex Adaptation Rules

- Do not recreate legacy approval-heavy choreography; use evidence-backed checkpoints instead.
- Do not open parallel lanes until the scope and success criteria are explicit.
- Prefer repo artifacts and exact references over broad narrative summaries.

## Handoff

Recommend the next step, usually `$studio-dev-story`, `$studio-team-qa`, `$studio-story-done`, or a focused fix pass.

## Completion

Complete when the selected scope has a coordinated output package or verdict that another Codex workflow can act on immediately.
