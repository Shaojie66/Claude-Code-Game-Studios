# Legacy Studio Reference

This file is preserved from the upstream template as historical context only.
In this fork, use [AGENTS.md](AGENTS.md) as the active entrypoint, generated
prompts under `.codex/prompts/studio-*.md` for studio roles, and
`.codex/skills/studio-*/SKILL.md` for workflow execution.

The project now runs through Codex and OMX surfaces; do not treat this file as
the runtime authority.

## Technology Stack

- **Engine**: [CHOOSE: Godot 4 / Unity / Unreal Engine 5]
- **Language**: [CHOOSE: GDScript / C# / C++ / Blueprint]
- **Version Control**: Git with trunk-based development
- **Build System**: [SPECIFY after choosing engine]
- **Asset Pipeline**: [SPECIFY after choosing engine]

> **Note**: Engine-specialist agents exist for Godot, Unity, and Unreal with
> dedicated sub-specialists. Use the set matching your engine.

## Project Structure

@docs/studio/directory-structure.md

## Engine Version Reference

@docs/engine-reference/godot/VERSION.md

## Technical Preferences

@docs/studio/technical-preferences.md

## Coordination Rules

@docs/studio/coordination-rules.md

## Collaboration Protocol

This file preserves upstream collaboration context only. The active
collaboration contract is defined by `AGENTS.md` and Codex runtime behavior.

> **First session?** In this fork, use `$game-studio` and
> `.codex/skills/studio-start/SKILL.md` as the onboarding playbook.

## Coding Standards

@docs/studio/coding-standards.md

## Context Management

@docs/studio/context-management.md
