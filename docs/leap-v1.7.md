# LEAP Framework Plan v1.7

## Framework name

**LEAP — Layer Execution & Assembly Protocol**

LEAP is a solution-level framework for turning rough software intent into pressure-tested direction, layered plans, and safe, bounded, implementation-ready AI coding prompts.

LEAP v1.7 is a Codex execution-configuration hardening release. It preserves the v1.6 lifecycle:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

v1.7 keeps the adversarial readiness gates, source-of-truth manifests, drift controls, and agent-handoff contracts from v1.6, then closes a practical handoff gap: every Codex-ready prompt must now state the exact model and reasoning level to use.

A prompt that tells the agent what to build but not what execution profile to use is not fully runnable.

---

## 1. Core hard rules

```text
No clarity, no build.
No source-of-truth manifest, no Recon.
No repo-reality inspection, no implementation prompt for existing repos.
No MVP boundary, no layer plan.
No concrete non-goals, no coding-agent prompt.
No stop conditions, no agent handoff.
No explicit model and reasoning level, no Codex-ready handoff.
No parallel-agent ownership map, no parallel-agent launch.
Repo reality outranks planning language unless a human explicitly decides otherwise.
Generated docs are Draft until marked Active or Canonical.
Use the lightest LEAP mode that controls the actual risk.
Use the lightest Codex reasoning level that controls the implementation risk.
```

LEAP may help clarify vague ideas. LEAP may not convert vague ideas directly into implementation plans, layer plans, or coding-agent prompts.

A coding agent must receive a bounded task packet, not a broad wish.

A Codex-ready LEAP Prompt must also receive an execution configuration, not a vibes-based launch instruction.

---

## 2. Intake classifier

Every LEAP run starts by classifying the request.

| Request Type | Default LEAP Path | Escalate When |
|---|---|---|
| Small task | Small Project Mode → bounded prompt | Scope is unclear, shared contracts change, tests are missing, or repo/docs conflict |
| New product idea | Phase 0 Inception | User/problem/workflow/MVP/non-goals are vague |
| Major new feature | Phase 0 Lite/Standard → Recon | User-facing workflow, data model, AI behavior, auth, billing, or privacy changes |
| Existing repo layer | Source-of-Truth Manifest → Recon | Stale docs, open PRs, branch drift, partial implementation, or unclear layer boundary |
| Strategic pivot | Partial Phase 0 rerun → Drift Ledger → Recon | User, MVP, architecture, monetization, risk, or layer sequence changes |
| Parallel-agent work | Parallel-Agent Preflight → per-agent Recon/Prompt | Shared files, schemas, APIs, generated types, migrations, auth, or state machines are involved |

Default rule:

```text
Ask the fewest questions needed to make the next safe gate decision.
```

---

## 3. Readiness gates, not fake precision

LEAP uses readiness gates for user-facing decisions.

| Gate | Meaning | Allowed Output |
|---|---|---|
| C0: Blocked | Idea or task is too vague for safe progress | Discovery questions only |
| C1: Discovery Ready | Enough context exists to explore the problem | Phase 0 discovery note |
| C2: Concept Ready | User, problem, and current workflow are understandable | Concept draft and assumption ledger |
| C3: Pressure-Test Ready | Concept is specific enough to challenge | Alternatives/no-build/MVP pressure test |
| C4: Layer-Planning Ready | MVP boundary, non-goals, risks, and approval are clear | Layer plan or Recon request |
| C5: Coding-Prompt Ready | Source truth, repo reality, scope, tests, stop conditions, and execution config are clear | Bounded coding-agent prompt |

Hard blocker rule:

```text
A high readiness impression does not override a hard blocker.
```

Hard blockers include missing target user, missing problem, missing current workflow, missing MVP boundary, missing concrete non-goals, unexamined sensitive-data risk, unresolved source-of-truth conflict, unknown repo reality for existing repos, unapproved architecture decision, missing tests/verification path, missing human approval, missing model, or missing reasoning level.

---

## 4. Phase 0 Inception protocol

Phase 0 is the product/startup clarity gate. It is not implementation planning.

Required Phase 0 flow:

```text
0.1 Raw idea intake
0.2 Problem and user discovery
0.3 Current workflow / workaround discovery
0.4 Pain intensity and success-event discovery
0.5 No-build and simpler-alternative review
0.6 MVP boundary definition
0.7 Concrete non-goal definition
0.8 Evidence labeling and assumption ledger
0.9 Gate decision
```

