# LEAP Framework Plan v1.2

## Framework name

**LEAP — Layer Execution & Assembly Protocol**

LEAP is a solution-level framework for turning a layered system concept into safe, sequential, implementation-ready AI coding prompts.

It can be used for software systems, product platforms, internal tools, data systems, AI applications, infrastructure buildouts, or modular engineering initiatives that benefit from layer-by-layer implementation.

LEAP takes a user’s high-level solution intent, application-specific source-of-truth material, and target layer, builds out the right-sized implementation subsections for that layer, pressure-tests them, and then converts the approved plan into a comprehensive implementation prompt.

---

## 1. Core concept

```text
Layer = A major system capability or architectural phase.
Build Unit = A scoped subsection of the layer that can be implemented and committed independently.
Source-of-Truth Document = An application-specific roadmap/status/architecture file that governs repo-specific decisions.
LEAP = The framework that designs, sequences, governs, pressure-tests, and prompt-generates the layer buildout.
```

---

## 2. Build Unit naming

LEAP uses **Build Unit** as the atomic implementation subsection.

A Build Unit is a bounded piece of layer functionality that can be scoped, implemented, tested, and committed independently.

Use shorthand `BU` only where space is tight. In prompts, prefer the full phrase **Build Unit**.

---

## 3. Two-stage LEAP workflow

```text
LEAP Recon → LEAP Prompt
```

### Stage 1 — LEAP Recon

LEAP Recon is the analysis, source-of-truth reconciliation, pressure-test, Build Unit design, sequencing, and clarification stage.

It produces:

1. solution and layer interpretation
2. source-of-truth document review
3. repo reality reconciliation
4. pressure-test findings
5. generated or refined Build Unit inventory
6. recommended build sequence
7. dependency review
8. architecture right-sizing review
9. data/destructive-change review
10. infrastructure escalation review
11. layer boundary review
12. coding-agent question forecast
13. clarification questions for the user
14. recommended prompt settings
15. reminder to generate the LEAP Prompt

LEAP Recon should not generate the full implementation prompt unless explicitly asked.

### Stage 2 — LEAP Prompt

LEAP Prompt is the implementation-prompt artifact stage.

It converts the approved LEAP Recon into a comprehensive prompt for Codex or another AI coding agent.

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
- full refined Build Unit implementation sequence
- per-Build Unit completion report schema
- final layer completion report schema

---

## 4. Repository boundary model

LEAP separates **framework methodology** from **application-specific planning**.

### Framework repository

The LEAP repository should contain:

- generic LEAP methodology
- LEAP Recon structure
- LEAP Prompt structure
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
- implementation notes and architecture decisions specific to that application

### Rule of thumb

```text
If the content describes how LEAP works for any application, store it in the LEAP repo.
If the content describes how a specific application should be built, store it in that application repo.
```

LEAP Recon and LEAP Prompt should preserve this boundary unless the user explicitly instructs otherwise.

---

## 5. Source-of-truth document handling

A source-of-truth document is an application-specific file that records current status, roadmap decisions, layer definitions, architecture decisions, or implementation boundaries.

Examples:

```text
docs/application-plan-and-layer-status.md
docs/strategic-layer-roadmap.md
docs/domain-model-strategy.md
docs/architecture-decisions.md
```

When source-of-truth documents are supplied, LEAP Recon must:

1. Read them before generating Build Units.
2. Treat them as higher priority than chat memory.
3. Reconcile them against the current repository state when repo access is available.
4. Flag stale, conflicting, or overclaimed status.
5. Use them to avoid rebuilding existing capabilities.
6. Use them to constrain layer boundaries and non-goals.
7. Recommend updates when implementation reality has changed.

If a source-of-truth document conflicts with repo reality, repo reality wins for implementation planning, but LEAP should explicitly report the conflict and recommend a documentation update.

---

## 6. Workflow summary

```text
User provides:
- solution/system overview
- source-of-truth documents if available
- combined target layer identifier and name
- optional branch name, or branch naming preference
- buildout mode
- known constraints
- optional Build Unit sketches if already available

Assistant runs:
- LEAP Recon

Assistant returns:
- layer interpretation
- source-of-truth review
- repo reality reconciliation
- pressure-test findings
- generated/refined Build Unit inventory
- build sequence
- dependency review
- architecture right-sizing review
- data/destructive-change review
- infrastructure escalation review
- layer boundary review
- likely coding-agent questions
- clarification questions for the user
- recommended prompt settings
- reminder to generate the LEAP Prompt

User answers questions or approves defaults.

Assistant generates:
- LEAP Prompt

User runs:
- Codex or another AI coding agent implementation on target branch
```

