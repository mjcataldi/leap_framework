# LEAP Framework Plan v1.3

## Framework name

**LEAP — Layer Execution & Assembly Protocol**

LEAP is a solution-level framework for turning a layered system concept into safe, sequential, implementation-ready AI coding prompts.

LEAP v1.3 extends LEAP from a layer implementation workflow into a living architecture governance system. It preserves the two-stage model:

```text
LEAP Recon → LEAP Prompt
```

but adds strategic reconciliation, cross-layer impact tracking, execution logging, and regular source-of-truth maintenance.

---

## 1. Core concept

```text
Layer = A major system capability or architectural phase.
Build Unit = A scoped subsection of the layer that can be implemented and committed independently.
Source-of-Truth Document = An application-specific roadmap/status/architecture file that governs repo-specific decisions.
Execution Log = A per-run implementation record capturing what changed, what was discovered, and what follow-up is needed.
Cross-Layer Impact Map = A dependency registry that tracks which layers are affected by changes to shared entities, workflows, or architecture.
LEAP = The framework that designs, sequences, governs, pressure-tests, prompt-generates, implements, and reconciles layered buildout.
```

---

## 2. Strategic reconciliation philosophy

LEAP must not treat planning documents as static specifications.

Instead:

> Strategy defines direction. Implementation reveals reality. Reconciliation keeps the system truthful.

Every LEAP run should preserve the distinction between:

- **Strategic intent** — what the architecture and roadmap intend.
- **Implementation reality** — what the repository actually contains.
- **Execution telemetry** — what happened during a specific LEAP/Codex run.
- **Cross-layer impact** — what changed outside the target layer’s immediate scope.

The goal is to prevent roadmap drift, stale assumptions, duplicate implementation, and cross-layer breakage as multiple agents, worktrees, branches, or Build Units evolve the system.

---

## 3. Documentation governance model

LEAP v1.3 recognizes four documentation classes.

### 3.1 Canonical strategic vision documents

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

Update frequency:

- infrequent
- major pivots
- quarterly or milestone review

Rules:

- Keep these clean and durable.
- Do not accumulate implementation noise.
- Do not record per-commit details here.

### 3.2 Layer strategic plans

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

Rules:

- Keep these implementation-informed but readable.
- Update after meaningful layer changes, not every small commit.
- Prefer concise status updates over noisy execution details.

### 3.3 LEAP execution logs

Recommended application-repo directory:

```text
docs/execution/
```

Example files:

```text
docs/execution/2026-05-20-layer4-bu-4.3-results.md
docs/execution/2026-05-20-layer7-recon-results.md
```

Purpose:

- operational memory
- implementation telemetry
- architecture archaeology
- per-run auditability
- multi-agent coordination

Each execution log should include:

```markdown
# LEAP Execution Log — <Target Layer / Build Unit>

## Objective
## Scope
## Completed Work
## Architectural Discoveries
## Cross-Layer Impacts
## Technical Debt Introduced
## TODO / Follow-On Work
## Reconciliation Summary
```

Execution logs are intentionally more detailed and historical than strategy docs.

### 3.4 Cross-layer dependency registry

Recommended application-repo file:

```text
docs/architecture/cross-layer-impact-map.md
```

Purpose:

- track shared entities and dependencies
- identify ripple effects
- support recon scanning
- prevent downstream layers from silently going stale

Example structure:

| Change Area | Impacted Layers | Reason |
|---|---|---|
| Opportunity schema | Layers 2, 3, 4, 5, 7, 8 | Shared intake, evaluation, workflow, analytics, and integration object |
| STRIDE engine | Layers 3, 5, 6, 9 | Evaluation, insights, artifacts, and automation depend on it |
| Resume artifacts | Layers 3, 4, 6, 8 | Workflow, lifecycle, export, and integrations depend on artifact state |
| Search tracks/workspaces | Most layers | Core organizational primitive |

---

## 4. Repository boundary model

LEAP separates **framework methodology** from **application-specific planning**.

### Framework repository

The LEAP repository should contain:

- generic LEAP methodology
- reusable LEAP Recon structure
- reusable LEAP Prompt structure
- reusable templates
- generic examples
- versioned framework documentation
- terminology and governance that applies across applications

### Application repository

The application repository should contain:

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

## 5. Two-stage LEAP workflow

```text
LEAP Recon → LEAP Prompt
```

### Stage 1 — LEAP Recon

LEAP Recon is the analysis, source-of-truth reconciliation, repo scan, pressure-test, Build Unit design, sequencing, cross-layer impact review, and clarification stage.

It produces:

1. solution and layer interpretation
2. source-of-truth document review
3. repo reality reconciliation
4. strategic plan reconciliation
5. cross-layer impact scan
6. pressure-test findings
7. generated or refined Build Unit inventory
8. recommended build sequence
9. dependency review
10. architecture right-sizing review
11. data/destructive-change review
12. infrastructure escalation review
13. layer boundary review
14. coding-agent question forecast
15. clarification questions for the user
16. recommended prompt settings
17. reminder to generate the LEAP Prompt

LEAP Recon should not generate the full implementation prompt unless explicitly asked.

### Stage 2 — LEAP Prompt

LEAP Prompt converts the approved LEAP Recon into a comprehensive implementation prompt for Codex or another AI coding agent.

It includes:

