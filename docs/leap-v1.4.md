# LEAP Framework Plan v1.4

## Framework name

**LEAP — Layer Execution & Assembly Protocol**

LEAP is a solution-level framework for turning rough software intent into pressure-tested direction, layered plans, and safe, sequential, implementation-ready AI coding prompts.

LEAP v1.4 extends LEAP with a mandatory project-inception front door. LEAP no longer begins with layer planning when the user has only a vague app idea.

The v1.4 lifecycle is:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

---

## 1. Core concept

```text
Phase 0 Inception = The mandatory project-start workflow that converts vague software intent into pressure-tested baseline direction.
Layer = A major system capability or architectural phase.
Build Unit = A scoped subsection of the layer that can be implemented and committed independently.
Source-of-Truth Document = An application-specific project charter, MVP boundary, roadmap/status/architecture file, or execution-state file that governs repo-specific decisions.
Execution Log = A per-run implementation record capturing what changed, what was discovered, and what follow-up is needed.
Cross-Layer Impact Map = A dependency registry that tracks which layers are affected by changes to shared entities, workflows, or architecture.
LEAP = The framework that discovers, pressure-tests, designs, sequences, governs, prompt-generates, implements, and reconciles layered buildout.
```

LEAP v1.4 adds a hard rule:

> LEAP may help clarify vague ideas. LEAP may not convert vague ideas directly into implementation plans or coding-agent prompts.

---

## 2. Lifecycle overview

### 2.1 Phase 0 — LEAP Inception

Phase 0 is the discovery, pressure-test, MVP boundary, and documentation-bootstrap phase.

It is required for:

- new software projects
- major new product directions
- unclear app ideas
- projects without a documented baseline direction
- projects where the user asks to build before the problem, user, and MVP are clear

Phase 0 produces:

1. clear problem statement
2. target user definition
3. current pain / workflow description
4. current alternatives or competitors
5. pressure-tested product thesis
6. first useful MVP boundary
7. explicit non-goals
8. known risks and constraints
9. baseline implementation strategy
10. starter documentation structure
11. source-of-truth index
12. approval gate before layer planning

### 2.2 Stage 1 — LEAP Recon

LEAP Recon begins only after Phase 0 is complete or when an existing project already has enough source-of-truth documentation.

Recon analyzes the target layer, reconciles source-of-truth docs with repo reality, generates or refines Build Units, pressure-tests the plan, and identifies clarification needs before generating a coding prompt.

### 2.3 Stage 2 — LEAP Prompt

LEAP Prompt converts approved Recon findings into the final implementation prompt for Codex or another AI coding agent.

Prompt generation is blocked if Phase 0, source-of-truth, or Recon approval requirements are not met.

---

## 3. Phase 0 purpose

Phase 0 exists to prevent this failure mode:

```text
“I want to build a cool app. Go build it.”
```

That is not enough context for layer planning, implementation strategy, or coding-agent work.

Phase 0 turns rough intent into a baseline direction by establishing:

- who the first real user is
- what painful problem the user has
- what they do today instead
- why the current workflow is inadequate
- what the first useful version should accomplish
- what the app should explicitly avoid becoming
- what risks and constraints matter
- whether a full app is even the right solution
- what docs must exist before implementation begins

Phase 0 is not a giant business-plan generator. It is a clarity and safety gate.

---

## 4. Phase 0 workflow

LEAP Phase 0 has eight required stages.

```text
0.1 Idea Intake
0.2 Socratic Discovery
0.3 Clarity Scoring
0.4 Market / Alternative Solution Pressure Test
0.5 MVP Boundary Definition
0.6 Strategic Plan Generation
0.7 Documentation Bootstrap
0.8 Approval Gate to Begin Layer Planning
```

### 4.1 Idea Intake

The user begins with a general idea.

LEAP captures:

```text
- original user idea
- stated problem
- intended users, if known
- desired outcome
- known constraints
- existing repo or new repo
- technical preferences, if any
- business or personal motivation
- urgency / timeline
- known risks or worries
```

LEAP should preserve the user’s original wording because early phrasing often reveals the real motivation.

### 4.2 Socratic Discovery

LEAP asks targeted follow-up questions in rounds.

Each round should include:

```text
- 5 to 8 high-leverage questions
- short summary of what is now understood
- list of open uncertainties
- recommendation on whether another round is needed
```

LEAP should not dump 30 questions at once.

