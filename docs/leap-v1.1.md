# LEAP Framework Plan v1.1

## Framework name

**LEAP — Layer Execution & Assembly Protocol**

LEAP is a solution-level framework for turning a layered system concept into safe, sequential, implementation-ready AI coding prompts.

It can be used for software systems, product platforms, internal tools, data systems, AI applications, infrastructure buildouts, or modular engineering initiatives that benefit from layer-by-layer implementation.

LEAP takes a user’s high-level solution intent and target layer, builds out the right-sized implementation subsections for that layer, pressure-tests them, and then converts the approved plan into a comprehensive implementation prompt.

---

## 1. Core concept

```text
Layer = A major system capability or architectural phase.
Build Unit = A scoped subsection of the layer that can be implemented and committed independently.
LEAP = The framework that designs, sequences, governs, and prompt-generates the layer buildout.
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

LEAP Recon is the analysis, Build Unit design, sequencing, and clarification stage.

It produces:

1. solution and layer interpretation
2. pressure-test findings
3. generated or refined Build Unit inventory
4. recommended build sequence
5. dependency review
6. architecture right-sizing review
7. data/destructive-change review
8. infrastructure escalation review
9. coding-agent question forecast
10. clarification questions for the user
11. recommended prompt settings
12. reminder to generate the LEAP Prompt

LEAP Recon should not generate the full implementation prompt unless explicitly asked.

### Stage 2 — LEAP Prompt

LEAP Prompt is the implementation-prompt artifact stage.

It converts the approved LEAP Recon into a comprehensive prompt for Codex or another AI coding agent.

It includes:

- coding-agent context
- target branch
- buildout mode
- plan/no-plan instruction
- reasoning effort recommendation
- per-Build Unit execution contract
- branch/commit policy
- architecture escalation policy
- destructive-change policy
- full refined Build Unit implementation sequence
- per-Build Unit completion report schema
- final layer completion report schema

---

## 4. Workflow summary

```text
User provides:
- solution/system overview
- combined target layer identifier and name
- optional branch name, or branch naming preference
- buildout mode
- known constraints
- optional Build Unit sketches if already available

Assistant runs:
- LEAP Recon

Assistant returns:
- layer interpretation
- generated/refined Build Unit inventory
- build sequence
- dependency review
- architecture right-sizing review
- data/destructive-change review
- infrastructure escalation review
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

## 5. Framework hierarchy

```text
Solution Strategy
└── Layer Roadmap
    └── LEAP Package for Layer X
        ├── Stage 1: LEAP Recon
        │   ├── Solution Context
        │   ├── Layer Intent
        │   ├── Build Unit Generation / Refinement
        │   ├── Build Sequence
        │   ├── Dependency Review
        │   ├── Architecture Right-Sizing Review
        │   ├── Data / Migration Review
        │   ├── Infrastructure Escalation Review
        │   ├── Coding-Agent Question Forecast
        │   ├── User Clarification Questions
        │   └── Prompt Settings Recommendation
        │
        └── Stage 2: LEAP Prompt
            ├── Coding-Agent Context
            ├── Branch / Commit Rules
            ├── Plan Mode
            ├── Reasoning Effort
            ├── Per-Build Unit Execution Contract
            ├── Refined Build Unit Inventory
            ├── Per-Build Unit Commit Contract
            ├── Per-Build Unit Completion Report
            ├── Final Layer Completion Report
            └── Manual Follow-Up Requirements
```

---

## 6. LEAP Recon schema

### 6.1 Recon header

```yaml
framework: LEAP
framework_version: 1.1
stage: Recon
stage_name: LEAP Reconnaissance Pass
solution_name: <solution/system name>
target_layer: <combined layer identifier and layer name>
branch: <branch name or generated default>
buildout_mode: Rapid POC | Standard | Production-safe | Refactor
prompt_generation: deferred
```

### 6.2 Solution context

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

### 6.3 Layer intent

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

### 6.4 Buildout mode assessment

```yaml
buildout_mode:
  selected_mode: Rapid POC | Standard | Production-safe | Refactor
  planning_depth: LEAP Recon first; LEAP Prompt second
  sequential_execution: true
  one_build_unit_per_commit: true
  destructive_changes_allowed: true | false
  production_migration_discipline: true | false
  backward_compatibility_required: true | false
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
```

### 6.5 Branch naming policy

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
layer6_intelligent_decisions
layer4_application_workflow
layer2_intake_parsing
```

### 6.6 Build Unit inventory generation / review

LEAP can operate in two modes.

#### Mode A — User supplies Build Unit sketches

If the user supplies Build Unit sketches, LEAP should refine them, right-size them, and sequence them.

#### Mode B — User supplies only layer intent

If the user supplies only the overarching system plan and target layer, LEAP should generate the Build Units itself.

Generated Build Units should be:

- detailed enough for implementation
- scoped enough to be one commit each
- sequenced by dependency
- not shortened into vague task bullets
- not overdeveloped into future-layer architecture
- tied to the solution’s actual current maturity

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
    likely_code_areas:
      - backend
      - frontend
      - database
      - tests
    likely_new_models:
      - <model/entity if any>
    infrastructure_risk: none | low | medium | high
    clarification_needed: true | false
```

