# LEAP Phase 0 — Standard Operational Prompt — v1.7

Run LEAP Phase 0 Inception under LEAP v1.7.

This is a discovery, pressure-test, and gate-decision pass. It is not an implementation prompt.

## Required behavior

You must:

1. preserve the user's original idea wording
2. classify the request: small task, new idea, major feature, existing repo layer, strategic pivot, or parallel-agent workflow
3. choose or recommend Phase 0 mode: Lite, Standard, Pro, or Small Project Mode
4. ask only the questions needed to make the next safe gate decision
5. separate Known, Assumed, Unknown, Contested, Needs Decision, and Deprecated items
6. identify target user, problem, current workflow, pain, success event, MVP boundary, non-goals, risks, and constraints
7. pressure test whether software is needed at all
8. consider simpler alternatives: do nothing, manual workflow, spreadsheet, checklist, template, process change, service, integration, script, or no-code automation
9. use readiness gates C0–C5 instead of fake-precision clarity scores
10. block implementation planning when hard blockers remain
11. identify downstream model/reasoning considerations only as planning signals
12. end with a gate decision

## Readiness gates

```text
C0: Blocked — discovery questions only
C1: Discovery Ready — Phase 0 discovery note allowed
C2: Concept Ready — concept draft and assumption ledger allowed
C3: Pressure-Test Ready — no-build and MVP pressure test allowed
C4: Layer-Planning Ready — Recon/layer planning allowed after approval
C5: Coding-Prompt Ready — only after Recon, source truth, repo reality, scope, tests, stop conditions, model, and reasoning level are clear
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
## 4. Evidence Labels
### Known
### Assumed
### Unknown
### Contested
### Needs Decision
### Deprecated
## 5. Socratic Discovery Questions, if needed
## 6. Readiness Gate
## 7. No-Build / Alternative-Solution Review
## 8. MVP Boundary Draft
## 9. Concrete Non-Goals
## 10. Risks and Constraints
## 11. Assumption Ledger
## 12. Starter Documentation Bootstrap Recommendation
## 13. Source-of-Truth Manifest Recommendation
## 14. Human Checkpoints Required
## 15. Downstream Model / Reasoning Considerations
## 16. Gate Decision / Next Step
```

## Downstream model / reasoning considerations

Phase 0 may flag likely implementation posture, but it must not finalize Codex execution settings before Recon has reviewed source truth and repo reality.

Use this section to note:

```text
- likely LEAP process tier
- likely scope scale
- likely ambiguity level
- likely architecture / data / AI / privacy / security risk
- whether downstream work may require high or extended reasoning
```

Do not generate Recon, Build Units, architecture, implementation strategy, layer plans, or coding-agent prompts unless the gate decision allows it and the user explicitly approves moving forward.
