# LEAP Framework Plan v1.5

## Framework name

**LEAP — Layer Execution & Assembly Protocol**

LEAP is a solution-level framework for turning rough software intent into pressure-tested direction, layered plans, and safe, bounded, implementation-ready AI coding prompts.

LEAP v1.5 hardens the v1.4 lifecycle. It keeps Phase 0 Inception, Recon, and Prompt, but makes the framework more explicitly gate-based, source-of-truth-aware, model-effort-aware, and safe for Codex-style coding agents.

The v1.5 lifecycle is:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

---

## 1. Core concept

```text
Phase 0 Inception = The mandatory project-start workflow that converts vague software intent into pressure-tested baseline direction.
Gate Decision = The explicit decision at the end of Phase 0 or Recon that determines whether LEAP proceeds, narrows, pressure-tests more, waits for a human, or stops.
Evidence Label = A label that separates known facts from assumptions, unknowns, contested claims, and decisions still needed.
Layer = A major system capability or architectural phase.
Build Unit = A scoped subsection of the layer that can be implemented and committed independently.
Source-of-Truth Document = An application-specific project charter, MVP boundary, roadmap/status/architecture file, or execution-state file that governs repo-specific decisions.
Execution Log = A per-run implementation record capturing what changed, what was discovered, and what follow-up is needed.
Cross-Layer Impact Map = A dependency registry that tracks which layers are affected by changes to shared entities, workflows, or architecture.
Model-Effort Tier = The selected LEAP depth: Standard, Pro Standard, or Pro Extended.
Stop Condition = A rule that tells the coding agent to stop and report instead of guessing.
LEAP = The framework that discovers, pressure-tests, designs, sequences, governs, prompt-generates, implements, and reconciles layered buildout.
```

LEAP v1.5 keeps the hard v1.4 rule:

> LEAP may help clarify vague ideas. LEAP may not convert vague ideas directly into implementation plans or coding-agent prompts.

LEAP v1.5 adds a second hard rule:

> A coding agent must receive a bounded task packet, not a broad wish.

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
9. evidence labels for knowns, assumptions, unknowns, contested claims, and decisions needed
10. lean starter documentation recommendation
11. source-of-truth index recommendation
12. gate decision before Recon

### 2.2 Stage 1 — LEAP Recon

LEAP Recon begins only after Phase 0 is complete or when an existing project already has enough source-of-truth documentation.

Recon analyzes the target layer, reconciles source-of-truth docs with repo reality, scans for stale assumptions, generates or refines Build Units, pressure-tests the plan, and identifies clarification needs before generating a coding prompt.

### 2.3 Stage 2 — LEAP Prompt

LEAP Prompt converts approved Recon findings into the final implementation prompt for Codex-style or another AI coding agent.

Prompt generation is blocked if Phase 0, source-of-truth, Recon approval, or implementation-scope requirements are not met.

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
- whether a software product is actually needed
- what simpler non-app solution could work first
- what the first useful version should accomplish
- what the app should explicitly avoid becoming
- what risks and constraints matter
- what docs must exist before implementation begins

Phase 0 is not a giant business-plan generator. It is a clarity and safety gate.

---

## 4. Phase 0 modes

LEAP v1.5 makes Phase 0 mode-aware.

| Mode | Use When | Output |
|---|---|---|
| Lite Inception | Bug fix, small feature, known project direction, low risk | Focused clarity check, evidence labels, gate decision |
| Standard Inception | New feature, unclear scope, early product idea, moderate risk | Problem, user, workflow, MVP, non-goals, risks, pressure test, gate decision |
| Pro Inception | New product, strategic pivot, sensitive data, major architecture, high-risk AI behavior, monetization, parallel agents | Full discovery, pressure test, documentation bootstrap, source-of-truth recommendation, human checkpoint plan, gate decision |

Default rule:

```text
Ask the fewest questions needed to make the next safe gate decision.
```

---

## 5. Phase 0 workflow

LEAP Phase 0 has eight stages. The depth of each stage depends on the selected mode.

```text
0.1 Idea Intake
0.2 Socratic Discovery
0.3 Evidence Labeling and Clarity Assessment
0.4 Market / Alternative Solution Pressure Test
0.5 MVP Boundary Definition
0.6 Strategic Plan Generation
0.7 Documentation Bootstrap Recommendation
0.8 Gate Decision
```