### 4.3 Clarity Scoring

LEAP estimates readiness using clarity bands.

```text
Below 67% clarity:
Continue discovery. Do not generate implementation strategy.

67% to 79% clarity:
Generate a draft concept brief. Continue pressure testing and refinement.

80% or higher clarity:
Allow implementation strategy and layer planning after approval.

Coding-agent prompts:
Forbidden until the approval gate is passed.
```

The score is a planning signal, not a precise measurement.

### 4.4 Market / Alternative Solution Pressure Test

LEAP pressure tests the idea against reality.

This includes:

```text
- existing products
- substitute workflows
- manual workarounds
- open-source alternatives
- internal-tool alternatives
- spreadsheet / no-code / automation alternatives
- user adoption friction
- monetization friction
- data/security/privacy risks
- maintenance burden
- hidden adjacent opportunities
```

Important rule:

```text
LEAP must consider whether the solution should be an app at all.
```

Sometimes the better first solution is a workflow, spreadsheet, script, plugin, browser extension, Slack/Teams bot, dashboard, integration, or manual service.

### 4.5 MVP Boundary Definition

LEAP defines the smallest useful version around the first meaningful user outcome.

Required sections:

```text
- first useful user outcome
- must-have features
- should-have features if easy
- explicit non-goals
- later roadmap candidates
- manual-for-now workflows
- validation criteria
- overbuild risks
- assumptions that must be validated
```

The MVP should answer:

```text
Could a real target user get value from this version without the entire long-term vision being built?
```

### 4.6 Strategic Plan Generation

Once the concept reaches sufficient clarity, LEAP generates the baseline strategic plan.

It should include:

```text
- product thesis
- target users
- problem statement
- current alternatives
- core workflows
- MVP boundary
- non-goals
- differentiators
- risks and constraints
- initial implementation assumptions
- recommended layer strategy
- open questions
```

This becomes the first strategic source of truth.

### 4.7 Documentation Bootstrap

LEAP creates the starter documentation structure before detailed implementation planning.

Recommended minimum:

```text
docs/
  README.md
  source-of-truth.md

  strategy/
    project-charter.md
    discovery-notes.md
    pressure-test.md
    mvp-boundary.md
    implementation-strategy.md

  architecture/
    decision-log.md

  layers/
    README.md

  execution/
    execution-log.md
```

### 4.8 Approval Gate to Begin Layer Planning

Before moving to layer planning, LEAP must present an approval packet.

The user must approve:

```text
- product direction
- MVP boundary
- non-goals
- initial implementation strategy
- documentation structure
- open assumptions
- permission to begin layer planning
```

Only after this approval may LEAP proceed to Recon and layer planning.

---

## 5. Socratic discovery model

LEAP should ask questions across six discovery areas.

### 5.1 User and problem

Purpose: identify who the app is for and what pain matters.

Example questions:

```text
1. Who is the first real user of this app?
2. What problem are they trying to solve?
3. How painful or frequent is the problem?
4. What happens if they do nothing?
5. Is this problem urgent, expensive, annoying, risky, or emotionally draining?
```

### 5.2 Current workflow

Purpose: understand what users do today.

Example questions:

```text
1. What are users doing today instead of using this app?
2. Are they using spreadsheets, manual processes, existing software, email, documents, or memory?
3. What breaks in the current workflow?
4. Where does time, money, accuracy, or confidence get lost?
5. What part of the workflow is most frustrating?
```

### 5.3 Product shape

Purpose: determine what the application actually is.

Example questions:

```text
1. Is this primarily a dashboard, workflow tool, marketplace, automation, AI assistant, database, communication tool, or something else?
2. What is the core action the user performs?
3. What does the user need to see, decide, create, or track?
4. What would the user come back to the app for?
5. What would make the product feel immediately useful?
```

### 5.4 MVP boundary

Purpose: prevent overbuilding.

Example questions:

```text
1. What is the smallest version that would still be useful?
2. What features are tempting but not necessary at launch?
3. What should the product explicitly not do yet?
4. Which workflow must be excellent first?
5. What can stay manual in the first version?
```

### 5.5 Risks and constraints

Purpose: surface hidden blockers.

Example questions:

```text
1. Does the app handle sensitive data?
2. Are there legal, financial, medical, employment, privacy, or compliance concerns?
3. Does the app depend on third-party APIs or external data?
4. What could make the product hard to maintain?
5. What would make the idea fail even if the app is technically well-built?
```

