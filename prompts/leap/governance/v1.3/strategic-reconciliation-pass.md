# LEAP Governance Prompt — Strategic Reconciliation Pass — v1.3

Run a strategic reconciliation pass.

You are operating under LEAP v1.3.

The purpose of this pass is not to build new functionality.

The purpose is to reconcile:

- repository reality
- strategic plans
- layer-status documents
- execution logs
- cross-layer dependency assumptions
- branch drift
- stale implementation claims

## Required analysis

You must:

1. inspect the current main branch
2. inspect relevant active or diverged branches if available
3. inspect strategic plans and layer-status documents
4. inspect execution logs if present
5. inspect cross-layer impact maps if present
6. identify stale roadmap claims
7. identify already-built but undocumented functionality
8. identify planned-but-missing functionality
9. identify downstream layer impacts
10. identify architectural drift
11. identify duplicate abstractions or inconsistent naming
12. identify stale Build Units or stale future prompts
13. recommend documentation corrections
14. recommend future Recon passes if required

## Required output sections

```text
# LEAP Strategic Reconciliation Pass

## 1. Repo Reality Summary
## 2. Strategic Plan Alignment Review
## 3. Branch Drift Findings
## 4. Cross-Layer Impact Findings
## 5. Stale Assumptions
## 6. Duplicate / Divergent Architecture Findings
## 7. Recommended Documentation Updates
## 8. Recommended Future Recon Passes
## 9. Technical Debt / Cleanup Recommendations
## 10. Strategic Conclusion
```

Do not generate implementation prompts unless explicitly requested.