- coding-agent context
- source-of-truth document instructions
- target branch
- buildout mode
- plan/no-plan instruction
- reasoning effort recommendation
- per-Build Unit execution contract
- branch/commit policy
- architecture escalation policy
- destructive-change policy
- source-of-truth update policy
- execution log policy
- cross-layer impact policy
- full refined Build Unit implementation sequence
- per-Build Unit completion report schema
- final layer completion report schema

---

## 6. Required LEAP Recon additions in v1.3

LEAP Recon must now explicitly answer these questions.

### 6.1 Strategic plan reconciliation

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

### 6.2 Cross-layer impact scan

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

### 6.3 Execution log expectations

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

### 6.4 Regular reconciliation cadence

```yaml
reconciliation_cadence:
  per_build_unit:
    - execution log update
    - source-of-truth delta check
    - cross-layer impact check
  per_layer_completion:
    - layer strategic plan update
    - dependency registry review
    - technical debt review
  regular_review:
    cadence: weekly | biweekly | milestone-based | project-specific
    actions:
      - stale-plan scan
      - branch drift review
      - roadmap/status correction
      - dependency map update
```

---

## 7. Required LEAP Prompt additions in v1.3

Every LEAP Prompt must include these policies when application source-of-truth docs are present.

### 7.1 Strategic reconciliation policy

```yaml
strategic_reconciliation_policy:
  update_required: true
  update_when:
    - implementation changes layer status
    - repo reality contradicts the strategic plan
    - a Build Unit is completed, deferred, superseded, or materially changed
    - implementation reveals a new architectural constraint
    - implementation affects other layers
  update_scope:
    - application-specific strategic plans
    - layer status documents
    - architecture decision docs when applicable
  preserve_separation:
    - keep strategic docs clean
    - put per-run implementation telemetry in execution logs
```

### 7.2 Execution log policy

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

### 7.3 Cross-layer impact policy

```yaml
cross_layer_impact_policy:
  inspect_required: true
  recommended_registry: docs/architecture/cross-layer-impact-map.md
  update_required_when:
    - shared entity boundaries change
    - cross-layer dependency changes
    - downstream assumptions become stale
    - future-layer work is discovered
  report_required_when:
    - an impacted layer needs a future Recon pass
    - the impact map does not exist yet
    - the coding agent cannot safely determine downstream implications
```

### 7.4 Post-implementation reconciliation checklist

```yaml
post_implementation_reconciliation:
  required_before_final_report:
    - update execution log
    - update affected layer strategic plan/status doc
    - update cross-layer impact map if changed
    - record technical debt or follow-up work
    - identify downstream layer risks
    - report any stale Build Units or stale future prompts
```

---

## 8. Source-of-truth document handling

When source-of-truth documents are supplied, LEAP Recon must:

1. Read them before generating Build Units.
2. Treat them as higher priority than chat memory.
3. Reconcile them against the current repository state when repo access is available.
4. Flag stale, conflicting, or overclaimed status.
5. Use them to avoid rebuilding existing capabilities.
6. Use them to constrain layer boundaries and non-goals.
7. Recommend updates when implementation reality has changed.
8. Identify cross-layer impacts when changes affect shared entities or future layers.
9. Distinguish between strategy-doc updates and execution-log updates.

If a source-of-truth document conflicts with repo reality, repo reality wins for implementation planning, but LEAP must explicitly report the conflict and recommend a documentation update.

---

## 9. LEAP Recon output template

```text
# LEAP Recon — <Target Layer>

## 1. Framework Interpretation
## 2. Solution Context
## 3. Source-of-Truth Review
## 4. Repo Reality Reconciliation
## 5. Strategic Plan Reconciliation
## 6. Cross-Layer Impact Scan
## 7. Layer Intent
## 8. Pressure-Test Findings
## 9. Generated / Refined Build Unit Inventory
## 10. Recommended Build Sequence
## 11. Dependency Review
## 12. Architecture Right-Sizing Review
## 13. Data / Destructive-Change Review
## 14. Infrastructure Escalation Review
## 15. Layer Boundary Review
## 16. Execution Log Expectations
## 17. Coding-Agent Question Forecast
## 18. Recommended Prompt Settings
## 19. Clarification Questions Before LEAP Prompt Generation
## 20. Next Step
```

---

## 10. LEAP Prompt output template

```text
# <Solution Name> — LEAP Prompt — <Target Layer>

## Purpose
## Prompt Settings
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

## 11. Recommended application-repo files

LEAP v1.3 recommends, but does not require, the following application-repo structure:

```text
docs/
  application-plan-and-layer-status.md
  strategic-layer-roadmap.md
  architecture/
    cross-layer-impact-map.md
    decisions/
      <adr-files>.md
  execution/
    <date>-<layer-or-build-unit>-results.md
```

If the application repo does not yet have these files, the LEAP Prompt should instruct the coding agent to create them only when doing so is relevant to the current buildout and does not create documentation noise.

---

## 12. Operational cadence

Recommended defaults:

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

## 13. Versioning

LEAP uses:

```text
LEAP vMajor.Minor
```

Current version:

```text
LEAP v1.3
```

Minor versions refine the framework without changing its core two-stage model.

Major versions change the framework structure or execution philosophy.

---

## 14. v1.3 change summary

LEAP v1.3 adds:

- living architecture governance
- strategic plan reconciliation
- execution logs
- cross-layer impact mapping
- post-implementation reconciliation checklist
- regular reconciliation cadence
- clearer separation between strategic intent and implementation reality
- stronger support for multi-agent, multi-branch, and multi-worktree workflows

LEAP v1.3 keeps the same two-stage model as v1.2:

```text
LEAP Recon → LEAP Prompt
```
