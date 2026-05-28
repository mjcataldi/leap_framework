# LEAP Framework Plan v1.9

## Framework name

**LEAP — Layered Execution & Alignment Protocol**

LEAP is a software delivery framework for turning rough software intent into pressure-tested direction, source-grounded plans, and safe, bounded, implementation-ready AI coding-agent handoffs.

LEAP is software-delivery-first. It uses AI-agent governance as part of the delivery system, and many of its underlying ideas can later generalize into broader decision and execution workflows.

LEAP v1.9 is a repository canonicalization and prompt flattening release. It preserves the v1.8 lifecycle:

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

v1.9 keeps readiness gates, source-of-truth manifests, drift controls, agent-handoff contracts, the public front door, tool-agnostic agent language, risk examples, and the explicit **Ideation Loop** from v1.8. It changes the repository shape so the current framework document has one canonical path and current operational prompts live at the top of `prompts/`.

---

## 1. Core hard rules

```text
No clarity, no build.
No source-of-truth manifest, no Recon.
No repo-reality inspection, no implementation prompt for existing repos.
No MVP boundary, no layer plan.
No concrete non-goals, no coding-agent prompt.
No stop conditions, no agent handoff.
No explicit execution profile, no agent-ready handoff.
No parallel-agent ownership map, no parallel-agent launch.
Repo reality outranks planning language unless a human explicitly decides otherwise.
Generated docs are Draft until marked Active or Canonical.
Use the lightest LEAP mode that controls the actual risk.
Use the lightest agent reasoning level that controls the implementation risk.
Ask until the idea becomes buildable, then stop asking and build only the bounded task.
```

LEAP may help clarify vague ideas. LEAP may not convert vague ideas directly into implementation plans, layer plans, or coding-agent prompts.

A coding agent must receive a bounded task packet, not a broad wish.

---

## 2. What LEAP is for

LEAP helps avoid asking an AI coding agent to build from confusion.

Use LEAP when:

```text
- the idea is vague
- the repo already has code
- docs may be stale
- the task spans multiple files
- data models, APIs, auth, billing, AI behavior, privacy, security, or user trust are involved
- multiple people or agents may touch the same system
- the agent must know when to stop instead of guessing
```

Do not use full LEAP when:

```text
- the task is tiny
- the scope is obvious
- one file is affected
- no shared contract changes
- no strategic ambiguity
- no sensitive data, auth, billing, migration, AI behavior, or architecture risk
```

Use Small Project Mode for low-risk work.

---

## 3. Ideation Loop

Humans often begin with an emotional or intuitive picture of the solution. That picture may feel complete, but the gaps are often filled by assumptions, optimism, preference, frustration, or urgency rather than mechanisms.

LEAP treats ideation as a clarification loop:

```text
Intent → Questions → Evidence labels → Assumption ledger → Pressure test → Revised intent → Gate decision
```

The loop continues while hard blockers remain.

### 3.1 What the Ideation Loop does

The Ideation Loop turns:

```text
"I think I want an app that does X"
```

into:

```text
- who the user is
- what problem they have
- what they do today
- what the smallest useful outcome is
- what the system must not do
- what can be manual for now
- what is known, assumed, unknown, contested, or needs a decision
- what would make the idea not worth building
- what source truth exists
- what must be checked in the repo before coding
```

The loop is not meant to slow delivery. It prevents fast delivery of the wrong thing.

### 3.2 Question-loop rule

```text
Ask the fewest questions needed to make the next safe gate decision.
If the next gate decision is still unsafe, ask another small question round.
Do not ask a giant question dump when a focused round will clarify the next blocker.
Do not proceed to implementation planning while hard blockers remain.
```

Questions are the source of answers. LEAP uses questions to expose the difference between what a user imagines and what a system must mechanically do.

### 3.3 Minimum clarity threshold

LEAP v1.9 keeps readiness gates as the user-facing mechanism. Numeric clarity estimates may be used as private thinking aids, but they must not override hard blockers.

A useful planning heuristic:

```text
Phase 0 is required when the project cannot answer core product questions with roughly 80% confidence.
Recon begins when product direction is clear enough, but repo reality still needs to be inspected.
Implementation prompts begin only after scope, non-goals, verification, stop conditions, and execution profile are clear.
```

Core product questions:

```text
Who is this for?
What problem does it solve?
What is the current workaround?
What is the smallest useful outcome?
What is explicitly out of scope?
What risks or sensitive areas exist?
What would make this not worth building?
```