---

## 7. Framework hierarchy

```text
Solution Strategy
└── Source-of-Truth Documents
    └── Layer Roadmap
        └── LEAP Package for Layer X
            ├── Stage 1: LEAP Recon
            │   ├── Solution Context
            │   ├── Source-of-Truth Review
            │   ├── Repo Reality Reconciliation
            │   ├── Layer Intent
            │   ├── Pressure-Test Findings
            │   ├── Build Unit Generation / Refinement
            │   ├── Build Sequence
            │   ├── Dependency Review
            │   ├── Architecture Right-Sizing Review
            │   ├── Data / Migration Review
            │   ├── Infrastructure Escalation Review
            │   ├── Layer Boundary Review
            │   ├── Coding-Agent Question Forecast
            │   ├── User Clarification Questions
            │   └── Prompt Settings Recommendation
            │
            └── Stage 2: LEAP Prompt
                ├── Coding-Agent Context
                ├── Source-of-Truth Instructions
                ├── Branch / Commit Rules
                ├── Plan Mode
                ├── Reasoning Effort
                ├── Per-Build Unit Execution Contract
                ├── Refined Build Unit Inventory
                ├── Per-Build Unit Commit Contract
                ├── Source-of-Truth Update Policy
                ├── Per-Build Unit Completion Report
                ├── Final Layer Completion Report
                └── Manual Follow-Up Requirements
```

---

## 8. LEAP Recon schema

### 8.1 Recon header

```yaml
framework: LEAP
framework_version: 1.2
stage: Recon
stage_name: LEAP Reconnaissance Pass
solution_name: <solution/system name>
target_layer: <combined layer identifier and layer name>
branch: <branch name or generated default>
buildout_mode: Rapid POC | Standard | Production-safe | Refactor
prompt_generation: deferred
```

### 8.2 Solution context

```yaml
solution_context:
  solution_name: <name>
  solution_type: <product/platform/internal tool/data system/etc.>
  high_level_goal: <what the system is trying to accomplish>
  current_state:
    - <what exists already>
  known_constraints:
    - <technical/product/process constraint>
  repo_context:
    - <known repository facts>
```

### 8.3 Source-of-truth review

```yaml
source_of_truth_review:
  documents_reviewed:
    - path: <repo path or URL>
      role: roadmap | layer_status | architecture | domain_model | other
      relevance: high | medium | low
  key_decisions:
    - <decision from source-of-truth document>
  current_status_claims:
    - <claim from document>
  constraints_from_documents:
    - <constraint>
  recommended_doc_updates:
    - <update if implementation reality appears different>
```

### 8.4 Repo reality reconciliation

When repo access is available, LEAP Recon should inspect the repository enough to avoid stale planning.

```yaml
repo_reality_reconciliation:
  repo_inspected: true | false
  inspected_areas:
    - <files/directories/APIs/models/tests/docs inspected>
  confirmed_existing_capabilities:
    - <capability confirmed in repo>
  partially_built_or_drifted_capabilities:
    - <capability that exists but is incomplete or branch-diverged>
  missing_capabilities:
    - <capability not found>
  conflicts_with_source_of_truth:
    - claim: <source-of-truth claim>
      repo_reality: <observed repo state>
      recommendation: <how to handle>
```

If repo access is not available, LEAP must say so and avoid pretending it verified implementation reality.

### 8.5 Layer intent

```yaml
layer_intent:
  target_layer: <combined layer identifier and layer name>
  purpose: <what this layer accomplishes>
  user_or_system_value:
    - <value 1>
    - <value 2>
    - <value 3>
  primary_transition: <what changes from the prior layer>
  non_goals:
    - <non-goal 1>
    - <non-goal 2>
```

### 8.6 Buildout mode assessment

```yaml
buildout_mode:
  selected_mode: Rapid POC | Standard | Production-safe | Refactor
  planning_depth: LEAP Recon first; LEAP Prompt second
  sequential_execution: true
  one_build_unit_per_commit: true
  destructive_changes_allowed: true | false
  production_migration_discipline: true | false
  backward_compatibility_required: true | false
  source_of_truth_updates_required: true | false
  optimize_for:
    - working vertical slices
    - coherent domain model
    - repository consistency
    - speed with guardrails
  avoid:
    - speculative architecture
    - hand-jamming into bad fit
    - unnecessary production ceremony
    - future-layer work
    - rebuilding existing capabilities
```

### 8.7 Branch naming policy

If the user provides a branch name, use it.

