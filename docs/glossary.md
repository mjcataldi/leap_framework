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
- clarity assessment
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

A polished assumption is still an assumption.

## Clarity Threshold

A directional readiness estimate used during Phase 0.

Default clarity bands:

```text
Below 67% clarity:
Continue discovery.

67% to 79% clarity:
Draft concept brief and continue pressure testing.

80%+ clarity:
Implementation strategy and layer planning allowed after approval.
```

The clarity threshold is not a precise mathematical measurement. It is a planning signal and must be paired with blockers, confidence notes, and evidence labels.

## Gate Decision

The explicit decision at the end of Phase 0 or Recon.

Supported gate decisions:

- Proceed to Recon
- Pressure Test Further
- Narrow MVP First
- Needs Human Decision
- Do Not Build Yet
- Reconcile Docs First
- Generate LEAP Prompt

## No-Build Gate

A LEAP rule that blocks implementation planning and coding-agent prompts until minimum clarity and documentation requirements are met.

At minimum, LEAP should not proceed to layer planning without:

- project charter or equivalent baseline strategy
- MVP boundary or explicit scope boundary
- pressure-test summary when the idea is new or strategically material
- source-of-truth index or explicit source-of-truth list
- open questions list
- explicit human approval

## Approval Gate

The explicit human checkpoint between Phase 0 and layer planning.

The user must approve the baseline product direction, MVP boundary, non-goals, risks, assumptions, documentation scaffold, and permission to begin layer planning.

## Human Checkpoint

A point where LEAP must stop and ask for human approval before continuing.

Human approval is required when the agent would otherwise need to guess about product direction, MVP expansion, source-of-truth changes, architecture, auth, permissions, sensitive data, monetization, destructive migrations, external integrations, AI behavior, or overlapping parallel-agent scopes.

## Documentation Bootstrap

The initial documentation scaffold created for a LEAP-managed application repository.

LEAP v1.5 separates required starter docs from conditional docs.

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

## Source-of-Truth Index

The application-repo file, usually `docs/source-of-truth.md`, that identifies the canonical project strategy, MVP boundary, implementation strategy, layer map, execution log, and deprecated or archived docs.

In v1.5 it should also identify document owners, last meaningful update, doc status, truth owned, and conflict-resolution rules.

## Source-of-Truth Status

The classification for a planning document.

Supported statuses:

- Canonical
- Supporting
- Archived
- Unknown

No two canonical docs should own the same truth.

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

The analysis, source-of-truth reconciliation, repo reality reconciliation, pressure-test, Build Unit generation/refinement, sequencing, cross-layer impact review, stale-assumption scan, and clarification stage.

Recon is run before generating the implementation prompt.

For new projects, Phase 0 must be completed and approved before Recon begins.

## LEAP Prompt

The final implementation prompt artifact given to Codex-style or another AI coding agent.

It tells the coding agent how to build the layer sequentially and safely.

In v1.5, a LEAP Prompt must be a bounded task packet with objective, scope, constraints, verification, and stop conditions.

## Stop Condition

A rule inside a LEAP Prompt that tells the coding agent to stop and report instead of guessing.

Stop conditions are required when docs conflict with code, architecture is unclear, sensitive data handling is unclear, implementation requires unapproved dependencies/migrations/auth/billing/AI behavior changes, or the task would violate non-goals.

## Model-Effort Tier

The LEAP process depth selected for the task.

Supported defaults:

- Standard
- Pro Standard
- Pro Extended

Model-effort tier should match ambiguity, risk, and blast radius.

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

---

## LEAP v1.6 Addendum

### Readiness Gate

A user-facing operational gate that replaces fake-precision clarity scoring.

Supported gates:

- C0: Blocked
- C1: Discovery Ready
- C2: Concept Ready
- C3: Pressure-Test Ready
- C4: Layer-Planning Ready
- C5: Coding-Prompt Ready

### Source-of-Truth Manifest

The active manifest that identifies canonical and active docs, stale/archived/do-not-use docs, target branch, base branch, relevant PRs, repo reality, known conflicts, and human owner/approver.

### Documentation Lifecycle Status

The v1.6 doc status system:

- Canonical
- Active
- Draft
- Stale
- Archived
- Delete Candidate
- Unknown

Generated docs are Draft until ratified.

### Drift Ledger

A record of strategy, documentation, implementation, branch/worktree/PR, or prompt drift.

### Parallel-Agent Preflight

A required ownership and merge-order review before multiple agents or worktrees operate at the same time.

### Small Project Mode

A lightweight LEAP mode for low-risk, clearly scoped tasks. It requires only goal, current state, scope, non-goals, likely files, acceptance criteria, tests/checks, and stop conditions.

### Thinking Extended

The model tier between Standard and Pro Standard. Use it for Phase 0 discovery, MVP/non-goal work, moderate Recon, bounded prompt drafting, and small architecture tradeoffs.