### 5.6 Success and direction

Purpose: define what “working” means.

Example questions:

```text
1. What would success look like for the first version?
2. What user behavior would prove the app is useful?
3. What should the app help users do faster, better, cheaper, or with less stress?
4. What is the long-term vision?
5. What should remain true even if the product evolves?
```

---

## 6. Clarity threshold rules

LEAP should estimate clarity across ten dimensions.

Each dimension can be rated:

```text
0 = unclear
1 = partially clear
2 = clear enough for planning
```

The ten dimensions:

```text
1. Target user
2. Problem statement
3. Current workflow / alternative
4. Pain severity
5. Product thesis
6. Core workflow
7. MVP boundary
8. Non-goals
9. Risks and constraints
10. Success criteria
```

Total score:

```text
0 to 20 points
```

Suggested clarity band:

```text
0–12 points:
Below 67% clarity. Continue discovery.

13–15 points:
67% to 79% clarity. Draft concept brief allowed. Implementation planning not yet allowed.

16–20 points:
80%+ clarity. Implementation strategy and layer planning allowed after approval gate.
```

### Blocker rule

Some missing items block implementation even if the total score appears high.

Implementation planning is blocked if any of these are unclear:

```text
- target user
- problem statement
- MVP boundary
- non-goals
- sensitive data / risk profile
- human approval to proceed
```

---

## 7. Pressure-test method

The pressure test should answer:

```text
Why should this exist?
Why now?
Why would someone use this instead of what they already do?
What could make this fail?
What simpler solution might be better?
```

Required categories:

```text
1. Existing products
2. Substitute workflows
3. User adoption friction
4. Differentiation
5. MVP feasibility
6. Technical complexity
7. Data/privacy/security risks
8. Maintenance risks
9. Monetization or sustainability concerns
10. Adjacent opportunities
11. Reasons not to build
12. Recommendation
```

Pressure-test judgment labels:

```text
Strong candidate
Promising but unclear
Better as a smaller tool
Needs major rethink
Do not build yet
```

For real product concepts where current market conditions matter, LEAP should use current research before making claims about competitors or market alternatives.

---

## 8. MVP boundary method

The MVP boundary should be defined around the first useful outcome.

Recommended sequence:

```text
1. Identify the first user.
2. Identify the first painful workflow.
3. Identify the smallest useful improvement.
4. Identify the minimum features required to deliver that improvement.
5. Identify what can remain manual.
6. Identify what should be explicitly excluded.
7. Identify what could be added later.
```

MVP boundary template:

```text
# MVP Boundary

## First Useful User Outcome
## Must Include
## Should Include If Easy
## Must Not Include Yet
## Later Roadmap Candidates
## Manual for Now
## Validation Criteria
## Overbuild Risks
```

MVP guardrail:

```text
The MVP must not be defined as “build the whole platform, but basic.”
```

A good MVP is a thin, coherent workflow that proves value.

---

## 9. Documentation bootstrap structure

LEAP should create a lean documentation scaffold for new application repositories.

The goal is durable context, not paperwork.

Recommended structure:

```text
docs/
  README.md
  source-of-truth.md

  strategy/
    project-charter.md
    discovery-notes.md
    pressure-test.md
    mvp-boundary.md
    implementation-strategy.md

  architecture/
    decision-log.md

  layers/
    README.md

  execution/
    execution-log.md
```

### 9.1 Required starter docs

| File | Purpose | Canonical? | Required at Bootstrap? |
|---|---|---:|---:|
| `docs/README.md` | Entry point for project documentation | Yes | Yes |
| `docs/source-of-truth.md` | Identifies canonical docs and current authority | Yes | Yes |
| `docs/strategy/project-charter.md` | Defines product purpose, user, problem, and thesis | Yes | Yes |
| `docs/strategy/discovery-notes.md` | Records questions, answers, assumptions, and open issues | Supporting | Yes |
| `docs/strategy/pressure-test.md` | Records market, substitute, and feasibility pressure testing | Yes | Yes |
| `docs/strategy/mvp-boundary.md` | Defines MVP scope, non-goals, and overbuild risks | Yes | Yes |
| `docs/strategy/implementation-strategy.md` | Establishes initial technical and sequencing strategy | Yes | Once 80% clarity is reached |
| `docs/architecture/decision-log.md` | Tracks major architecture and product decisions | Yes | Yes |
| `docs/layers/README.md` | Defines project-specific LEAP layer structure | Yes | Before layer planning |
| `docs/execution/execution-log.md` | Tracks implementation history and agent/human actions | Yes | Yes |

