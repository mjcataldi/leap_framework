# LEAP Governance Prompt — Strategic Reconciliation Pass — v1.5

Run a strategic reconciliation pass.

You are operating under LEAP v1.5.

The purpose of this pass is not to build new functionality.

The purpose is to reconcile:

- repository reality
- strategic plans
- source-of-truth ownership
- layer-status documents
- execution logs
- cross-layer dependency assumptions
- branch/worktree drift
- stale implementation claims
- stale future prompts
- conflicting docs

## Required analysis

You must:

1. inspect the current main branch
2. inspect relevant active or diverged branches/worktrees if available
3. inspect source-of-truth index and canonical docs
4. inspect strategic plans and layer-status documents
5. inspect execution logs if present
6. inspect cross-layer impact maps if present
7. identify stale roadmap claims
8. identify already-built but undocumented functionality
9. identify planned-but-missing functionality
10. identify downstream layer impacts
11. identify architectural drift
12. identify duplicate abstractions or inconsistent naming
13. identify stale Build Units or stale future prompts
14. identify docs with missing owner, freshness, or canonical/supporting/archived status
15. recommend documentation corrections
16. recommend future Recon passes if required
17. identify human decisions needed before further implementation

## Required output sections

```text
# LEAP Strategic Reconciliation Pass

## 1. Repo Reality Summary
## 2. Source-of-Truth Ownership Review
## 3. Strategic Plan Alignment Review
## 4. Branch / Worktree Drift Findings
## 5. Cross-Layer Impact Findings
## 6. Stale Assumptions
## 7. Duplicate / Divergent Architecture Findings
## 8. Recommended Documentation Updates
## 9. Recommended Future Recon Passes
## 10. Human Decisions Needed
## 11. Technical Debt / Cleanup Recommendations
## 12. Strategic Conclusion
```

Do not generate implementation prompts unless explicitly requested and the reconciliation pass concludes that prompt generation is safe.