If no branch name is provided, generate a default from the layer identifier and a short layer definition.

Default format:

```text
layer<number>_<definition>
```

Rules:

- lowercase
- snake_case
- maximum four descriptive words after the layer number
- remove filler words
- prefer capability nouns
- keep it repo-safe and easy to type

Examples:

```text
layer5_insights_optimization
layer6_artifact_lifecycle
layer7_opportunity_model
layer4_application_workflow
layer2_intake_parsing
```

### 8.8 Pressure-test rubric

LEAP Recon must include a pressure-test section. This is not optional.

The pressure test should assess whether the target layer and generated Build Units are safe, useful, properly bounded, and implementable against current repo reality.

```yaml
pressure_test_findings:
  repo_reality_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  already_built_collision_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  branch_drift_check:
    rating: pass | caution | fail | not_checked
    findings:
      - <finding>
  layer_boundary_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  build_unit_atomicity_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  dependency_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  migration_destructive_change_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  frontend_backend_api_alignment_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  testability_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  truthfulness_or_source_grounding_check:
    rating: pass | caution | fail | not_applicable
    findings:
      - <finding>
  user_value_check:
    rating: pass | caution | fail
    findings:
      - <finding>
  overall_recommendation:
    proceed | proceed_with_changes | pause_and_reconcile | do_not_proceed
```

#### Pressure-test guidance

- **Repo reality check** asks whether the plan matches actual code.
- **Already-built collision check** asks whether a Build Unit duplicates existing models/routes/services/components.
- **Branch drift check** asks whether open/diverged branches contain relevant partial work.
- **Layer boundary check** asks whether the layer is accidentally building future-layer work.
- **Build Unit atomicity check** asks whether each Build Unit can realistically be one commit.
- **Dependency check** asks whether required earlier-layer capabilities exist.
- **Migration/destructive-change check** asks whether data changes are safe for the selected buildout mode.
- **Frontend/backend/API alignment check** asks whether the work creates a coherent vertical slice.
- **Testability check** asks whether each Build Unit has an obvious validation path.
- **Truthfulness/source-grounding check** applies when AI, generated content, user claims, compliance, privacy, or source-of-truth material is involved.
- **User value check** asks whether the layer produces meaningful product/system value now rather than only speculative architecture.

### 8.9 Build Unit inventory generation / review

LEAP can operate in two modes.

#### Mode A — User supplies Build Unit sketches

If the user supplies Build Unit sketches, LEAP should refine them, right-size them, pressure-test them, and sequence them.

#### Mode B — User supplies only layer intent

If the user supplies only the overarching system plan and target layer, LEAP should generate the Build Units itself.

Generated Build Units should be:

- detailed enough for implementation
- scoped enough to be one commit each
- sequenced by dependency
- not shortened into vague task bullets
- not overdeveloped into future-layer architecture
- tied to the solution’s actual current maturity
- checked against source-of-truth documents
- checked against current repo reality when possible

Each Build Unit should use this shape:

```yaml
build_unit_inventory:
  - id: LX.1
    title: <Build Unit title>
    purpose: <what this unit accomplishes>
    refined_scope_summary: <right-sized scope for this buildout>
    domain_boundary: <what belongs here>
    exclusions:
      - <what should not be built here>
    depends_on:
      - <prior layers or earlier Build Units>
    enables:
      - <later Build Units>
    source_of_truth_alignment:
      - <how this maps to source-of-truth docs>
    repo_reality_notes:
      - <existing code or missing code relevant to this unit>
    likely_code_areas:
      - backend
      - frontend
      - database
      - tests
      - docs
    likely_new_models:
      - <model/entity if any>
    likely_existing_models_to_reuse:
      - <existing model/entity if any>
    infrastructure_risk: none | low | medium | high
    migration_risk: none | low | medium | high
    testability: low | medium | high
    clarification_needed: true | false
```

### 8.10 Build sequence

```yaml
build_sequence:
  - order: 1
    build_unit_id: LX.1
    title: <title>
    reason_for_position: <why this comes first>
```

Default sequence should follow the generated or supplied numbering, but LEAP Recon may recommend reordering if dependencies require it.

### 8.11 Dependency review

```yaml
dependencies:
  prior_layer_dependencies:
    - <existing prior-layer capability>
  intra_layer_dependencies:
    - <LX.3 depends on LX.1 service>
  source_of_truth_dependencies:
    - <dependency named in source-of-truth docs>
  repo_confirmed_dependencies:
    - <dependency confirmed in code>
  risky_dependencies:
    - <dependency that might be missing>
  dependency_recommendations:
    - <recommendation>
```