Phase 0 must separate:

```text
Known = directly provided, observed, measured, implemented, or confirmed.
Assumed = plausible but not confirmed.
Unknown = missing information.
Contested = conflicts with docs, repo, user statements, or prior decisions.
Needs Decision = a human decision is required before safe progress.
Deprecated = previously true or previously planned but no longer active.
```

Phase 0 may recommend a downstream LEAP process tier, but it should not assign a final Codex execution configuration until Recon has inspected source truth and repo reality.

---

## 5. No-build protocol

Every new product idea and material feature must pass a no-build review before layer planning.

Required questions:

```text
What happens if we do nothing?
What manual workflow solves 80% of this?
What spreadsheet, checklist, template, or lightweight doc solves 80%?
What existing product solves 80%?
What integration, script, no-code automation, or service solves 80%?
What behavior/process change solves 80%?
Why is custom software still justified?
Why is AI specifically justified, if AI is proposed?
What would make this not worth building?
```

LEAP must not treat “the user wants an app” as evidence that an app should be built.

---

## 6. MVP boundary protocol

An MVP is not “the whole platform, but basic.”

A valid MVP must define:

```text
- one primary user
- one primary workflow
- one primary success event
- one smallest useful outcome
- must-have features
- manual-for-now items
- explicit non-goals
- later roadmap candidates
- validation criteria
- overbuild risks
```

If the MVP includes multiple primary users, multiple workflows, marketplace dynamics, deep integrations, dashboards, automation, and admin tooling, LEAP must flag it as a full product in disguise.

---

## 7. Source-of-truth protocol

No Recon, layer plan, or coding prompt may proceed without an active source-of-truth manifest.

### 7.1 Source-of-truth hierarchy

When sources conflict, use this hierarchy unless a human explicitly decides otherwise:

```text
1. Running implementation / repo reality
2. Current target branch diff
3. Merged code on base branch
4. Database schema and migrations
5. Tests and fixtures
6. Canonical docs
7. Active ADRs / decision records
8. Current layer plan
9. Recent PR descriptions and execution logs
10. Old plans / archived docs
```

Old plans are not source truth unless explicitly reactivated.

### 7.2 Source-of-truth manifest

Every serious LEAP run should create, update, or require this structure:

```text
# Source-of-Truth Manifest

- Project:
- Date:
- Target branch:
- Base branch:
- Current layer / task:
- Canonical strategic docs:
- Canonical architecture docs:
- Active ADRs / decision records:
- Active layer plan:
- Execution log path:
- Cross-layer impact map path:
- Stale / archived docs:
- Do-not-use docs:
- Open branches / PRs affecting this work:
- Repo reality summary:
- Known doc-code conflicts:
- Human owner / approver:
- Last reviewed:
```

### 7.3 Required prompt source block

Every coding prompt must include:

```text
Use these sources:
- <canonical / active sources>

Do not use these sources:
- <draft / stale / archived / superseded sources>

Current repo reality:
- <summary>

Known conflicts:
- <conflicts and decisions>
```

AI agents cannot be trusted to infer canonical status from filenames.

---

## 8. Documentation lifecycle protocol

All durable docs must have a lifecycle status.

| Status | Meaning | Agent Behavior |
|---|---|---|
| Canonical | Authoritative for a named truth | May use as governing source |
| Active | Current and useful but limited scope | May use within stated scope |
| Draft | Generated or incomplete, not ratified | Do not treat as authority |
| Stale | Likely outdated or contradicted | Use only as historical context |
| Archived | Superseded | Do not use for planning |
| Delete Candidate | Harmful, duplicate, or misleading | Recommend removal |

Minimum doc metadata:

```text
Status:
Scope:
Owner:
Created:
Last reviewed:
Supersedes:
Superseded by:
Related branch/layer:
Use for:
Do not use for:
```

Rules:

1. A new durable doc must update the source-of-truth manifest.
2. A superseded doc must be marked stale or archived.
3. A coding prompt may not cite Draft docs as governing authority.
4. Old roadmaps must not remain active by accident.
5. If docs conflict, LEAP must surface the conflict instead of choosing silently.
6. If a doc has no status, owner, or date, treat it as suspect.