### 9.2 Source-of-truth conflict rule

```text
If documentation conflicts with implementation reality, flag the conflict before proceeding.
If two documents conflict, prefer the document listed as canonical in source-of-truth.md.
If source-of-truth.md is stale, stop and request reconciliation.
```

---

## 10. No-build gate

LEAP must enforce a no-build gate before implementation planning or coding-agent prompting.

### 10.1 No-build rule

```text
LEAP must not produce a coding-agent prompt until Phase 0 is complete and the user has approved the transition to layer planning.
```

### 10.2 Required before layer planning

The following must exist:

```text
1. Project charter
2. Discovery notes
3. Pressure-test summary
4. MVP boundary
5. Implementation strategy
6. Source-of-truth index
7. Initial layer map
8. Open questions list
9. Human approval to proceed
```

### 10.3 Required before coding-agent prompt

The following must exist:

```text
1. Approved layer plan
2. Current source-of-truth check
3. Current repo reality check, if repo exists
4. Implementation scope
5. Files or areas to change
6. Files or areas not to change
7. Acceptance criteria
8. Testing expectations
9. Documentation update expectations
10. Rollback or risk notes, if relevant
```

### 10.4 Hard blockers

LEAP must refuse to generate implementation prompts when:

```text
- the target user is unknown
- the problem is unknown
- the MVP boundary is missing
- non-goals are missing
- the product handles sensitive data but risks are unexamined
- the user has not approved moving from planning to implementation
- the docs identify unresolved strategic conflicts
- the repo state is unknown but the prompt assumes implementation reality
```

---

## 11. Human approval gate

The approval gate is the final checkpoint before layer planning.

Approval packet template:

```text
# Phase 0 Approval Packet

## Product Direction
We are building [product] for [target user] to solve [problem].

## First Useful Outcome
The first version should help users [specific outcome].

## MVP Boundary
Must include:
- ...

Must not include:
- ...

## Key Risks
- ...

## Current Assumptions
- ...

## Documentation Created
- docs/README.md
- docs/source-of-truth.md
- docs/strategy/project-charter.md
- docs/strategy/discovery-notes.md
- docs/strategy/pressure-test.md
- docs/strategy/mvp-boundary.md
- docs/strategy/implementation-strategy.md
- docs/architecture/decision-log.md
- docs/layers/README.md
- docs/execution/execution-log.md

## Recommendation
Proceed to LEAP layer planning: Yes / No

## Approval Question
Do you approve this baseline direction and want LEAP to begin layer planning?
```

Approval must be explicit.

---

## 12. Documentation governance model

LEAP v1.4 recognizes five documentation classes.

### 12.1 Phase 0 inception documents

Examples:

```text
docs/strategy/project-charter.md
docs/strategy/discovery-notes.md
docs/strategy/pressure-test.md
docs/strategy/mvp-boundary.md
docs/strategy/implementation-strategy.md
docs/source-of-truth.md
```

Purpose:

- baseline direction
- product thesis
- target user and problem
- initial MVP boundary
- non-goals
- current assumptions
- initial implementation direction

Rules:

- Must exist before layer planning for new projects.
- Must separate confirmed facts from assumptions.
- Must be updated when the user intentionally changes direction.

### 12.2 Canonical strategic vision documents

Examples:

```text
docs/product-strategy.md
docs/layer-0-strategy.md
docs/platform-principles.md
```

Purpose:

- mission
- product principles
- governance posture
- durable architecture direction
- AI or automation boundaries
- monetization or operating philosophy

Rules:

- Keep these clean and durable.
- Do not accumulate implementation noise.
- Do not record per-commit details here.

### 12.3 Layer strategic plans

Examples:

```text
docs/layer-4-application-workflow-strategy.md
docs/layer-7-opportunity-model-strategy.md
docs/application-plan-and-layer-status.md
```

Purpose:

- layer goals
- subsystem boundaries
- architectural assumptions
- integration expectations
- layer completion state
- current best-known architectural truth

Update triggers:

- implementation changes layer status
- architecture evolves
- a Build Unit is deferred or superseded
- repo reality contradicts the plan
- cross-layer impact changes downstream assumptions

### 12.4 LEAP execution logs

Recommended application-repo directory:

