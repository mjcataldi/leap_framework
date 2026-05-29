# LEAP Release History

This file summarizes historical LEAP framework versions after the repository moved to a canonical current-document model in v1.9.

The active framework document is [`docs/leap.md`](leap.md), with LEAP Charter guidance in [`docs/leap-charter.md`](leap-charter.md). Detailed change entries remain in [`../CHANGELOG.md`](../CHANGELOG.md). Full historical framework files remain available through Git history, with the final v1.8 repository state preserved by the `leap-v1.8` tag.

## LEAP v1.9 - Repository canonicalization and prompt flattening

LEAP v1.9 is a repository-structure release. It keeps the v1.8 methodology intact while simplifying the active repository surface.

### What changed

- Replaced the versioned current framework document path with `docs/leap.md`.
- Flattened current operational prompts into root-level files under `prompts/`.
- Removed old versioned framework docs from the active repository.
- Removed nested historical prompt directories from the active repository.
- Added this release history document.
- Added `VERSION.md` as a small current-version marker.
- Preserved v1.8 history with the `leap-v1.8` Git tag.

### Current canonical files

```text
docs/leap.md
docs/leap-charter.md
prompts/leap-charter-standard.md
prompts/leap-recon-standard.md
prompts/leap-prompt-standard.md
prompts/leap-governance-pass-standard.md
```

## LEAP v1.8 - Adoption and ideation hardening

LEAP v1.8 made the framework easier to understand and apply, especially for users beginning with vague product intent.

### Added

- Renamed LEAP expansion to **Layered Execution & Alignment Protocol**.
- Added the **Ideation Loop** for turning vague human intent into buildable mechanisms.
- Added the question-loop rule: ask the fewest questions needed for the next safe gate decision, then keep looping while hard blockers remain.
- Added beginner-facing docs:
  - `docs/00_start_here.md`
  - `docs/leap-for-humans.md`
  - `docs/quick-leap-brief.md`
- Added tool-agnostic agent support docs:
  - `docs/agent-profiles.md`
- Added lightweight risk and destructive-change guidance:
  - `docs/risk-taxonomy.md`
- Added examples:
  - `docs/examples/small-build-unit.md`
  - `docs/examples/full-layer-recon.md`
- Added lightweight contribution guidance in `CONTRIBUTING.md`.

### Changed

- Shifted public framing from Codex-specific handoff language toward tool-agnostic **Agent Execution Configuration** language.
- Added minimum viable source-truth guidance.
- Added Recon confidence heuristics for Layer 0, whole layers, sublayers, Build Units, and tiny fixes.
- Added Build Unit sizing heuristics and red flags.
- Added agent failure-mode guidance.

## LEAP v1.7 - Codex execution configuration hardening

LEAP v1.7 closed a handoff gap by requiring coding-agent prompts to include explicit model and reasoning-level guidance.

### Added

- Added mandatory **Codex Execution Configuration** requirements for final LEAP implementation prompts.
- Added the rule that a prompt is not Codex-ready unless it includes an explicit model and reasoning level.
- Added separation between **LEAP process tier** and **Codex reasoning level**.
- Added execution fields for model, reasoning level, execution mode, scope scale, repository, branch/worktree, permissions, validation, and commit guidance.
- Added reasoning-level guidance for Low, Medium, High, and Extended execution settings.
- Added model/reasoning prompt-readiness blockers to stop conditions.
- Added v1.7 operational prompts for Phase 0, Recon, implementation, and governance.

### Changed

- Updated templates and prompts to require explicit execution settings.
- Updated prompt-library documentation to distinguish process tier from reasoning level.
- Updated glossary terminology for execution configuration, model, reasoning level, execution mode, scope scale, and prompt drift.

## LEAP v1.6 - Adversarial gate hardening

LEAP v1.6 made the framework more willing to block unsafe implementation and less likely to turn vague intent into polished coding prompts.

### Added

- Added readiness gates C0-C5 to replace user-facing fake-precision clarity thresholds.
- Added Source-of-Truth Manifest requirements before Recon or prompt generation.
- Added expanded documentation lifecycle states: Canonical, Active, Draft, Stale, Archived, Delete Candidate, Unknown.
- Added Drift Ledger guidance for strategy, documentation, implementation, branch/worktree/PR, and prompt drift.
- Added stronger coding-agent handoff contract requirements.
- Added Parallel-Agent Preflight and collision-zone rules.
- Added Small Project Mode.
- Added Thinking Extended as a model-selection tier between Standard and Pro Standard.
- Added v1.6 operational prompts for Phase 0, Recon, implementation, and governance.

### Changed

- Updated templates to use readiness gates, source-of-truth manifests, doc lifecycle status, drift review, and stricter stop conditions.
- Tightened blockers around missing non-goals, stale docs, unresolved source conflicts, unknown repo reality, branch drift, missing verification, and missing stop conditions.

## LEAP v1.5 - Gate-based inception and agent-safe prompting