### 6.7 Build sequence

```yaml
build_sequence:
  - order: 1
    build_unit_id: LX.1
    title: <title>
    reason_for_position: <why this comes first>
```

Default sequence should follow the generated or supplied numbering, but LEAP Recon may recommend reordering if dependencies require it.

### 6.8 Dependency review

```yaml
dependencies:
  prior_layer_dependencies:
    - <existing prior-layer capability>
  intra_layer_dependencies:
    - <LX.3 depends on LX.1 service>
  risky_dependencies:
    - <dependency that might be missing>
  dependency_recommendations:
    - <recommendation>
```

### 6.9 Architecture right-sizing review

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

### 6.10 Data and migration review

```yaml
data_policy:
  production_status: not_in_production | production | unknown
  destructive_changes_allowed: true | false
  migration_plans_required: true | false
  migration_files_required_if_tooling_requires: true | false
  local_reset_reporting_required: true | false
  likely_destructive_changes:
    - <schema/model cleanup>
  recommendation:
    - <data approach>
```

### 6.11 Infrastructure escalation review

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

### 6.12 Coding-agent question forecast

Before generating the LEAP Prompt, LEAP should forecast the kinds of intrinsic questions Codex or another coding agent may need to ask during implementation.

```yaml
coding_agent_question_forecast:
  likely_questions:
    - question: <what the coding agent may need to know>
      why_it_matters: <why this affects implementation>
      default_recommendation: <recommended default if user does not answer>
      risk_if_unanswered: low | medium | high
```

### 6.13 User clarification questions

At the end of LEAP Recon, before the LEAP Prompt is generated, ask a concise set of user questions.

Each question should include a recommended default.

End with:

```text
When you are ready, say: “Generate the LEAP Prompt.”
```

### 6.14 Prompt settings recommendation

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

## 7. LEAP Prompt schema

The LEAP Prompt should only be generated after LEAP Recon is complete and the user either answers questions or accepts defaults.

### 7.1 Prompt header

```yaml
framework: LEAP
framework_version: 1.1
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

### 7.2 Required operating instructions

The final prompt should include:

- target branch
- no merge-to-main rule unless explicitly requested
- one Build Unit per commit rule
- exact commit message pattern
- inspect-before-each-Build Unit rule
- destructive-change policy
- architecture right-sizing policy
- infrastructure escalation/reporting policy
- per-Build Unit validation requirements
- per-Build Unit completion report
- final layer completion report

### 7.3 Plan mode instruction

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

### 7.4 Reasoning effort instruction

Every LEAP Prompt should include reasoning effort.

Suggested default:

```yaml
reasoning_effort:
  value: high
  rationale: >
    This is a multi-commit layer buildout with dependency tracking, architecture right-sizing,
    and repo-state inspection before each Build Unit.
```

---

## 8. LEAP Recon input template

```text
Run LEAP Recon.

Solution/system overview:
- Solution name:
- Solution type:
- High-level goal:
- Current state:
- Known constraints:

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

Optional existing Build Unit sketches:
[paste if available]

If Build Unit sketches are not supplied, generate the Build Units from the solution overview and target layer.

Return only the LEAP Recon output first. Do not generate the LEAP Prompt yet.
At the end, ask any material clarification questions that should be answered before generating the LEAP Prompt.
Then remind me that I can say: “Generate the LEAP Prompt.”
```

---

## 9. LEAP Recon output template

```text
# LEAP Recon — <Target Layer>

## 1. Framework Interpretation

## 2. Solution Context

## 3. Layer Intent

## 4. Pressure-Test Findings

## 5. Generated / Refined Build Unit Inventory

## 6. Recommended Build Sequence

## 7. Dependency Review

## 8. Architecture Right-Sizing Review

## 9. Data / Destructive-Change Review

## 10. Infrastructure Escalation Review

## 11. Coding-Agent Question Forecast

## 12. Recommended Prompt Settings

## 13. Clarification Questions Before LEAP Prompt Generation

## 14. Next Step
```

---

## 10. LEAP Prompt input template

```text
Generate the LEAP Prompt for <Target Layer>.

Use the LEAP Recon findings above.
Use my answers/defaults below:
- <answer/default 1>
- <answer/default 2>

Create the final implementation prompt as a canvas/textdoc artifact.
Do not include extra analysis inside the prompt unless it is operationally necessary for the coding agent.
```

---

## 11. LEAP Prompt output template

```text
# <Solution Name> — LEAP Prompt — <Target Layer>

## Purpose
## Prompt Settings
## Branch / Commit Instructions
## Plan Mode
## Destructive Change Policy
## Architecture Right-Sizing Policy
## Infrastructure Escalation Policy
## General Engineering Requirements
## Governance / Safety Requirements
## Per-Build Unit Execution Contract
## Per-Build Unit Completion Report
## Refined Build Unit Implementation Sequence
## Final Layer Completion Report
```

---

## 12. Versioning

LEAP uses:

```text
LEAP vMajor.Minor
```

Current version:

```text
LEAP v1.1
```

Minor versions refine the framework without changing its core two-stage model.

Major versions change the framework structure or execution philosophy.