### 8.12 Architecture right-sizing review

```yaml
architecture_right_sizing:
  default_architecture: reuse existing stack and domain patterns where reasonable
  hand_jamming_risk: low | medium | high
  speculative_architecture_risk: low | medium | high
  likely_tipping_points:
    - vector search
    - background workers
    - analytics event model
    - search index
  recommendation:
    - <minimal architecture approach>
    - <what to avoid>
```

### 8.13 Data and migration review

```yaml
data_policy:
  production_status: not_in_production | production | unknown
  destructive_changes_allowed: true | false
  migration_plans_required: true | false
  migration_files_required_if_tooling_requires: true | false
  local_reset_reporting_required: true | false
  source_of_truth_status_update_required: true | false
  likely_destructive_changes:
    - <schema/model cleanup>
  recommendation:
    - <data approach>
```

### 8.14 Infrastructure escalation review

```yaml
infrastructure_escalation:
  expected_new_services:
    - none
  possible_new_services:
    - vector database
    - queue
    - cache
    - search index
    - scheduled worker
  should_coding_agent_implement_now:
    - <yes/no and why>
  should_coding_agent_report_manual_follow_up:
    - <yes/no and what>
```

### 8.15 Layer boundary review

```yaml
layer_boundary_review:
  in_scope:
    - <work that belongs in this layer>
  out_of_scope:
    - <work that belongs in a future or prior layer>
  likely_scope_creep:
    - <tempting but inappropriate work>
  boundary_recommendations:
    - <how to keep the implementation focused>
```

### 8.16 Coding-agent question forecast

Before generating the LEAP Prompt, LEAP should forecast the kinds of intrinsic questions Codex or another coding agent may need to ask during implementation.

```yaml
coding_agent_question_forecast:
  likely_questions:
    - question: <what the coding agent may need to know>
      why_it_matters: <why this affects implementation>
      default_recommendation: <recommended default if user does not answer>
      risk_if_unanswered: low | medium | high
```

### 8.17 User clarification questions

At the end of LEAP Recon, before the LEAP Prompt is generated, ask a concise set of user questions.

Each question should include a recommended default.

End with:

```text
When you are ready, say: “Generate the LEAP Prompt.”
```

### 8.18 Prompt settings recommendation

```yaml
prompt_settings_recommendation:
  model: latest Codex / ChatGPT model
  reasoning_effort: low | medium | high | extended
  plan_required: true | false
  plan_style: none | brief upfront layer execution confirmation | per-Build Unit plan | full plan
  why: <reasoning>
```

For Rapid POC, the usual default is:

```yaml
prompt_settings_recommendation:
  model: latest Codex / ChatGPT model
  reasoning_effort: high
  plan_required: false
  plan_style: none
  why: LEAP Recon already serves as the planning layer; the coding agent should execute sequentially and report after each Build Unit.
```

---

## 9. LEAP Prompt schema

The LEAP Prompt should only be generated after LEAP Recon is complete and the user either answers questions or accepts defaults.

### 9.1 Prompt header

```yaml
framework: LEAP
framework_version: 1.2
stage: Prompt
stage_name: LEAP Prompt
solution_name: <solution/system name>
target_layer: <combined layer identifier and layer name>
branch: <branch>
buildout_mode: <mode>
model: latest Codex / ChatGPT model
reasoning_effort: <recommended effort>
plan_required: <true/false>
```

### 9.2 Required operating instructions

The final prompt should include:

- target branch
- source-of-truth document paths
- source-of-truth update rules
- no merge-to-main rule unless explicitly requested
- one Build Unit per commit rule
- exact commit message pattern
- inspect-before-each-Build Unit rule
- destructive-change policy
- architecture right-sizing policy
- infrastructure escalation/reporting policy
- layer boundary policy
- per-Build Unit validation requirements
- per-Build Unit completion report
- final layer completion report

### 9.3 Source-of-truth instructions

Every LEAP Prompt that references application-specific source-of-truth docs must include:

```yaml
source_of_truth_instructions:
  application_docs:
    - <path to app-specific status/roadmap doc>
  instructions:
    - Read these documents before implementation.
    - Treat these documents as application-specific planning authority unless repo reality contradicts them.
    - If implementation changes layer status, update the relevant application-specific source-of-truth document.
    - Do not place generic LEAP methodology changes in the application repo.
    - If generic LEAP methodology needs changes, report that as manual follow-up for the LEAP repo.
```

### 9.4 Plan mode instruction

This is required in every LEAP Prompt.