### 5.1 Idea Intake

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

### 5.2 Socratic Discovery

LEAP asks targeted follow-up questions in rounds.

Each round should include:

```text
- 3 to 8 high-leverage questions depending on mode
- short summary of what is now understood
- list of open uncertainties
- recommendation on whether another round is needed
```

LEAP should not dump 30 questions at once.

### 5.3 Evidence Labeling

Every Phase 0 pass should separate:

```text
Known = directly provided, observed, or confirmed.
Assumed = plausible but not confirmed.
Unknown = missing information.
Contested = conflicting information or likely disagreement.
Needs Decision = a human decision is required before safe progress.
```

A polished assumption is still an assumption.

### 5.4 Clarity Assessment

LEAP may estimate readiness using clarity bands.

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

The score is a planning signal, not a precise measurement. It must be paired with blocker status and evidence labels.

### 5.5 Market / Alternative Solution Pressure Test

LEAP pressure tests the idea against reality.

This includes:

```text
- existing products
- substitute workflows
- manual workarounds
- open-source alternatives
- internal-tool alternatives
- spreadsheet / no-code / automation alternatives
- process, service, checklist, template, or policy alternatives
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

Sometimes the better first solution is a workflow, spreadsheet, script, plugin, browser extension, Slack/Teams bot, dashboard, integration, checklist, coaching process, or manual service.

### 5.6 MVP Boundary Definition

LEAP defines the smallest useful version around the first meaningful user outcome.

Required sections:

```text
- one primary user
- one primary workflow
- one primary outcome
- one success signal
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

### 5.7 Strategic Plan Generation

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

### 5.8 Documentation Bootstrap Recommendation

LEAP recommends a lean starter documentation structure before detailed implementation planning.

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

Additional docs for new products or major features:

```text
docs/strategy/mvp-boundary.md
docs/strategy/pressure-test.md
```

Additional docs for multi-step, multi-agent, or long-running implementation:

```text
docs/strategy/implementation-strategy.md
docs/layers/README.md
docs/execution/execution-log.md
docs/architecture/cross-layer-impact-map.md
```

---

## 6. Gate decisions

Phase 0 and Recon should end with a gate decision, not just notes.

| Decision | Meaning |
|---|---|
| Proceed to Recon | Enough clarity exists to inspect repo/docs and plan implementation. |
| Pressure Test Further | The idea may be valid, but alternatives, risks, or market/context claims need more review. |
| Narrow MVP First | Direction is valid, but scope is too broad. |
| Needs Human Decision | A consequential product, risk, architecture, privacy, monetization, or implementation decision is unresolved. |
| Do Not Build Yet | Software is premature, unnecessary, risky, unsupported, or not the simplest useful next step. |

Gate rule:

```text
When LEAP would otherwise guess on a consequential decision, LEAP must stop and ask for human approval.
```

---

## 7. Clarity threshold rules

LEAP may estimate clarity across ten dimensions.

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

### False-precision rule

Do not let a clarity score hide uncertainty.

Every score must be accompanied by:

```text
- evidence labels
- blockers
- assumptions
- human decisions needed
- confidence notes
```

---

## 8. Pressure-test method

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
3. Manual, spreadsheet, checklist, template, service, process, or policy alternatives
4. User adoption friction
5. Differentiation
6. MVP feasibility
7. Technical complexity
8. Data/privacy/security risks
9. Maintenance risks
10. Monetization or sustainability concerns
11. Adjacent opportunities
12. Reasons not to build
13. Recommendation
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

## 9. MVP boundary method

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
## Primary User
## Primary Workflow
## Primary Success Signal
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

## 10. Documentation bootstrap structure

LEAP should create a lean documentation scaffold for new application repositories.

The goal is durable context, not paperwork.

### 10.1 Required starter docs

| File | Purpose | Required at Bootstrap? |
|---|---|---:|
| `docs/README.md` | Entry point for project documentation and update rules | Yes |
| `docs/source-of-truth.md` | Identifies canonical docs, ownership, freshness, and conflict resolution | Yes |
| `docs/strategy/project-charter.md` | Defines product purpose, user, problem, and thesis | Yes for new products |
| `docs/architecture/decision-log.md` | Tracks major architecture and product decisions | Yes; can start empty |

