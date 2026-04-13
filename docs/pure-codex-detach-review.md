# Pure Codex Detach Review

This review complements `docs/pure-codex-detach-audit.md` with a human-readable summary of what changed to finish the Codex migration and what remains intentionally archived-only.

## Current Readiness Snapshot

As of the current branch state:

- The active detach gate is passing: prompt sources, generated prompts, and skill counts all match expectations, and active legacy runtime-marker references are gone from the audited scope.
- The prompt layer is generated from `.codex/prompt-sources/studio/` through the Codex-native generator path.
- The full `studio-*` skill surface is now authored as Codex-native workflow definitions rather than bridge wrappers.
- Active docs now describe the repo as a Codex-native maintenance model, while archived upstream material remains reference-only.
- The prompt source tree under `.codex/prompt-sources/studio/` is already canonical for generated prompts.

## What Changed

### 1. Status documents were brought back in sync

`docs/pure-codex-detach-audit.md`, `README.md`, `docs/codex-port.md`, and related active docs were updated so the checked-in maintenance story matches the actual runtime state.

### 2. Skill wrappers were replaced with native workflow contracts

The remaining `studio-*` bridge wrappers were rewritten into self-contained Codex-native workflow definitions. The active skill surface no longer depends on bridge wording or self-referential wrapper structure.

### 3. Generator ownership is now Codex-native in active surfaces

The prompt/catalog generator now uses a Codex-native tool name and emits native comments in generated prompts and the agent catalog, so the maintenance path is consistent from source to output.

### 4. Archived upstream material remains intentionally non-active

Historical upstream material may still exist under archived or reference-only locations. That content is no longer part of the active runtime contract.

## Maintenance Model

1. Prompts and the agent catalog are generated from `.codex/prompt-sources/studio/`.
2. `.codex/skills/studio-*/SKILL.md` files are the maintained Codex-native workflow source of truth.
3. Archived upstream content is reference-only and should not be treated as active runtime input.
4. `docs/pure-codex-detach-audit.md` is the quick integrity check for the active detach gate.

## Completed Exit Evidence

The current branch state now includes all of the following:

- `49` prompt sources under `.codex/prompt-sources/studio/`
- `49` generated `studio-*` prompts sourced only from the prompt-source tree
- `72` Codex-native studio skills with no bridge/self-referential wrapper structure in active files
- Zero active legacy runtime-marker hits in the audited scope
- Zero active legacy generator-name references in prompts, docs, scripts, and tools
- A documented maintenance flow that distinguishes generated prompts/catalog from hand-maintained skills
