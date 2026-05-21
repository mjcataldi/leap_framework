# LEAP Recon — Standard Operational Prompt — v1.5

Run LEAP Recon.

You are operating under LEAP v1.5.

This Recon pass must:

- verify Phase 0 and source-of-truth readiness before planning implementation
- inspect source-of-truth documents first
- classify source-of-truth docs as canonical, supporting, archived, or unknown
- inspect repository reality before planning
- reconcile strategy against implementation
- identify branch/worktree drift and stale assumptions
- identify cross-layer impacts
- generate or refine Build Units
- pressure-test the layer or task
- recommend model-effort and prompt settings
- identify required documentation updates
- identify human checkpoints
- forecast coding-agent implementation risks
- end with a gate decision

## Required LEAP v1.5 behavior

You must:

1. distinguish between strategic intent and implementation reality
2. distinguish Known, Assumed, Unknown, Contested, and Needs Decision items
3. identify stale roadmap or layer-status claims
4. identify downstream layer impacts
5. avoid rebuilding already-existing functionality
6. avoid future-layer scope creep
7. identify implementation drift when visible
8. recommend execution-log updates where appropriate
9. recommend strategic-plan updates where appropriate
10. recommend cross-layer impact-map updates where appropriate
11. keep architecture appropriately right-sized for the current maturity level
12. stop before prompt generation when scope, source of truth, repo reality, or human approval is insufficient

## Required outputs

Return the following sections:

```text
# LEAP Recon — <Target Layer or Task>

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

## Gate decisions

Use one of these decisions:

```text
Generate LEAP Prompt
Continue Phase 0
Pressure Test Further
Narrow Scope First
Needs Human Decision
Reconcile Docs First
Do Not Build Yet
```

Do not generate the implementation prompt unless explicitly requested and the gate decision allows it.