Unclassified docs are a liability.

---

## 9. Drift-control protocol

LEAP tracks five drift types.

| Drift Type | Detection | Required Control |
|---|---|---|
| Strategy drift | User, MVP, monetization, risks, or product direction changed | Strategy change record and partial Phase 0 rerun |
| Documentation drift | Docs disagree with each other or with code | Doc lifecycle update and manifest correction |
| Implementation drift | Code does not match plan | Drift report: accept, revert, refactor, or update docs |
| Branch drift | Branches/PRs/worktrees diverge on shared surfaces | Branch map, merge order, ownership map |
| Prompt drift | Prompt assumes stale files, stale branch state, old decisions, missing model, or missing reasoning level | Prompt freshness check and regenerated handoff |

Drift ledger entry:

```text
# Drift Ledger Entry

- Date:
- Drift type:
- Source A:
- Source B:
- Conflict:
- Risk:
- Decision:
- Owner:
- Required update:
```

Recon must report mismatches before proposing new work.

---

## 10. Recon protocol

Recon starts only when Phase 0 is complete or when an existing project has enough source truth to proceed.

Recon must inspect:

```text
- target branch and base branch
- open PRs and relevant branches
- recent commits if available
- source-of-truth manifest
- canonical and active docs
- stale/archived docs that may mislead agents
- existing implementation for the target capability
- routes, APIs, schemas, migrations, generated types
- tests, fixtures, scripts, package/dependency changes
- existing UI text/components/hooks/services/utilities
- cross-layer impact map
- execution logs and prior Build Unit records
```

Recon must search for existing functionality before recommending new implementation.

Recon must recommend a Codex execution configuration when the gate decision is `Generate LEAP Prompt` or when the user asks for a whole-layer/sublayer implementation prompt.

Recon gate decisions:

```text
Generate LEAP Prompt
Continue Phase 0
Pressure Test Further
Narrow Scope First
Needs Human Decision
Reconcile Docs First
Resolve Branch Drift First
Do Not Build Yet
```

---

## 11. Agent-handoff protocol

A LEAP Prompt is a handoff contract. It must be boring, narrow, and hard to misinterpret.

Required handoff structure:

```text
# <Solution Name> — LEAP Prompt — <Target Layer or Task>

## 1. Codex Execution Configuration
## 2. Objective
## 3. Current repo reality
## 4. Canonical and active sources
## 5. Sources not to use
## 6. Scope
## 7. Non-goals
## 8. Files/components likely involved
## 9. Files/components not to touch
## 10. Data model / API / auth / state constraints
## 11. UX and accessibility constraints
## 12. Dependencies and branch assumptions
## 13. Implementation sequence
## 14. Acceptance criteria
## 15. Required tests and manual checks
## 16. Stop conditions
## 17. Completion summary format
```

Prompt rules:

```text
Do not say “infer the rest.”
Do not ask the agent to broadly clean up architecture.
Do not combine discovery, architecture design, and implementation in one prompt.
Do not omit non-goals.
Do not omit files not to touch.
Do not omit tests.
Do not omit stop conditions.
Do not omit model.
Do not omit reasoning level.
```

Stop conditions must include:

```text
- required source files are missing
- existing implementation contradicts the prompt
- docs conflict with repo reality
- tests reveal unrelated failures
- schema/API/auth/migration changes are needed but not authorized
- task requires touching forbidden files
- unmerged branch appears to own the same surface
- implementation would violate non-goals
- acceptance criteria are impossible as written
- requested model is unavailable and no approved fallback is provided
- requested reasoning level is unavailable and no approved fallback is provided
```

---

## 12. Codex execution-configuration protocol

LEAP v1.7 distinguishes between two related but different decisions:

```text
LEAP process tier = how much LEAP analysis is needed before prompt generation.
Codex execution configuration = how the implementation agent should be run after prompt generation.
```

A model tier such as Standard, Thinking Extended, Pro Standard, or Pro Extended is not enough by itself. The final Codex-ready prompt must specify the concrete execution profile.

### 12.1 Required configuration block

Every Codex-ready LEAP Prompt must include this block near the top:

```text
## 1. Codex Execution Configuration

| Field | Value |
|---|---|
| Model | <exact model name or approved project default> |
| Reasoning Level | <low / medium / high / extended / project-approved enum> |
| Execution Mode | <recon-only / plan-first / implement-directly / implement-with-brief-plan> |
| Scope Scale | <small task / Build Unit / sublayer / entire layer / repo-wide maintenance> |
| Repository | <owner/repo or local repo name> |
| Branch / Worktree | <target branch/worktree> |
| Permissions | <allowed modifications> |
| Validation | <tests/lint/typecheck/build/manual checks> |
| Commit Guidance | <commit message convention or none> |
```

If the project uses model names with minor versions, the model field must include the minor version.

If the model or reasoning level is not known, LEAP must recommend one explicitly and mark it as a recommendation, not leave the field blank.

### 12.2 Reasoning-level selection rules

Use the smallest reasoning level that controls the actual risk.

| Reasoning Level | Use For | Avoid For |
|---|---|---|
| Low | Tiny localized edits, typo fixes, obvious one-file changes | Anything with ambiguity or shared contracts |
| Medium | Small bounded implementation, clear UI fixes, simple tests, isolated refactors | Schema/API/auth/migration/state changes |
| High | Build Units, sublayers, multi-file features, state workflows, cross-component UX, meaningful test updates | Strategic pivots, branch drift, high-risk AI/security/privacy work |
| Extended | Full-layer implementation, architecture-sensitive work, repo-wide refactors, parallel-agent sequencing, stale-doc reconciliation, destructive schema/data-model changes, sensitive AI behavior | Routine cleanup |

If the requested task is a whole layer, default to High or Extended unless Recon proves the layer is narrow and low-risk.

If the prompt is intended for direct Codex insertion, the model and reasoning level must be visible before the task instructions.

### 12.3 Recommended defaults

These are defaults, not universal rules:

```text
Small cleanup prompt:
- Model: project-approved Codex model
- Reasoning Level: Medium
- Execution Mode: implement-directly

Build Unit / sublayer prompt:
- Model: project-approved Codex model
- Reasoning Level: High
- Execution Mode: implement-with-brief-plan

Whole-layer prompt:
- Model: project-approved Codex model
- Reasoning Level: Extended
- Execution Mode: plan-first, then implement

Recon-only prompt:
- Model: project-approved reasoning model
- Reasoning Level: High or Extended depending on ambiguity
- Execution Mode: recon-only
```

### 12.4 Prompt-readiness blocker

```text
A LEAP Prompt is not Codex-ready unless it tells the user exactly which model and reasoning level to use.
```

---

## 13. Parallel-agent protocol

Parallel work is allowed only when ownership boundaries are explicit.

Parallel-agent preflight:

```text
# Parallel-Agent Preflight

- Agent count:
- Base branch:
- Worktree/branch per agent:
- Owner/task per agent:
- Files each agent may touch:
- Files each agent must not touch:
- Shared schemas/types/APIs:
- Migration ownership:
- Generated file ownership:
- Test ownership:
- Merge order:
- Integration checkpoint:
- Conflict zones:
- Model per agent:
- Reasoning level per agent:
```

Hard rules:

1. No two agents may own the same migration sequence.
2. No two agents may independently change a shared state machine.
3. No two agents may independently change the same API contract.
4. Shared types require one owner.
5. Generated files require coordination.
6. Each agent must know what other agents are changing.
7. Merge order must be declared before work begins.
8. Integration happens after every merge, not after all merges.
9. Each agent must have its own explicit model and reasoning level.

Collision zones:

```text
Database schema
Migrations
Auth/session code
Shared types
Route definitions
API clients
State machines
Generated artifacts
Package/dependency files
Test setup
Configuration files
Design-system components
```

---

## 14. Model-selection protocol

Use the smallest LEAP process tier that controls the risk.

| LEAP Tier | Use For | Do Not Use For |
|---|---|---|
| Standard | Small edits, bug fixes, one-file prompts, low ambiguity | Vague ideas, branch drift, architecture or data changes |
| Thinking Extended | Phase 0 discovery, MVP boundaries, non-goals, moderate Recon, bounded prompt drafting | Conflicting docs, parallel agents, major architecture drift |
| Pro Standard | Existing repo with partial implementation, multiple docs, cross-layer review, significant refactor planning | Strategic pivots with branch drift or sensitive workflows |
| Pro Extended | Deep adversarial audits, strategy pivots, stale docs, multiple branches/worktrees, high-risk AI handoffs, privacy/security-sensitive workflows | Routine work |

