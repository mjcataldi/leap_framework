# LEAP Charter Request Template

Use this template when starting a new solution or reconciling an existing project before LEAP Recon, LEAP Prompt, implementation, or Validation/Handoff.

LEAP Charter establishes or reconciles project direction, source-of-truth docs, roadmap, and implementation posture. It replaces the active use of the older "Phase 0" label.

```text
Run LEAP Charter using the current LEAP framework.

Charter mode:
- Greenfield / Brownfield / you recommend

Initial request:
- <Describe the app, tool, product, workflow, automation, feature, gap, or existing project. Rough is okay.>

Known context:
- Solution name:
- Target users, if known:
- Current workflow or workaround, if known:
- Existing repo? yes/no/link if available:
- Existing docs, if known:
- Known stale or conflicting docs:
- Business/personal motivation:
- Technical preferences or constraints:
- Timeline or urgency:
- Sensitive data, compliance, AI-behavior, monetization, or risk concerns:

Charter settings:
- Use the Ideation Loop to clarify vague intent before implementation planning.
- Ask the fewest questions needed to make the next safe gate decision.
- Separate Known, Assumed, Unknown, Contested, Needs Decision, and Deprecated items.
- Use readiness gates C0-C5 instead of numeric clarity scores.
- Pressure test whether this should be custom software at all.
- If Brownfield, inspect and classify existing docs before treating them as source truth.
- If Brownfield, apply this policy:
  Canonicalize forward. Archive backward. Preserve traceability. Never let stale docs compete with source-of-truth docs.
- Do not generate runtime implementation changes unless I explicitly ask.
- Capture runtime work as follow-up LEAP Recon, LEAP Prompt, or LEAP LHS recommendations.
- Use LHS only when staged repo/docs work is warranted by implementation gravity. Charter does not use LHS by default.

Required Charter workflow:
1. Intake classification.
2. Raw request preservation.
3. Greenfield/Brownfield mode decision.
4. Ideation Loop question pass.
5. Evidence labeling and assumption ledger.
6. No-build / alternative-solution review where relevant.
7. Product direction and MVP/scope boundary.
8. Concrete non-goals.
9. Documentation baseline recommendation.
10. Source-of-truth recommendation.
11. Gap register.
12. Brownfield migration map if existing docs are reconciled.
13. Prompt backlog recommendation.
14. Recommended next LEAP Recon, LEAP Prompt, or LEAP LHS.
15. Gate decision.

Return the LEAP Charter output only.
If more information is needed, ask the next discovery round instead of producing implementation plans.
```

## Expected Charter sections

```text
# LEAP Charter - <Project Name or Working Title>

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
## 6. Discovery Questions, if needed
## 7. Readiness Gate
## 8. Greenfield or Brownfield Findings
## 9. No-Build / Alternative-Solution Review
## 10. MVP Boundary or Current Scope Boundary
## 11. Concrete Non-Goals
## 12. Risks and Constraints
## 13. Documentation Baseline Recommendation
## 14. Source-of-Truth Recommendation
## 15. Gap Register
## 16. Migration Map, if Brownfield
## 17. Prompt Backlog Recommendations
## 18. Human Checkpoints Required
## 19. Recommended Next LEAP Recon / LEAP Prompt / LEAP LHS
## 20. Gate Decision / Next Step
```

## LEAP LHS note

LEAP LHS is a structured LEAP Prompt format for layered implementation work using the House Standard. It is useful when work is layered, staged, or large enough to require House Standard-style execution. Not every LEAP Prompt is an LHS prompt.

Greenfield Charter should usually avoid LHS during early product shaping, naming, ideation, MVP definition, or strategic discovery. Brownfield Charter may use or recommend LHS only after the reconciliation plan is clear and the repo-changing documentation work needs staged execution, commit boundaries, tests/docs checks, or source-truth validation.
