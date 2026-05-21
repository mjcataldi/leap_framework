# Changelog

All notable changes to the LEAP Framework will be documented here.

## LEAP v1.5 — Gate-based inception and agent-safe prompting

### Added

- Added a versioned **LEAP v1.5** framework plan in `docs/leap-v1.5.md`.
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
- Added evidence labels for separating implementation truth from uncertainty:
  - Known
  - Assumed
  - Unknown
  - Contested
  - Needs Decision
- Added model-effort tiers for scaling LEAP process depth:
  - Standard
  - Pro Standard
  - Pro Extended
- Added agent stop-condition requirements for implementation prompts.
- Added stronger human-checkpoint rules for high-risk decisions.
- Added source-of-truth ownership and stale-document governance rules.
- Added operational prompt files for v1.5:
  - `prompts/leap/phase-0/v1.5/leap-phase-0-standard.md`
  - `prompts/leap/recon/v1.5/leap-recon-standard.md`
  - `prompts/leap/implementation/v1.5/leap-prompt-standard.md`
  - `prompts/leap/governance/v1.5/strategic-reconciliation-pass.md`

### Changed

- Updated README to point to LEAP v1.5 as the current version.
- Updated Phase 0 behavior from a single mandatory workflow to a mode-aware workflow with gate decisions.
- Updated clarity scoring guidance to avoid false precision and preserve blocker rules.
- Updated documentation bootstrap rules to distinguish required starter docs from conditional docs.
- Updated Recon expectations to include stale-assumption scans, source-of-truth ownership, branch/worktree drift, and human checkpoint triggers.
- Updated Prompt expectations to require objective, scope, constraints, non-goals, verification, stop conditions, and explicit output requirements.
- Updated prompt library README to include v1.5 prompt directories.
- Expanded glossary with v1.5 terminology.

### Notes

LEAP v1.5 is a minor-version hardening release. It keeps the v1.4 lifecycle:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

The release tightens the gates, source-of-truth rules, documentation governance, and coding-agent safety model.

The short rule:

```text
Clarity before code.
Evidence before polish.
Source of truth before prompt.
Bounded task before agent handoff.
Stop conditions before guessing.
```

## LEAP v1.4 — Phase 0 inception and no-build gate

### Added

- Added **LEAP Phase 0 Inception** as the mandatory front door for new software projects and major product-direction changes.
- Added a three-stage lifecycle:
  - LEAP Phase 0 Inception
  - LEAP Recon
  - LEAP Prompt
- Added Socratic discovery rules for turning vague software ideas into baseline project direction.
- Added directional clarity scoring:
  - below 67% clarity: continue discovery
  - 67% to 79% clarity: draft concept brief and continue pressure testing
  - 80%+ clarity: implementation strategy and layer planning allowed after approval
- Added market, competitor, substitute-workflow, and simpler-alternative pressure testing before implementation planning.
- Added MVP boundary requirements including first useful user outcome, explicit non-goals, manual-for-now workflows, validation criteria, and overbuild risks.
- Added the **No-Build Gate** that blocks layer planning and coding-agent prompts until minimum clarity, source-of-truth docs, and human approval exist.
- Added documentation bootstrap requirements for new LEAP-managed application repositories.
- Added source-of-truth index requirements for application repos.
- Added `templates/leap-phase-0-template.md`.

### Changed

- Updated README to point to LEAP v1.4 as the current version.
- Updated README workflow from two stages to three stages.
- Updated Recon template to check Phase 0 / source-of-truth readiness before layer planning.
- Updated Prompt template to require Phase 0 and approved Recon before coding-agent prompt generation.
- Expanded glossary with Phase 0, clarity threshold, no-build gate, documentation bootstrap, and approval gate terminology.

### Notes

LEAP v1.4 changes the framework lifecycle. LEAP still uses Recon and Prompt for implementation, but it now requires project inception and pressure-tested direction before implementation planning for new projects.

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

## LEAP v1.3 — Living architecture governance

### Added

- Added strategic plan reconciliation.
- Added cross-layer impact scanning.
- Added execution log expectations.
- Added regular reconciliation cadence.
- Added post-implementation reconciliation checklist.
- Added clearer separation between strategic intent, implementation reality, execution telemetry, and cross-layer impact.
- Added support for multi-agent, multi-branch, and multi-worktree workflows.

### Changed

- Extended LEAP from a layer implementation workflow into a living architecture governance system.
- Updated LEAP Recon output expectations to include strategic reconciliation, cross-layer impacts, and execution log expectations.
- Updated LEAP Prompt expectations to include strategic reconciliation policy, execution log policy, cross-layer impact policy, and post-implementation reconciliation.

### Notes

LEAP v1.3 kept the same two-stage model as v1.2:

```text
LEAP Recon → LEAP Prompt
```

## LEAP v1.2 — Source-of-truth and pressure-test hardening

### Added

- Added explicit source-of-truth document intake for application-specific roadmap, status, domain, and architecture files.
- Added source-of-truth review as a required LEAP Recon section.
- Added repo reality reconciliation as a required LEAP Recon section when repository access is available.
- Added a formal Recon pressure-test rubric covering:
  - repo reality
  - already-built collisions
  - branch drift
  - layer boundaries
  - Build Unit atomicity
  - dependencies
  - migrations and destructive changes
  - frontend/backend/API alignment
  - testability
  - truthfulness/source grounding
  - user value
- Added layer boundary review to reduce scope creep and prevent future-layer work from leaking into current-layer implementation.
- Added source-of-truth update policy for LEAP Prompts.
- Added application-repo vs LEAP-repo boundary guidance.
- Added stronger Build Unit fields for source-of-truth alignment, repo reality notes, existing models to reuse, migration risk, and testability.

### Changed

- Updated the README to point to LEAP v1.2 as the current version.
- Updated the LEAP Recon template to include source-of-truth documents, repo reality reconciliation, and pressure-test expectations.
- Updated the LEAP Prompt template to include source-of-truth instructions and update policy.
- Expanded the glossary with v1.2 terms.

### Notes

LEAP v1.2 keeps the same two-stage model as v1.1:

```text
LEAP Recon → LEAP Prompt
```

This is a minor-version hardening release, not a major framework redesign.

## LEAP v1.1 — Initial repository version

### Added

- Generalized LEAP from a Careero-specific workflow to a reusable solution-level framework.
- Established the two-stage workflow:
  - LEAP Recon
  - LEAP Prompt
- Replaced the earlier LHS terminology with **Build Unit**.
- Added Build Unit generation when the user supplies only solution context and target layer intent.
- Added default branch naming convention:
  - `layer<number>_<short_definition>`
- Added coding-agent question forecasting before prompt generation.
- Added clarification-question requirements before LEAP Prompt generation.
- Added required plan mode and reasoning effort recommendations.
- Added buildout-mode defaults:
  - Rapid POC
  - Standard
  - Production-safe
  - Refactor

### Notes

This is the first repository-backed version of LEAP.