### 10.2 Conditional docs

| File | Use When |
|---|---|
| `docs/strategy/discovery-notes.md` | Discovery is substantial enough to preserve question/answer history. |
| `docs/strategy/pressure-test.md` | New product, major feature, high uncertainty, or market/alternative-solution risk. |
| `docs/strategy/mvp-boundary.md` | New product or meaningful product workflow. Can be combined with project charter for small projects. |
| `docs/strategy/implementation-strategy.md` | Multi-step implementation, architectural sequencing, or parallel work. |
| `docs/layers/README.md` | Project uses explicit LEAP layers. |
| `docs/execution/execution-log.md` | Long-running work, multi-agent work, or implementation telemetry needs preserving. |
| `docs/architecture/cross-layer-impact-map.md` | Shared entities, APIs, workflows, models, or layers can drift across workstreams. |

### 10.3 Source-of-truth conflict rule

```text
If documentation conflicts with implementation reality, flag the conflict before proceeding.
If two documents conflict, prefer the document listed as canonical in source-of-truth.md.
If source-of-truth.md is stale, stop and request reconciliation.
```

### 10.4 Stale-doc prevention rules

Every durable doc should state:

```text
- owner
- last meaningful update
- status: canonical | supporting | archived
- what truth it owns
- when it must be updated
```

No two docs should own the same truth.

---

## 11. No-build gate

LEAP must enforce a no-build gate before implementation planning or coding-agent prompting.

### 11.1 No-build rule

```text
LEAP must not produce a coding-agent prompt until Phase 0 is complete, the user has approved the transition to layer planning, Recon has passed, and implementation scope is bounded.
```

### 11.2 Required before layer planning

The following must exist:

```text
1. Project charter or equivalent baseline strategy
2. MVP boundary or explicit scope boundary
3. Pressure-test summary when the idea is new or strategically material
4. Source-of-truth index or explicit source-of-truth list
5. Open questions list
6. Human approval to proceed
```

### 11.3 Required before coding-agent prompt

The following must exist:

```text
1. Approved layer plan or task scope
2. Current source-of-truth check
3. Current repo reality check, if repo exists
4. Implementation objective
5. User-visible outcome
6. Files or areas to inspect
7. Files or areas not to change
8. In-scope items
9. Out-of-scope items and non-goals
10. Acceptance criteria
11. Testing expectations
12. Documentation update expectations
13. Stop conditions
14. Rollback or risk notes, if relevant
```

### 11.4 Hard blockers

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
- the implementation requires architecture, dependency, migration, auth, permissions, billing, AI behavior, or sensitive-data decisions that have not been approved
```

---

## 12. Human approval checkpoints

LEAP requires explicit human approval before:

```text
- building from unresolved vague intent
- expanding MVP scope
- violating non-goals
- changing product thesis
- changing source-of-truth docs that own strategy
- making durable architecture decisions
- adding external integrations
- changing auth, permissions, roles, billing, pricing, monetization, or ranking incentives
- collecting, exposing, inferring, or storing sensitive data in a new way
- adding or changing AI behavior that affects user trust, user claims, recommendations, or automation
- introducing destructive migrations
- launching parallel agents that touch overlapping files or layers
- proceeding when docs and repo reality conflict
```

The checkpoint rule is blunt:

```text
When the agent would otherwise guess on a consequential decision, LEAP must stop.
```

---

## 13. LEAP Recon requirements in v1.5

LEAP Recon must now verify Phase 0 readiness and source-of-truth quality before generating Build Units.

### 13.1 Phase 0 / source-of-truth gate check

```yaml
phase_0_gate_check:
  phase_0_required: true | false
  phase_0_mode: lite | standard | pro | not_applicable
  phase_0_complete: true | false | not_applicable
  project_charter_path: <path or not_found>
  mvp_boundary_path: <path or not_found>
  pressure_test_path: <path or not_found>
  source_of_truth_path: <path or not_found>
  initial_layer_map_path: <path or not_found>
  human_approval_status: approved | missing | unknown
  evidence_labels_present: true | false
  gate_result: proceed | continue_phase_0 | narrow_mvp | pressure_test_further | needs_human_decision | do_not_build_yet | reconcile_docs_first
  reason: <why>