---

## 4. Intake classifier

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

## 5. Readiness gates, not fake precision

LEAP uses readiness gates for user-facing decisions.

| Gate | Meaning | Allowed Output |
|---|---|---|
| C0: Blocked | Idea or task is too vague for safe progress | Discovery questions only |
| C1: Discovery Ready | Enough context exists to explore the problem | Phase 0 discovery note |
| C2: Concept Ready | User, problem, and current workflow are understandable | Concept draft and assumption ledger |
| C3: Pressure-Test Ready | Concept is specific enough to challenge | Alternatives/no-build/MVP pressure test |
| C4: Layer-Planning Ready | MVP boundary, non-goals, risks, and approval are clear | Layer plan or Recon request |
| C5: Coding-Prompt Ready | Source truth, repo reality, scope, tests, stop conditions, and execution profile are clear | Bounded coding-agent prompt |

Hard blocker rule:

```text
A high readiness impression does not override a hard blocker.
```

Hard blockers include missing target user, missing problem, missing current workflow, missing MVP boundary, missing concrete non-goals, unexamined sensitive-data risk, unresolved source-of-truth conflict, unknown repo reality for existing repos, unapproved architecture decision, missing tests/verification path, missing human approval, missing agent/tool, missing model, or missing reasoning level.

---

## 6. Phase 0 Inception protocol

Phase 0 is the product/startup clarity gate. It is not implementation planning.

Required Phase 0 flow:

```text
0.1 Raw idea intake
0.2 Problem and user discovery
0.3 Current workflow / workaround discovery
0.4 Pain intensity and success-event discovery
0.5 Ideation Loop question round
0.6 No-build and simpler-alternative review
0.7 MVP boundary definition
0.8 Concrete non-goal definition
0.9 Evidence labeling and assumption ledger
0.10 Gate decision
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

Phase 0 may recommend a downstream LEAP process tier, but it should not assign a final agent execution configuration until Recon has inspected source truth and repo reality.

---

## 7. No-build protocol

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

## 8. MVP boundary protocol

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

## 9. Source-of-truth protocol

No Recon, layer plan, or coding prompt may proceed without an active source-of-truth manifest or an explicitly scoped minimum viable source-truth list.

Minimum viable source truth:

```text
1. Strategic plan or project charter
2. Source-of-truth manifest or explicit source list
3. Current layer/task description
4. Repo reality summary when repo exists
5. Explicit stale/do-not-use docs list
6. LEAP framework version being used
```

For a small solo project, this can be compressed into one doc. For AI-heavy teams, separate the documents.

### 9.1 Source-of-truth hierarchy

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

---

## 10. Recon confidence guidance

Recon coverage is directional, not mathematical. Hard blockers still override confidence estimates.

| Work Type | Suggested Confidence Before Prompt |
|---|---:|
| New product / Layer 0 baseline | 90–95% |
| Whole layer | 80–90% |
| Sublayer | 75–85% |
| Single Build Unit / LEAP LHS | 60–75%, default around 67% |
| Tiny local fix | 50–60%, if no shared contracts are touched |

Use the lightest LEAP mode that controls the actual risk.

---

## 11. Build Unit sizing rule

A Build Unit is too large when it requires the agent to modify multiple unrelated capabilities, make unapproved architecture decisions, touch shared contracts without ownership clarity, or compress durable design into “good enough for now” implementation.

Split a layer before that happens.

Red flags:

```text
- one prompt touches schema, API, UI, auth, tests, docs, and workflow state
- the agent has to decide product behavior
- implementation sequence has more than 5–7 meaningful steps
- test plan becomes vague
- non-goals start sounding like “try not to”
```

---

## 12. Agent execution profile

LEAP is tool-agnostic. Codex is one possible implementation agent, not the framework boundary.

An agent execution profile should include:

```text
Agent / Tool:
Model:
Reasoning level:
Context size:
Repo browsing ability:
Shell access:
Autonomous edit behavior:
Preferred handoff style:
Known strengths:
Known failure modes:
Required stop conditions:
Validation commands:
Commit behavior:
```

Different agents need different constraints. Weak repo awareness requires stronger file lists and inspect-first steps. Strong autonomous editing requires tighter non-goals and forbidden-file lists. Long-context agents may accept more source material, but still need source hierarchy and conflict rules.

---

## 13. Risk taxonomy

LEAP risk categories:

| Risk Area | Example | Control |
|---|---|---|
| Product risk | Building the wrong workflow | Phase 0 / no-build review |
| Source-truth risk | Agent follows stale docs | Manifest + doc lifecycle |
| Architecture risk | Feature forced into bad structure | Recon + architecture right-sizing |
| Data risk | Destructive migration or data loss | Human approval + rollback plan |
| Security risk | Auth/session/permission changes | Mandatory checkpoint |
| Privacy risk | Sensitive user data exposed | Sensitive-area approval |
| AI behavior risk | Fabricated claims or unsafe automation | AI behavior constraints |
| UX risk | Flow becomes confusing or inaccessible | Acceptance criteria + manual checks |
| Collaboration risk | Agents touch same files/contracts | Ownership map + merge order |

Sensitive-area rule:

```text
If the change can affect money, identity, privacy, data durability, legal exposure, or user trust, stop and ask.
```

---

## 14. Destructive-change protocol

A destructive change is anything that can break, delete, rewrite, or invalidate existing state in a way that is not trivially reversible.

Examples:

```text
- dropping database columns or tables
- replacing a data model
- deleting existing records
- changing IDs or ownership relationships
- rewriting migrations
- changing auth/session behavior
- changing infrastructure that affects availability
- removing user-visible workflows
```

Default public rule:

```text
Destructive changes are not allowed unless explicitly authorized.
```

A LEAP Prompt should state:

```text
Destructive changes: allowed / not allowed / allowed only in these areas.
Rollback required: yes/no.
Data preservation required: yes/no.
Human approval required before migration: yes/no.
```

---

## 15. Agent failure modes

LEAP should guard against:

```text
- hallucinating files, APIs, or business rules
- obeying stale docs over current code
- broad refactors disguised as cleanup
- silent schema or contract changes
- adding dependencies without approval
- passing tests by weakening them
- overfitting to prompt wording instead of repo reality
- completing the task while violating non-goals
- making product decisions inside implementation
```

---

## 16. Operational outputs

### Phase 0 output

```text
# LEAP Phase 0 Inception — <Project>

