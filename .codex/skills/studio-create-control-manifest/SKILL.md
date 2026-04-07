---
name: studio-create-control-manifest
description: Codex-native workflow for extracting programmer rules from accepted ADRs and engine guidance
---

# Studio Create Control Manifest

Use this after architecture review to produce the flat programmer rule sheet derived from accepted ADRs, technical preferences, and engine guidance.

## Read First

1. `AGENTS.md`
2. `docs/codex-port.md`
3. `.claude/skills/create-control-manifest/SKILL.md`
4. Accepted ADRs under `docs/architecture/`
5. `.claude/docs/technical-preferences.md`
6. Engine reference docs under `docs/engine-reference/<engine>/`

## Goal

Write or refresh `docs/architecture/control-manifest.md` so story authors and implementers have a concise, source-backed rules sheet for what to do and what not to do.

## Workflow

1. Load accepted ADRs only and collect their governing rules by layer:
   - required patterns
   - forbidden approaches
   - performance guardrails
   - engine API constraints
2. Merge in cross-cutting rules from technical preferences:
   - naming conventions
   - approved libraries
   - forbidden patterns
   - performance budgets
3. Merge engine-level constraints from:
   - deprecated APIs
   - current best practices
   - pinned engine/version notes
4. Classify rules by architecture layer:
   - `Foundation`
   - `Core`
   - `Feature`
   - `Presentation`
   - `Global`
5. Write `docs/architecture/control-manifest.md` with source references and manifest metadata.
6. If the manifest already exists, regenerate it from current accepted inputs instead of hand-editing stale rules.

## Codex Adaptation Rules

- Source every rule from an accepted ADR, technical preference, or engine reference document.
- Keep the manifest actionable and flat; do not repeat long ADR rationale.
- Never treat proposed ADRs as binding rules.
- When review or engine evidence is missing, flag the manifest as incomplete rather than filling gaps from intuition.
- Keep the output aligned with story creation and readiness workflows.

## Handoff

Recommend the next step, usually `$studio-create-stories`, `$studio-story-readiness`, or a manifest refresh after new ADRs are accepted.

## Completion

Complete when `docs/architecture/control-manifest.md` exists or is refreshed from current accepted sources and is ready for story and implementation use.
