# Changelog

All notable changes to the LEAP Framework will be documented here.

## LEAP v1.9 — Repository canonicalization and prompt flattening

### Added

- Added canonical current framework document path: `docs/leap.md`.
- Added detailed historical summary in `docs/release-history.md`.
- Added current version marker in `VERSION.md`.
- Added flattened current operational prompt files:
  - `prompts/leap-phase-0-standard.md`
  - `prompts/leap-recon-standard.md`
  - `prompts/leap-prompt-standard.md`
  - `prompts/leap-governance-pass-standard.md`

### Changed

- Updated README and prompt-library documentation to describe the canonical-current repository model.
- Replaced the active versioned framework-doc model with a canonical current framework document.
- Replaced nested current prompt paths with root-level prompt files under `prompts/`.
- Updated templates and current prompt files to use version-neutral current-framework wording.

### Removed

- Removed old versioned framework docs from the active repository.
- Removed nested historical prompt directories from the active repository.
- Removed the old v1.3 prompt-library document from the active repository.

### Notes

LEAP v1.9 is a repository-structure release. It does not change the Ideation Loop, readiness gates, source-of-truth discipline, risk taxonomy, or agent execution configuration semantics from v1.8.

Historical version visibility is preserved through Git tags, Git history, this changelog, and `docs/release-history.md`.

## LEAP v1.8 — Adoption and ideation hardening

### Added

- Added a versioned **LEAP v1.8** framework plan in `docs/leap-v1.8.md`.
- Renamed LEAP expansion to **Layered Execution & Alignment Protocol**.
- Added the **Ideation Loop** for turning vague human intent into buildable mechanisms.
- Added the question-loop rule: ask the fewest questions needed to make the next safe gate decision, then keep looping while hard blockers remain.
- Added beginner-facing adoption docs:
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

- Updated README to point to LEAP v1.8 as the current version.
- Updated public framing from Codex-specific handoff language toward tool-agnostic **Agent Execution Configuration** language.
- Added minimum viable source-truth guidance.
- Added Recon confidence heuristics for Layer 0, whole layers, sublayers, Build Units, and tiny fixes.
- Added Build Unit sizing heuristics and red flags.
- Added agent failure-mode guidance.

### Notes

LEAP v1.8 is an adoption and ideation hardening release. It keeps the lifecycle:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

The release clarifies how LEAP helps ideation: it does not assume the first expression of an idea is buildable. It cycles through targeted questions, evidence labeling, assumption tracking, pressure testing, and gate decisions until the next safe step is clear.

The short rule:

```text
No clarity, no build.
No source truth, no Recon.
No repo reality, no implementation plan.
No stop conditions, no coding task.
No execution profile, no agent-ready prompt.
Ask until the idea becomes buildable, then stop asking and build only the bounded task.
```

## LEAP v1.7 — Codex execution configuration hardening

### Added

- Added a versioned **LEAP v1.7** framework plan in `docs/leap-v1.7.md`.
- Added mandatory **Codex Execution Configuration** requirements for final LEAP implementation prompts.
- Added the hard rule that a prompt is not Codex-ready unless it includes an explicit model and reasoning level.
- Added clear separation between **LEAP process tier** and **Codex reasoning level**.
- Added Codex execution fields for:
  - Model
  - Reasoning Level
  - Execution Mode
  - Scope Scale
  - Repository
  - Branch / Worktree
  - Permissions
  - Validation
  - Commit Guidance
- Added reasoning-level guidance for Low, Medium, High, and Extended execution settings.
- Added model/reasoning prompt-readiness blockers to stop conditions.
- Added v1.7 operational prompts:
  - `prompts/leap/phase-0/v1.7/leap-phase-0-standard.md`
  - `prompts/leap/recon/v1.7/leap-recon-standard.md`
  - `prompts/leap/implementation/v1.7/leap-prompt-standard.md`
  - `prompts/leap/governance/v1.7/strategic-reconciliation-pass.md`

### Changed

- Updated README to point to LEAP v1.7 as the current version.
- Updated Phase 0, Recon, and Prompt templates to reference LEAP v1.7.
- Updated Recon templates and prompts to recommend explicit Codex execution settings before LEAP Prompt generation.
- Updated Prompt templates and implementation prompts to include the Codex Execution Configuration block near the top of the final handoff.
- Updated prompt library README to document v1.7 prompt directories and distinguish process tier from reasoning level.
- Updated glossary with v1.7 terminology for Codex Execution Configuration, Model, Reasoning Level, Execution Mode, Scope Scale, and Prompt Drift.

### Notes

LEAP v1.7 is a minor hardening release. It keeps the lifecycle:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

The release closes a practical handoff gap: v1.6 knew how to recommend model tiers, but Codex-ready prompts also need concrete model and reasoning-level instructions at the point of use.

The short rule:

```text
No model, no handoff.
No reasoning level, no Codex-ready prompt.
No source truth, no Recon.
No repo reality, no implementation plan.
No stop conditions, no coding task.
```

## LEAP v1.6 — Adversarial gate hardening

### Added

- Added a versioned **LEAP v1.6** framework plan in `docs/leap-v1.6.md`.
- Added readiness gates C0–C5 to replace user-facing fake-precision clarity thresholds.
- Added Source-of-Truth Manifest requirements before Recon or prompt generation.
- Added expanded documentation lifecycle states: Canonical, Active, Draft, Stale, Archived, Delete Candidate, Unknown.
- Added Drift Ledger guidance for strategy, documentation, implementation, branch/worktree/PR, and prompt drift.
- Added stronger agent-handoff contract requirements for Codex-style coding agents.
- Added explicit Parallel-Agent Preflight and collision-zone rules.
- Added Small Project Mode to prevent LEAP from becoming bureaucracy.
- Added Thinking Extended as a model-selection tier between Standard and Pro Standard.
- Added v1.6 operational prompts:
  - `prompts/leap/phase-0/v1.6/leap-phase-0-standard.md`
  - `prompts/leap/recon/v1.6/leap-recon-standard.md`
  - `prompts/leap/implementation/v1.6/leap-prompt-standard.md`
  - `prompts/leap/governance/v1.6/strategic-reconciliation-pass.md`

### Changed

- Updated README to point to LEAP v1.6 as the current version.
- Updated Phase 0, Recon, and Prompt templates to use readiness gates, source-of-truth manifests, doc lifecycle status, drift review, and stricter stop conditions.
- Updated prompt library README to include v1.6 prompt directories and model-tier guidance.
- Tightened prompt generation blockers around missing non-goals, stale docs, unresolved source conflicts, unknown repo reality, branch drift, missing verification, and missing stop conditions.

### Notes

LEAP v1.6 is a minor hardening release. It keeps the lifecycle:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

The release makes the framework more willing to block unsafe implementation and less likely to launder vague intent into polished coding prompts.


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
