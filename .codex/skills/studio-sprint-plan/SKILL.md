---
name: studio-sprint-plan
description: Codex-native workflow for creating or updating sprint plans
---

# Studio Sprint Plan

Use this to create, update, or report sprint planning artifacts in `production/`.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/sprint-plan/SKILL.md`
4. Existing milestone, sprint, risk-register, and story backlog files

## Goal

Generate a practical sprint plan and matching `production/sprint-status.yaml` that downstream workflows can trust.

## Workflow

1. Resolve mode:
   - `new`
   - `update`
   - `status`
2. Gather context from:
   - `production/milestones/`
   - previous sprint files
   - available story backlog under `production/epics/`
   - `production/risk-register/` if present
3. For `new` or `update`, produce:
   - sprint goal
   - must/should/nice buckets
   - carryover
   - risks
   - definition of done
4. Write:
   - `production/sprints/sprint-<N>.md`
   - `production/sprint-status.yaml`
5. For `status`, summarize progress from the latest sprint artifacts instead of rewriting the plan.

## Codex Adaptation Rules

- Do not block on Claude-style review prompts for straightforward plan generation.
- Prefer explicit backlog and status artifacts that other Codex workflows can read directly.
- Keep the QA-plan dependency visible; do not hide missing QA planning.

## Handoff

Recommend the next step, usually `$studio-qa-plan`, `$studio-story-readiness <story>`, or `$studio-dev-story <story>`.

## Completion

Complete when the sprint plan and machine-readable status file are in sync, or when the sprint status report is clearly produced.