```

### 13.2 Source-of-truth discovery

```yaml
source_of_truth_discovery:
  documents_reviewed:
    - path: <path>
      status: canonical | supporting | archived | unknown
      owner: <owner or unknown>
      last_meaningful_update: <date or unknown>
      truth_owned: <strategy | mvp | architecture | layer_status | execution_state | decisions | other>
  conflicts:
    - <conflict>
  missing_canonical_truths:
    - <missing source of truth>
```

### 13.3 Repo reality reconciliation

```yaml
repo_reality_reconciliation:
  branch_reviewed: <branch>
  recent_changes_reviewed: true | false
  package_scripts_reviewed: true | false
  tests_reviewed: true | false
  dependencies_reviewed: true | false
  migrations_reviewed: true | false
  existing_patterns_reviewed: true | false
  docs_vs_code_alignment:
    - aligned | stale | overclaimed | underclaimed | unknown
  required_updates:
    - target_doc: <path>
      update_type: status | scope | architecture | dependency | todo | decision
      reason: <why the update is needed>
```

### 13.4 Stale assumption scan

```yaml
stale_assumption_scan:
  stale_docs:
    - <path and reason>
  stale_assumptions:
    - <assumption>
  assumptions_to_revalidate:
    - <assumption>
  prompt_risks_if_not_reconciled:
    - <risk>
```

### 13.5 Cross-layer impact scan

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

---

## 14. LEAP Recon output template

```text
# LEAP Recon — <Target Layer>

## 1. Framework Interpretation
## 2. Phase 0 / Source-of-Truth Gate Check
## 3. Solution Context
## 4. Source-of-Truth Discovery
## 5. Source-of-Truth Review
## 6. Repo Reality Reconciliation
## 7. Branch / Worktree Drift Review
## 8. Strategic Plan Reconciliation
## 9. Stale Assumption Scan
## 10. Cross-Layer Impact Scan
## 11. Layer Intent
## 12. Pressure-Test Findings
## 13. Generated / Refined Build Unit Inventory
## 14. Recommended Build Sequence
## 15. Dependency Review
## 16. Architecture Right-Sizing Review
## 17. Data / Destructive-Change Review
## 18. Infrastructure Escalation Review
## 19. Layer Boundary Review
## 20. Human Checkpoints Required
## 21. Execution Log Expectations
## 22. Coding-Agent Question Forecast
## 23. Recommended Model-Effort and Prompt Settings
## 24. Clarification Questions Before LEAP Prompt Generation
## 25. Gate Decision / Next Step
```

---

## 15. LEAP Prompt requirements in v1.5

Every LEAP Prompt must be a bounded implementation packet.

### 15.1 Required prompt skeleton

```text
# <Solution Name> — LEAP Prompt — <Target Layer or Task>

## Task
- Objective:
- User-visible outcome:
- Source of truth:

## Scope
- In scope:
- Out of scope:
- Non-goals:
- Files/areas to inspect:
- Files/areas not to touch:

## Constraints
- Existing patterns to follow:
- Dependencies allowed/disallowed:
- Architecture constraints:
- Data/privacy/security constraints:
- AI behavior constraints, if relevant:

## Implementation Guidance
- Suggested sequence:
- Edge cases:
- Error handling:
- Accessibility/UX notes, if relevant:
- Backward compatibility:

## Verification
- Tests to run:
- Manual checks:
- Expected result:

## Stop Conditions
- Stop if docs conflict with code.
- Stop if scope requires architecture not approved.
- Stop if sensitive data handling is unclear.
- Stop if implementation requires a new dependency, migration, auth/permission change, billing change, or AI behavior change not approved.

## Output Required
- Summary of changes.
- Tests run.
- Files changed.
- Deviations from prompt.
- Docs that need updating.
```

### 15.2 Phase 0 / no-build gate policy

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
    - implementation_scope_unbounded
    - stop_conditions_missing
  proceed_only_when:
    - phase_0_complete_or_not_applicable
    - recon_approved
    - source_of_truth_review_complete
    - implementation_scope_defined
    - verification_plan_defined
```

