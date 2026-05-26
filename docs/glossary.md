# LEAP Glossary

## LEAP

**Layer Execution & Assembly Protocol**.

A framework for turning rough software intent into pressure-tested direction, sequenced plans, governed implementation prompts, and maintainable application documentation.

## Solution

The system, product, platform, internal tool, data system, AI application, or infrastructure initiative being built.

## Phase 0 Inception

The mandatory LEAP project-start workflow for new software projects or major new product directions.

Phase 0 turns vague software intent into a pressure-tested baseline direction before implementation planning begins.

It includes:

- idea intake
- Socratic discovery
- evidence labeling
- clarity/readiness assessment
- market / alternative solution pressure testing
- MVP boundary definition
- strategic plan generation when clarity is sufficient
- documentation bootstrap recommendation
- gate decision before Recon

## Phase 0 Mode

The discovery depth selected for Phase 0.

Supported defaults:

- Lite Inception
- Standard Inception
- Pro Inception
- Small Project Mode

Mode is selected by ambiguity, risk, and blast radius.

## Socratic Discovery

The structured LEAP dialogue used to clarify an early software idea.

It asks targeted questions about the user, problem, current workflow, MVP, risks, constraints, and success criteria.

Socratic discovery should happen in small rounds rather than one giant question dump.

## Evidence Label

A label that separates implementation truth from uncertainty.

Supported labels:

- Known
- Assumed
- Unknown
- Contested
- Needs Decision
- Deprecated

A polished assumption is still an assumption.

## Readiness Gate

A user-facing operational gate that replaced fake-precision clarity scoring in v1.6.

Supported gates:

- C0: Blocked
- C1: Discovery Ready
- C2: Concept Ready
- C3: Pressure-Test Ready
- C4: Layer-Planning Ready
- C5: Coding-Prompt Ready

In v1.7, C5 requires source truth, repo reality, scope, tests, stop conditions, explicit model, and explicit reasoning level.

## Clarity Threshold

A legacy directional readiness estimate used during earlier Phase 0 versions.

v1.6+ uses readiness gates for user-facing decisions instead of numeric clarity thresholds. Numeric clarity may still be used privately as a thinking aid, but it must not override hard blockers.

## Gate Decision

The explicit decision at the end of Phase 0 or Recon.

Supported gate decisions include:

- Proceed to Recon
- Pressure Test Further
- Narrow MVP First
- Needs Human Decision
- Do Not Build Yet
- Reconcile Docs First
- Resolve Branch Drift First
- Generate LEAP Prompt

## No-Build Gate

A LEAP rule that blocks implementation planning and coding-agent prompts until minimum clarity and documentation requirements are met.

At minimum, LEAP should not proceed to layer planning without:

- project charter or equivalent baseline strategy
- MVP boundary or explicit scope boundary
- pressure-test summary when the idea is new or strategically material
- source-of-truth manifest or explicit source-of-truth list
- open questions list
- explicit human approval

## Approval Gate

The explicit human checkpoint between Phase 0 and layer planning.

The user must approve the baseline product direction, MVP boundary, non-goals, risks, assumptions, documentation scaffold, and permission to begin layer planning.

## Human Checkpoint

A point where LEAP must stop and ask for human approval before continuing.

Human approval is required when the agent would otherwise need to guess about product direction, MVP expansion, source-of-truth changes, architecture, auth, permissions, sensitive data, monetization, destructive migrations, external integrations, AI behavior, overlapping parallel-agent scopes, or execution configuration.

## Documentation Bootstrap

The initial documentation scaffold created for a LEAP-managed application repository.

Required starter docs for most new projects:

```text
docs/
  README.md
  source-of-truth.md
  strategy/
    project-charter.md
  architecture/
    decision-log.md
```

Conditional docs include:

```text
docs/strategy/discovery-notes.md
docs/strategy/pressure-test.md
docs/strategy/mvp-boundary.md
docs/strategy/implementation-strategy.md
docs/layers/README.md
docs/execution/execution-log.md
docs/architecture/cross-layer-impact-map.md
```

## Project Charter

The baseline strategy document that defines what the product is, who it serves, what problem it solves, and what the first version should prove.

## MVP Boundary

The document that defines the smallest useful version of the product.

It should include:

- first useful user outcome
- primary user
- primary workflow
- primary success signal
- must-have features
- should-have-if-easy features
- explicit non-goals
- later roadmap candidates
- manual-for-now workflows
- validation criteria
- overbuild risks

