---
name: game-studio
description: Codex-native router for the game-studio workflow assets in this repository
---

# Game Studio Router

Use this skill when the user wants to work with the studio framework in this repository through the Codex-native surfaces.

## Intent

This repository keeps the upstream studio knowledge base, but the active runtime lives in the Codex-native prompts and skills in this repo.
Your job is to route the user's request to the concrete Codex/OMX surfaces that now own execution.

## Sources Of Truth

Read these files as needed:

1. `AGENTS.md` for the top-level Codex operating contract
2. `docs/codex-port.md` for the fork-specific compatibility rules
3. `docs/codex-agent-catalog.md` for the upstream-agent to Codex-prompt mapping
4. `docs/studio/skills-reference.md` for the original workflow catalog
5. `.codex/skills/studio-<name>/SKILL.md` only when the user needs the details of a specific original workflow

## How To Route Work

1. Prefer Codex-native execution.
2. Use `/prompts:studio-...` when the task benefits from a specific studio role.
3. Treat `.codex/skills/studio-*` as the maintained workflow contracts behind the `$studio-*` surfaces.
4. When an upstream skill depends on `ask_user_dictation`, replace it with concise plain-text questions or proceed autonomously when the answer is obvious and low-risk.
5. Preserve upstream docs and assets unless the task specifically requires changing them.

## Quick Mapping

- Strategic direction or creative conflicts: use `/prompts:studio-creative-director`
- Technical planning or architecture: use `/prompts:studio-technical-director` or `/prompts:studio-lead-programmer`
- Feature implementation: use Codex directly, optionally with `/prompts:studio-gameplay-programmer`, `/prompts:studio-ui-programmer`, or engine specialists
- QA, release, and readiness checks: use `/prompts:studio-qa-lead`, `/prompts:studio-qa-tester`, or `/prompts:studio-release-manager`

## Deliverable Standard

When you rely on Codex-native workflow docs, cite which doc you used and translate the result into concrete Codex actions, file changes, or a concise plan.