```text
docs/execution/
```

Purpose:

- operational memory
- implementation telemetry
- architecture archaeology
- per-run auditability
- multi-agent coordination

### 12.5 Cross-layer dependency registry

Recommended application-repo file:

```text
docs/architecture/cross-layer-impact-map.md
```

Purpose:

- track shared entities and dependencies
- identify ripple effects
- support recon scanning
- prevent downstream layers from silently going stale

---

## 13. Repository boundary model

LEAP separates **framework methodology** from **application-specific planning**.

### Framework repository

The LEAP repository should contain:

- generic LEAP methodology
- reusable Phase 0 structure
- reusable LEAP Recon structure
- reusable LEAP Prompt structure
- reusable templates
- generic examples
- versioned framework documentation
- terminology and governance that applies across applications

### Application repository

The application repository should contain:

- application project charter
- application MVP boundary
- application pressure-test summary
- application roadmap
- application layer status
- application-specific product decisions
- application-specific domain model decisions
- application-specific LEAP Recon outputs
- application-specific LEAP Prompts
- implementation notes and application-specific architecture decisions
- execution logs
- cross-layer impact maps
- application-specific strategic plans

Rule of thumb:

```text
If the content describes how LEAP works for any application, store it in the LEAP repo.
If the content describes how a specific application should be built or what happened in that application, store it in that application repo.
```

---

## 14. LEAP Recon requirements in v1.4

LEAP Recon must now verify Phase 0 readiness before generating Build Units.

### 14.1 Phase 0 / source-of-truth gate check

```yaml
phase_0_gate_check:
  phase_0_required: true | false
  phase_0_complete: true | false | not_applicable
  project_charter_path: <path or not_found>
  mvp_boundary_path: <path or not_found>
  pressure_test_path: <path or not_found>
  source_of_truth_path: <path or not_found>
  initial_layer_map_path: <path or not_found>
  human_approval_status: approved | missing | unknown
  gate_result: proceed | continue_phase_0 | reconcile_docs_first
  reason: <why>
```

### 14.2 Strategic plan reconciliation

```yaml
strategic_plan_reconciliation:
  documents_reviewed:
    - <path>
  current_layer_status_claims:
    - <claim>
  repo_reality_alignment:
    - <aligned | stale | overclaimed | underclaimed | unknown>
  required_updates:
    - target_doc: <path>
      update_type: status | scope | architecture | dependency | todo | decision
      reason: <why the update is needed>
```

### 14.3 Cross-layer impact scan

```yaml
cross_layer_impact_scan:
  impact_map_reviewed: true | false
  impact_map_path: <path or not_found>
  change_areas:
    - <shared entity/workflow/service/API/model>
  impacted_layers:
    - layer: <Layer X>
      reason: <why this layer may be affected>
      required_follow_up: <none | doc_update | recon_required | implementation_required>
  stale_downstream_assumptions:
    - <assumption that may no longer hold>
```

### 14.4 Execution log expectations

```yaml
execution_log_expectations:
  execution_log_required: true | false
  recommended_path: docs/execution/<date>-<layer-or-build-unit>-results.md
  required_sections:
    - Objective
    - Scope
    - Completed Work
    - Architectural Discoveries
    - Cross-Layer Impacts
    - Technical Debt Introduced
    - TODO / Follow-On Work
    - Reconciliation Summary
```

---

## 15. LEAP Recon output template

```text
# LEAP Recon — <Target Layer>

## 1. Framework Interpretation
## 2. Phase 0 / Source-of-Truth Gate Check
## 3. Solution Context
## 4. Source-of-Truth Review
## 5. Repo Reality Reconciliation
## 6. Strategic Plan Reconciliation
## 7. Cross-Layer Impact Scan
## 8. Layer Intent
## 9. Pressure-Test Findings
## 10. Generated / Refined Build Unit Inventory
## 11. Recommended Build Sequence
## 12. Dependency Review
## 13. Architecture Right-Sizing Review
## 14. Data / Destructive-Change Review
## 15. Infrastructure Escalation Review
## 16. Layer Boundary Review
## 17. Execution Log Expectations
## 18. Coding-Agent Question Forecast
## 19. Recommended Prompt Settings
## 20. Clarification Questions Before LEAP Prompt Generation
## 21. Next Step
```

---

## 16. LEAP Prompt requirements in v1.4

Every LEAP Prompt must include these policies when application source-of-truth docs are present.