Escalate LEAP process depth when the task involves vague product intent, stale or conflicting docs, partial implementation, multiple branches, schema/API/auth changes, sensitive data, AI behavior, monetization, or broad blast radius.

Then translate the selected LEAP process tier into a concrete Codex execution configuration before generating the final implementation prompt.

---

## 15. Small Project Mode

LEAP should not become process for process’s sake.

Use Small Project Mode when:

```text
- task is small
- scope is obvious
- one branch
- one agent
- no stale docs
- no architecture change
- no schema/API/auth change
- no product-strategy ambiguity
```

Required fields:

```text
# Small LEAP Brief

- Goal:
- Current state:
- Scope:
- Non-goals:
- Files likely touched:
- Acceptance criteria:
- Tests/checks:
- Stop conditions:
- Model:
- Reasoning level:
```

Escalate out of Small Project Mode when the user cannot define the task, shared contracts change, implementation differs from docs, multiple branches are active, non-goals are missing, no obvious verification path exists, or the correct execution configuration is unclear.

If LEAP is slower than the work itself and the risk is low, LEAP is failing.

---

## 16. v1.7 operational outputs

### Phase 0 output

```text
# LEAP Phase 0 Inception — <Project>

## 1. Mode and Intake Classification
## 2. Original User Wording
## 3. Current Understanding
## 4. Evidence Labels
## 5. Socratic Discovery Questions, if needed
## 6. Readiness Gate
## 7. No-Build / Alternative-Solution Review
## 8. MVP Boundary
## 9. Concrete Non-Goals
## 10. Risks and Constraints
## 11. Assumption Ledger
## 12. Documentation Bootstrap Recommendation
## 13. Source-of-Truth Manifest Recommendation
## 14. Human Checkpoints Required
## 15. Downstream Model / Reasoning Considerations
## 16. Gate Decision / Next Step
```

### Recon output

```text
# LEAP Recon — <Target Layer or Task>

## 1. Framework Interpretation
## 2. Source-of-Truth Manifest Check
## 3. Phase 0 / Baseline Gate Check
## 4. Repo Reality Reconciliation
## 5. Branch / Worktree / PR Drift Review
## 6. Documentation Lifecycle Review
## 7. Strategic Plan Reconciliation
## 8. Existing Functionality Collision Check
## 9. Stale Assumption Scan
## 10. Cross-Layer Impact Scan
## 11. Layer Boundary Review
## 12. Build Unit Inventory
## 13. Recommended Build Sequence
## 14. Dependency and Destructive-Change Review
## 15. Human Checkpoints Required
## 16. Coding-Agent Risk Forecast
## 17. Recommended Codex Execution Configuration
## 18. Gate Decision / Next Step
```

### Prompt output

```text
# <Solution> — LEAP Prompt — <Target Layer or Task>

## 1. Codex Execution Configuration
## 2. Objective
## 3. Current Repo Reality
## 4. Source-of-Truth Instructions
## 5. Scope
## 6. Non-Goals
## 7. Constraints
## 8. Implementation Sequence
## 9. Verification
## 10. Stop Conditions
## 11. Branch / Worktree / Commit Instructions
## 12. Source-of-Truth Update Policy
## 13. Completion Report Format
```

---

## 17. Versioning

Current version:

```text
LEAP v1.7
```

LEAP v1.7 is a minor hardening release. It preserves the LEAP identity, lifecycle, readiness gates, source-of-truth controls, drift governance, and agent-safety posture from v1.6 while adding mandatory Codex execution-configuration requirements.

---

## 18. v1.7 change summary

LEAP v1.7 adds:

- mandatory model and reasoning-level fields for Codex-ready prompts
- a Codex Execution Configuration block in final implementation prompts
- clear separation between LEAP process tier and Codex execution configuration
- reasoning-level selection rules for small tasks, Build Units, sublayers, whole layers, and repo-wide work
- prompt-readiness blockers when model or reasoning level is missing
- parallel-agent model/reasoning ownership fields
- updated Recon and Prompt outputs that recommend and carry forward execution settings

The short rule:

```text
No model, no handoff.
No reasoning level, no Codex-ready prompt.
No source truth, no Recon.
No repo reality, no implementation plan.
No stop conditions, no coding task.
```