## 1. Mode and Intake Classification
## 2. Original User Wording
## 3. Current Understanding
## 4. Ideation Loop Status
## 5. Evidence Labels
## 6. Socratic Discovery Questions, if needed
## 7. Readiness Gate
## 8. No-Build / Alternative-Solution Review
## 9. MVP Boundary
## 10. Concrete Non-Goals
## 11. Risks and Constraints
## 12. Assumption Ledger
## 13. Documentation Bootstrap Recommendation
## 14. Source-of-Truth Manifest Recommendation
## 15. Human Checkpoints Required
## 16. Downstream Agent / Model / Reasoning Considerations
## 17. Gate Decision / Next Step
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
## 12. Generated / Refined Build Unit Inventory
## 13. Recommended Build Sequence
## 14. Dependency and Destructive-Change Review
## 15. Architecture Right-Sizing Review
## 16. Human Checkpoints Required
## 17. Execution Log / Drift Ledger Expectations
## 18. Coding-Agent Risk Forecast
## 19. Recommended Agent Execution Configuration
## 20. Clarification Questions Before LEAP Prompt Generation
## 21. Gate Decision / Next Step
```

### Prompt output

```text
# <Solution> — LEAP Prompt — <Target Layer or Task>

## 1. Agent Execution Configuration
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
LEAP v1.9
```

LEAP v1.9 is a repository canonicalization and prompt flattening release. It preserves the LEAP identity, lifecycle, readiness gates, source-of-truth controls, drift governance, agent-safety posture, public entry path, tool-agnostic agent language, question-loop mechanics, risk examples, and contribution scaffolding from v1.8 while moving the current framework and prompt library to canonical paths.

---

## 18. v1.9 change summary

LEAP v1.9 adds:

- canonical current framework document path: `docs/leap.md`
- flattened current operational prompts under `prompts/`
- detailed release history in `docs/release-history.md`
- current version marker in `VERSION.md`
- removal of old versioned framework docs from the active repo
- removal of nested historical prompt directories from the active repo
- preservation of historical version visibility through `CHANGELOG.md`, Git history, and the `leap-v1.8` tag

The short rule:

```text
No clarity, no build.
No source truth, no Recon.
No repo reality, no implementation plan.
No stop conditions, no coding task.
No execution profile, no agent-ready prompt.
Ask until the idea becomes buildable, then stop asking and build only the bounded task.
```
