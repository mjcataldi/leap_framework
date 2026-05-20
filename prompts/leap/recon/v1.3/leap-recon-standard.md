# LEAP Recon — Standard Operational Prompt — v1.3

Run LEAP Recon.

You are operating under LEAP v1.3.

This Recon pass must:

- inspect source-of-truth documents first
- inspect repository reality before planning
- reconcile strategy against implementation
- identify branch drift and stale assumptions
- identify cross-layer impacts
- generate or refine Build Units
- pressure-test the layer
- recommend prompt settings
- identify required documentation updates
- forecast coding-agent implementation risks

## Required LEAP v1.3 behavior

You must:

1. distinguish between strategic intent and implementation reality
2. identify stale roadmap or layer-status claims
3. identify downstream layer impacts
4. avoid rebuilding already-existing functionality
5. avoid future-layer scope creep
6. identify implementation drift when visible
7. recommend execution-log updates where appropriate
8. recommend strategic-plan updates where appropriate
9. recommend cross-layer impact-map updates where appropriate
10. keep architecture appropriately right-sized for the current maturity level

## Required outputs

Return the following sections:

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

Do not generate the implementation prompt unless explicitly requested.