LEAP v1.5 hardened the v1.4 lifecycle with clearer gates, stronger source-of-truth rules, and safer coding-agent handoffs.

### Added

- Added explicit Phase 0 gate decisions:
  - Proceed to Recon
  - Pressure Test Further
  - Narrow MVP First
  - Needs Human Decision
  - Do Not Build Yet
- Added Phase 0 modes:
  - Lite Inception
  - Standard Inception
  - Pro Inception
- Added evidence labels:
  - Known
  - Assumed
  - Unknown
  - Contested
  - Needs Decision
- Added model-effort tiers:
  - Standard
  - Pro Standard
  - Pro Extended
- Added agent stop-condition requirements.
- Added stronger human-checkpoint rules for high-risk decisions.
- Added source-of-truth ownership and stale-document governance rules.
- Added v1.5 operational prompts for Phase 0, Recon, implementation, and governance.

### Changed

- Made Phase 0 mode-aware.
- Updated clarity scoring guidance to avoid false precision and preserve blocker rules.
- Updated documentation bootstrap rules.
- Updated Recon expectations to include stale-assumption scans, source-of-truth ownership, branch/worktree drift, and human checkpoint triggers.
- Updated Prompt expectations to require objective, scope, constraints, non-goals, verification, stop conditions, and explicit output requirements.

## LEAP v1.4 - Phase 0 inception and no-build gate

LEAP v1.4 changed the lifecycle by adding mandatory project inception before Recon for new projects and major product-direction changes.

### Added

- Added **LEAP Phase 0 Inception** as the front door for new software projects and major product-direction changes.
- Added the three-stage lifecycle:
  - LEAP Phase 0 Inception
  - LEAP Recon
  - LEAP Prompt
- Added Socratic discovery rules for turning vague software ideas into baseline project direction.
- Added directional clarity scoring as a planning aid.
- Added market, competitor, substitute-workflow, and simpler-alternative pressure testing.
- Added MVP boundary requirements.
- Added the **No-Build Gate**.
- Added documentation bootstrap requirements for new LEAP-managed application repositories.
- Added source-of-truth index requirements.
- Added `templates/leap-phase-0-template.md`.

### Changed

- Updated the README workflow from two stages to three stages.
- Updated Recon and Prompt templates to require Phase 0/source-of-truth readiness before implementation planning.
- Expanded glossary terminology for Phase 0, clarity threshold, no-build gate, documentation bootstrap, and approval gate.

## LEAP v1.3 - Living architecture governance

LEAP v1.3 extended LEAP from a layer implementation workflow into a living architecture governance system.

### Added

- Added strategic plan reconciliation.
- Added cross-layer impact scanning.
- Added execution log expectations.
- Added regular reconciliation cadence.
- Added post-implementation reconciliation checklist.
- Added clearer separation between strategic intent, implementation reality, execution telemetry, and cross-layer impact.
- Added support for multi-agent, multi-branch, and multi-worktree workflows.
- Added the first reusable prompt-library structure.
- Added standard Recon, implementation, and governance prompts.

### Changed

- Updated LEAP Recon output expectations to include strategic reconciliation, cross-layer impacts, and execution log expectations.
- Updated LEAP Prompt expectations to include strategic reconciliation policy, execution log policy, cross-layer impact policy, and post-implementation reconciliation.

## LEAP v1.2 - Source-of-truth and pressure-test hardening

LEAP v1.2 strengthened the original two-stage model by requiring source grounding and repo reality review before implementation planning.

### Added

- Added explicit source-of-truth document intake for application-specific roadmap, status, domain, and architecture files.
- Added source-of-truth review as a required LEAP Recon section.
- Added repo reality reconciliation as a required LEAP Recon section when repository access is available.
- Added a formal Recon pressure-test rubric.
- Added layer boundary review.
- Added source-of-truth update policy for LEAP Prompts.
- Added application-repo vs LEAP-repo boundary guidance.
- Added stronger Build Unit fields for source-of-truth alignment, repo reality notes, existing models to reuse, migration risk, and testability.

### Changed

- Updated the README to point to LEAP v1.2 as current at the time.
- Updated Recon and Prompt templates for source-of-truth workflow.
- Expanded glossary terminology.

## LEAP v1.1 - Initial repository version

LEAP v1.1 was the first repository-backed version of the framework.

### Added

- Generalized LEAP from a Careero-specific workflow to a reusable solution-level framework.
- Established the original two-stage workflow:
  - LEAP Recon
  - LEAP Prompt
- Replaced earlier LHS terminology with **Build Unit**.
- Added Build Unit generation when the user supplies only solution context and target layer intent.
- Added default branch naming convention:
  - `layer<number>_<short_definition>`
- Added coding-agent question forecasting before prompt generation.
- Added clarification-question requirements before LEAP Prompt generation.
- Added required plan mode and reasoning-effort recommendations.
- Added buildout-mode defaults:
  - Rapid POC
  - Standard
  - Production-safe
  - Refactor