## Source-of-Truth Manifest

The active manifest that identifies canonical and active docs, stale/archived/do-not-use docs, target branch, base branch, relevant PRs, repo reality, known conflicts, and human owner/approver.

## Source-of-Truth Index

The application-repo file, usually `docs/source-of-truth.md`, that identifies the canonical project strategy, MVP boundary, implementation strategy, layer map, execution log, and deprecated or archived docs.

In v1.5+ it should also identify document owners, last meaningful update, doc status, truth owned, and conflict-resolution rules.

## Source-of-Truth Status

The classification for a planning document.

Legacy statuses:

- Canonical
- Supporting
- Archived
- Unknown

v1.6+ documentation lifecycle statuses:

- Canonical
- Active
- Draft
- Stale
- Archived
- Delete Candidate
- Unknown

No two canonical docs should own the same truth.

Generated docs are Draft until ratified.

## Layer

A major capability phase or architectural slice of the solution.

Examples:

- Layer 0 — Product foundation
- Layer 1 — Core platform
- Layer 2 — Intake & Parsing
- Layer 3 — Evaluation & Artifacts
- Layer 4 — Application Workflow

Project-specific layer names may vary.

## Build Unit

A scoped subsection of a layer that can be implemented, tested, and committed independently.

A Build Unit should be:

- specific enough for implementation
- large enough to represent a coherent domain capability
- small enough to be one commit in most cases
- sequenced against earlier Build Units
- explicit about exclusions and boundaries
- aligned to source-of-truth documents when provided
- checked against repo reality when repo access is available

## Source-of-Truth Document

An application-specific roadmap, layer status, domain model, architecture, project-charter, MVP-boundary, execution-state, or implementation-status document that governs repo-specific planning.

LEAP uses source-of-truth documents to avoid relying on stale chat history and to prevent rebuilding capabilities that already exist.

## Source-of-Truth Review

A LEAP Recon section that extracts relevant decisions, constraints, current-status claims, and required documentation updates from application-specific source-of-truth documents.

## Source-of-Truth Discovery

A LEAP Recon section that identifies which docs exist, which docs are canonical, which docs are stale or archived, who owns each doc, and which source of truth governs the current task.

## Repo Reality Reconciliation

A LEAP Recon section that compares source-of-truth claims against the actual repository state when repo access is available.

If repo reality conflicts with the source-of-truth document, repo reality should guide implementation planning, and the documentation conflict should be reported.

## Branch / Worktree Drift Review

A LEAP Recon section that identifies whether the base branch, target branch, active branches, worktrees, or recent changes may conflict with the planned implementation.

## Stale Assumption Scan

A LEAP Recon section that identifies old docs, stale roadmap claims, unverified assumptions, conflicting claims, and assumptions that must be revalidated before implementation.

## Strategic Plan Reconciliation

A LEAP Recon section that checks whether strategic or layer-planning documents remain aligned with current implementation reality.

## Cross-Layer Impact Scan

A LEAP Recon section that identifies whether work in the target layer affects shared entities, workflows, APIs, data models, architecture, future layers, or previous assumptions.

## Cross-Layer Impact Map

An application-repo dependency registry that tracks how shared concepts, models, workflows, and implementation decisions affect multiple layers.

Recommended path:

```text
docs/architecture/cross-layer-impact-map.md
```

## Execution Log

A per-run implementation record capturing what changed, what was discovered, and what follow-up is needed.

Recommended directory:

```text
docs/execution/
```

## Pressure-Test Findings

A LEAP assessment that evaluates whether the target concept, layer, or Build Units are safe, useful, properly bounded, and implementable.

Pressure testing may include:

- market and alternative-solution review
- simpler non-app alternatives
- repo reality check
- already-built collision check
- branch drift check
- layer boundary check
- Build Unit atomicity check
- dependency check
- migration/destructive-change check
- frontend/backend/API alignment check
- testability check
- truthfulness/source-grounding check where applicable
- user value check

## LEAP Recon

The analysis, source-of-truth reconciliation, repo reality reconciliation, pressure-test, Build Unit generation/refinement, sequencing, cross-layer impact review, stale-assumption scan, execution-configuration recommendation, and clarification stage.

Recon is run before generating the implementation prompt.

For new projects, Phase 0 must be completed and approved before Recon begins.

## LEAP Prompt