### 16.1 Phase 0 / no-build gate policy

```yaml
phase_0_no_build_gate_policy:
  phase_0_required_for_new_projects: true
  prompt_generation_blocked_when:
    - phase_0_required_but_missing
    - project_charter_missing
    - mvp_boundary_missing
    - explicit_non_goals_missing
    - source_of_truth_index_missing
    - recon_not_approved
    - unresolved_strategic_conflict
  proceed_only_when:
    - phase_0_complete_or_not_applicable
    - recon_approved
    - source_of_truth_review_complete
    - implementation_scope_defined
```

### 16.2 Strategic reconciliation policy

```yaml
strategic_reconciliation_policy:
  update_required: true
  update_when:
    - implementation changes layer status
    - repo reality contradicts the strategic plan
    - a Build Unit is completed, deferred, superseded, or materially changed
    - implementation reveals a new architectural constraint
    - implementation affects other layers
  preserve_separation:
    - keep strategic docs clean
    - put per-run implementation telemetry in execution logs
```

### 16.3 Execution log policy

```yaml
execution_log_policy:
  create_or_update_required: true
  recommended_directory: docs/execution/
  required_sections:
    - Objective
    - Scope
    - Completed Work
    - Architectural Discoveries
    - Cross-Layer Impacts
    - Technical Debt Introduced
    - TODO / Follow-On Work
    - Reconciliation Summary
```

### 16.4 Cross-layer impact policy

```yaml
cross_layer_impact_policy:
  inspect_required: true
  recommended_registry: docs/architecture/cross-layer-impact-map.md
  update_required_when:
    - shared entity boundaries change
    - cross-layer dependency changes
    - downstream assumptions become stale
    - future-layer work is discovered
```

---

## 17. LEAP Prompt output template

```text
# <Solution Name> — LEAP Prompt — <Target Layer>

## Purpose
## Prompt Settings
## Phase 0 / Source-of-Truth Gate Status
## Source-of-Truth Instructions
## Strategic Reconciliation Policy
## Execution Log Policy
## Cross-Layer Impact Policy
## Branch / Commit Instructions
## Plan Mode
## Destructive Change Policy
## Architecture Right-Sizing Policy
## Infrastructure Escalation Policy
## Layer Boundary Policy
## General Engineering Requirements
## Governance / Safety Requirements
## Per-Build Unit Execution Contract
## Per-Build Unit Completion Report
## Refined Build Unit Implementation Sequence
## Source-of-Truth Update Policy
## Post-Implementation Reconciliation Checklist
## Final Layer Completion Report
```

---

## 18. Operational cadence

Recommended defaults:

### Per Phase 0 project start

- capture original idea
- conduct Socratic discovery
- estimate clarity
- pressure test against existing and simpler alternatives
- define MVP boundary
- generate baseline strategy
- bootstrap docs
- get approval before layer planning

### Per Build Unit

- inspect repo before implementation
- implement the Build Unit
- commit the Build Unit independently
- update execution log
- identify source-of-truth deltas
- identify cross-layer impacts

### Per layer completion

- update layer strategic plan/status
- update cross-layer impact map if changed
- update debt/follow-up notes
- produce final layer completion report

### Weekly, biweekly, or milestone-based

- stale-plan scan
- branch drift review
- future prompt freshness review
- roadmap/status correction
- dependency map review

---

## 19. Versioning

LEAP uses:

```text
LEAP vMajor.Minor
```

Current version:

```text
LEAP v1.4
```

Minor versions refine the framework without changing its core identity.

Major versions change the framework structure or execution philosophy.

LEAP v1.4 is a minor version with a meaningful lifecycle change: it adds a mandatory inception phase before Recon for new projects.

---

## 20. v1.4 change summary

LEAP v1.4 adds:

- mandatory Phase 0 Inception
- Socratic discovery model
- directional clarity scoring
- market / alternative-solution pressure testing
- MVP boundary method
- documentation bootstrap requirements
- source-of-truth index requirement for new application repos
- no-build gate
- human approval gate before layer planning
- Phase 0 readiness check inside Recon
- Phase 0 / source-of-truth gate status inside LEAP Prompt

LEAP v1.4 changes the workflow from:

```text
LEAP Recon → LEAP Prompt
```

to:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

The short rule:

```text
No clarity, no build.
No source of truth, no agent handoff.
No MVP boundary, no implementation plan.
No approval, no coding prompt.
```