### 15.3 Strategic reconciliation policy

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

### 15.4 Execution log policy

```yaml
execution_log_policy:
  create_or_update_required: true | false | conditional
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

### 15.5 Cross-layer impact policy

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

## 16. Parallel-agent and parallel-worktree guidance

Parallel LEAP work is allowed only when scopes are separable.

For parallel work, LEAP requires:

```text
1. one task packet per agent
2. one branch or worktree per task
3. no overlapping file ownership unless explicitly approved
4. shared source-of-truth packet
5. merge order
6. cross-agent conflict review
7. final strategy-drift check
```

Parallelism is useful for independent work. It is dangerous for overlapping architecture, shared data-model changes, auth/permission changes, migrations, or product-scope changes.

---

## 17. Model-selection guidance

LEAP process depth should match ambiguity, risk, and blast radius.

| Tier | Use For | LEAP Depth |
|---|---|---|
| Standard | Bug fixes, small UI changes, simple refactors, known implementation tasks | Lite Phase 0 if needed, focused Recon, compact Prompt |
| Pro Standard | New features, unclear scope, product workflow changes, moderate architecture impact | Standard Phase 0, pressure test, source-of-truth check, full Recon, bounded Prompt |
| Pro Extended | New product, major architecture, sensitive data, parallel agents, strategic pivot, monetization, high-risk AI behavior | Full Phase 0, deep pressure test, docs bootstrap, risk review, human checkpoints, parallel coordination |

Default rule:

```text
Do not use maximum process for routine work.
Do not under-process strategic or high-risk work.
```

---

## 18. Structured scoring and STRIDE-style evaluation guidance

When a project uses a structured scoring model, such as STRIDE-style evaluation, LEAP treats the score as advisory.

Structured evaluation must:

```text
- expose rationale
- preserve uncertainty
- identify missing evidence
- separate facts from assumptions
- avoid pretending that incomplete evidence creates objective truth
- allow human override or annotation when applicable
```

Scoring is decision support, not a substitute for judgment.

---

## 19. Operational cadence

Recommended defaults:

### Per Phase 0 project start

- capture original idea
- conduct Socratic discovery at the correct mode depth
- label facts and assumptions
- estimate clarity without false precision
- pressure test against existing and simpler alternatives
- define MVP boundary
- generate baseline strategy
- recommend lean docs
- make a gate decision

### Per Recon

- inspect source-of-truth docs
- classify docs as canonical, supporting, archived, or unknown
- inspect repo before implementation planning
- inspect branch/worktree drift when available
- scan for stale assumptions
- generate or refine Build Units
- identify human checkpoints
- make a gate decision before prompt generation

### Per Build Unit

- inspect repo before implementation
- implement the Build Unit
- commit the Build Unit independently when feasible
- update execution log if required
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

## 20. Versioning

LEAP uses:

```text
LEAP vMajor.Minor
```

Current version:

```text
LEAP v1.5
```

Minor versions refine the framework without changing its core identity.

Major versions change the framework structure or execution philosophy.

LEAP v1.5 is a minor hardening release. It preserves the v1.4 lifecycle while tightening gates, source-of-truth control, stale-assumption detection, documentation bootstrap, model-effort selection, and agent-safe prompt structure.

---

## 21. v1.5 change summary

LEAP v1.5 adds:

- gate-based Phase 0 decisions
- Lite / Standard / Pro Inception modes
- evidence labels for knowns, assumptions, unknowns, contested claims, and human decisions
- clarity scoring as advisory rather than false precision
- stronger simpler non-app alternative review
- stricter MVP boundary rules
- leaner documentation bootstrap tiers
- canonical / supporting / archived source-of-truth classification
- source-of-truth ownership and stale-doc rules
- stale-assumption scanning in Recon
- branch/worktree drift review in Recon
- human checkpoint triggers
- model-effort tiers
- bounded coding-agent prompt packets
- explicit stop conditions
- parallel-agent/worktree coordination rules
- structured scoring and STRIDE-style advisory-score guidance

The short rule:

```text
No clarity, no build.
No source of truth, no agent handoff.
No MVP boundary, no implementation plan.
No approval, no coding prompt.
No stop conditions, no agent task.
```
