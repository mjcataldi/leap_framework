# LEAP Phase 0 — Standard Operational Prompt

Run LEAP Phase 0 Inception using the current LEAP framework.

This is a discovery, ideation, pressure-test, and gate-decision pass. It is not an implementation prompt.

## Required behavior

You must:

1. preserve the user's original idea wording
2. classify the request: small task, new idea, major feature, existing repo layer, strategic pivot, or parallel-agent workflow
3. choose or recommend Phase 0 mode: Lite, Standard, Pro, or Small Project Mode
4. use the Ideation Loop to clarify vague intent before implementation planning
5. ask only the questions needed to make the next safe gate decision
6. ask another small question round if hard blockers remain
7. separate Known, Assumed, Unknown, Contested, Needs Decision, and Deprecated items
8. identify target user, problem, current workflow, pain, success event, MVP boundary, non-goals, risks, and constraints
9. pressure test whether software is needed at all
10. consider simpler alternatives: do nothing, manual workflow, spreadsheet, checklist, template, process change, service, integration, script, or no-code automation
11. use readiness gates C0–C5 instead of fake-precision clarity scores
12. block implementation planning when hard blockers remain
13. identify downstream agent/model/reasoning considerations only as planning signals
14. end with a gate decision

## Ideation Loop

Use this loop while intent remains vague:

```text
Intent → Questions → Evidence labels → Assumption ledger → Pressure test → Revised intent → Gate decision
```

Question-loop rule:

```text
Ask the fewest questions needed to make the next safe gate decision.
If the next gate decision is still unsafe, ask another small question round.
Do not ask a giant question dump when a focused round will clarify the next blocker.
Do not proceed to implementation planning while hard blockers remain.
```

## Readiness gates

```text
C0: Blocked — discovery questions only
C1: Discovery Ready — Phase 0 discovery note allowed
C2: Concept Ready — concept draft and assumption ledger allowed
C3: Pressure-Test Ready — no-build and MVP pressure test allowed
C4: Layer-Planning Ready — Recon/layer planning allowed after approval
C5: Coding-Prompt Ready — only after Recon, source truth, repo reality, scope, tests, stop conditions, and execution profile are clear
```

## Hard blockers

Implementation planning is blocked if any of these are missing or unresolved:

```text
- primary user
- concrete problem
- current workflow or workaround
- MVP boundary
- concrete non-goals
- sensitive data / risk profile when applicable
- source-of-truth manifest for existing projects
- repo reality for existing repos
- verification path
- human approval to proceed
```

## Gate decisions

Use one of these decisions:

```text
Continue Discovery
Draft Concept Brief
Pressure Test Further
Narrow MVP First
Proceed to Recon
Do Not Build Yet
```

## Required output

```text
# LEAP Phase 0 Inception — <Project Name or Working Title>

## 1. Mode and Intake Classification
## 2. Original User Wording
## 3. Current Understanding
## 4. Ideation Loop Status
## 5. Evidence Labels
### Known
### Assumed
### Unknown
### Contested
### Needs Decision
### Deprecated
## 6. Socratic Discovery Questions, if needed
## 7. Readiness Gate
## 8. No-Build / Alternative-Solution Review
## 9. MVP Boundary Draft
## 10. Concrete Non-Goals
## 11. Risks and Constraints
## 12. Assumption Ledger
## 13. Starter Documentation Bootstrap Recommendation
## 14. Source-of-Truth Manifest Recommendation
## 15. Human Checkpoints Required
## 16. Downstream Agent / Model / Reasoning Considerations
## 17. Gate Decision / Next Step
```

Do not generate Recon, Build Units, architecture, implementation strategy, layer plans, or coding-agent prompts unless the gate decision allows it and the user explicitly approves moving forward.