```yaml
plan_mode:
  plan_required: false
  instruction: >
    Do not create a separate implementation plan. LEAP Recon already defines the execution approach.
    Begin implementation sequentially with the first Build Unit after inspecting the repository.
```

Or:

```yaml
plan_mode:
  plan_required: true
  instruction: >
    Before implementation, provide only a brief layer-level execution confirmation.
    Do not create detailed per-Build Unit plans unless blocked by missing information.
    Then proceed sequentially.
```

### 9.5 Reasoning effort instruction

Every LEAP Prompt should include reasoning effort.

Suggested default:

```yaml
reasoning_effort:
  value: high
  rationale: >
    This is a multi-commit layer buildout with dependency tracking, source-of-truth reconciliation,
    architecture right-sizing, and repo-state inspection before each Build Unit.
```

### 9.6 Source-of-truth update policy

Every LEAP Prompt should define whether source-of-truth updates are required.

```yaml
source_of_truth_update_policy:
  update_required: true | false
  update_when:
    - layer status changes
    - build sequence changes materially
    - implementation discovers repo reality differs from planning docs
    - a Build Unit is intentionally deferred
    - a future-layer follow-up is identified
  update_scope:
    - application-specific docs only
  do_not_update:
    - generic LEAP framework docs unless this prompt is explicitly targeting the LEAP repo
```

---

## 10. LEAP Recon input template

```text
Run LEAP Recon.

Solution/system overview:
- Solution name:
- Solution type:
- High-level goal:
- Current state:
- Known constraints:

Application source-of-truth documents:
- <repo path or URL to roadmap/status/domain/architecture docs>

Target layer:
- <Layer number + layer name in one line>

Buildout settings:
- Branch name: optional; generate default if omitted
- Buildout mode: Rapid POC / Standard / Production-safe / Refactor
- Production compatibility required: yes/no/unknown
- Destructive changes allowed: yes/no/you recommend
- One Build Unit per commit: yes/no
- Coding-agent plan required during implementation: yes/no/you recommend
- Reasoning effort: low/medium/high/extended/you recommend
- Source-of-truth updates required: yes/no/you recommend

Optional existing Build Unit sketches:
[paste if available]

If Build Unit sketches are not supplied, generate the Build Units from the solution overview, source-of-truth documents, repo reality, and target layer.

Return only the LEAP Recon output first. Do not generate the LEAP Prompt yet.
At the end, ask any material clarification questions that should be answered before generating the LEAP Prompt.
Then remind me that I can say: “Generate the LEAP Prompt.”
```

---

## 11. LEAP Recon output template

```text
# LEAP Recon — <Target Layer>

## 1. Framework Interpretation

## 2. Solution Context

## 3. Source-of-Truth Review

## 4. Repo Reality Reconciliation

## 5. Layer Intent

## 6. Pressure-Test Findings

## 7. Generated / Refined Build Unit Inventory

## 8. Recommended Build Sequence

## 9. Dependency Review

## 10. Architecture Right-Sizing Review

## 11. Data / Destructive-Change Review

## 12. Infrastructure Escalation Review

## 13. Layer Boundary Review

## 14. Coding-Agent Question Forecast

## 15. Recommended Prompt Settings

## 16. Clarification Questions Before LEAP Prompt Generation

## 17. Next Step
```

---

## 12. LEAP Prompt input template

```text
Generate the LEAP Prompt for <Target Layer>.

Use the LEAP Recon findings above.
Use my answers/defaults below:
- <answer/default 1>
- <answer/default 2>

Application source-of-truth documents:
- <repo path or URL to roadmap/status/domain/architecture docs>

Create the final implementation prompt as a canvas/textdoc artifact.
Do not include extra analysis inside the prompt unless it is operationally necessary for the coding agent.
```

---

## 13. LEAP Prompt output template

```text
# <Solution Name> — LEAP Prompt — <Target Layer>

## Purpose
## Prompt Settings
## Source-of-Truth Instructions
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
## Final Layer Completion Report
```

---

## 14. Versioning

LEAP uses:

```text
LEAP vMajor.Minor
```

Current version:

```text
LEAP v1.2
```

Minor versions refine the framework without changing its core two-stage model.

Major versions change the framework structure or execution philosophy.

---

## 15. v1.2 change summary

LEAP v1.2 adds:

- explicit source-of-truth document intake
- repo reality reconciliation
- formal Recon pressure-test rubric
- layer boundary review
- source-of-truth update policy
- application-repo vs LEAP-repo boundary guidance
- stronger Build Unit alignment with repo reality
- stronger implementation prompt instructions for keeping app-specific status docs current