The final implementation prompt artifact given to Codex-style or another AI coding agent.

It tells the coding agent how to build the layer sequentially and safely.

In v1.7, a LEAP Prompt must be a bounded task packet with objective, scope, constraints, verification, stop conditions, and explicit Codex execution configuration.

## Codex Execution Configuration

The explicit runtime handoff block required in every Codex-ready LEAP Prompt.

It must include:

- Model
- Reasoning Level
- Execution Mode
- Scope Scale
- Repository
- Branch / Worktree
- Permissions
- Validation
- Commit Guidance

A prompt is not Codex-ready unless it tells the user exactly which model and reasoning level to use.

## Model

The exact model or approved project default the user should select when running the Codex prompt.

If the project convention uses model minor versions, the model field must include the minor version.

## Reasoning Level

The intended reasoning depth for the coding agent.

Common guidance:

- Low — tiny localized edits, typo fixes, obvious one-file changes
- Medium — small bounded implementation, clear UI fixes, simple tests, isolated refactors
- High — Build Units, sublayers, multi-file features, state workflows, cross-component UX, meaningful test updates
- Extended — full-layer implementation, architecture-sensitive work, repo-wide refactors, parallel-agent sequencing, stale-doc reconciliation, destructive schema/data-model changes, sensitive AI behavior

## Execution Mode

The intended coding-agent posture.

Common values:

- recon-only
- plan-first
- implement-directly
- implement-with-brief-plan

## Scope Scale

The size of the target task.

Common values:

- small task
- Build Unit
- sublayer
- entire layer
- repo-wide maintenance

## LEAP Process Tier

The LEAP analysis depth selected for the task.

Supported defaults:

- Standard
- Thinking Extended
- Pro Standard
- Pro Extended

LEAP process tier controls how much framework analysis happens before prompt generation.

## Model-Effort Tier

Legacy term for LEAP process depth. Prefer **LEAP Process Tier** in v1.7+ to avoid confusing process depth with the final Codex reasoning level.

## Stop Condition

A rule inside a LEAP Prompt that tells the coding agent to stop and report instead of guessing.

Stop conditions are required when docs conflict with code, architecture is unclear, sensitive data handling is unclear, implementation requires unapproved dependencies/migrations/auth/billing/AI behavior changes, model or reasoning level is unavailable without an approved fallback, or the task would violate non-goals.

## Buildout mode

The execution posture for the layer.

Supported defaults:

- Rapid POC
- Standard
- Production-safe
- Refactor

## Architecture right-sizing

The rule that implementation should neither force new work into a bad architecture nor overbuild speculative infrastructure.

## Hand-jamming

Forcing a new capability into an unsuitable existing architecture because it is convenient in the short term.

LEAP discourages hand-jamming when the current architecture crosses a reasonable tipping point.

## Layer Boundary Review

A LEAP Recon section that separates what belongs in the target layer from work that belongs in prior or future layers.

This helps prevent scope creep and accidental implementation of integrations, automation, productization, or marketplace features before their intended layer.

## Source-of-Truth Update Policy

A LEAP Prompt section that tells the coding agent whether and when to update application-specific roadmap/status documents after implementation changes reality.

Generic LEAP methodology should not be updated from an application implementation prompt unless the prompt explicitly targets the LEAP repository.

## Structured Scoring / STRIDE-style Evaluation

A scoring or classification method used by a project to support decisions.

LEAP treats structured scores as advisory. Scores must expose rationale, uncertainty, missing evidence, and assumptions instead of pretending incomplete evidence creates objective truth.

## Coding-agent question forecast

A LEAP Recon section that predicts the questions a coding agent might otherwise ask during implementation.

The goal is to answer material questions before the coding run begins.

## Prompt Drift

A LEAP drift type where a prompt assumes stale files, stale branch state, old decisions, missing model, or missing reasoning level.

Prompt drift requires a prompt freshness check and regenerated handoff.

---

## LEAP v1.7 Addendum

### Codex Execution Configuration

The mandatory model/reasoning/execution block for final implementation prompts.

### LEAP Process Tier vs Codex Reasoning Level

LEAP process tier controls analysis depth before prompt generation.

Codex reasoning level controls how the implementation agent should be run after prompt generation.

They are related but not interchangeable.

### Prompt-readiness blocker

A LEAP Prompt is not Codex-ready unless it tells the user exactly which model and reasoning level to use.
