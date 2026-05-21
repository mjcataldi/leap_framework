# LEAP Governance Prompt — Strategic Reconciliation Pass — v1.6

Run a LEAP v1.6 strategic reconciliation pass.

This is not implementation work. It exists to make the project safe for future Recon and coding-agent prompts.

## Required analysis

You must inspect and reconcile:

1. source-of-truth manifest
2. canonical, active, draft, stale, archived, and delete-candidate docs
3. repo reality on the current base branch
4. relevant target branches, PRs, worktrees, and recent commits if available
5. strategic plans, layer plans, execution logs, and cross-layer impact maps
6. already-built but undocumented functionality
7. planned-but-missing functionality
8. stale roadmap claims and stale future prompts
9. architecture, naming, state-machine, schema, API, and generated-type drift
10. branch/merge-order conflicts
11. human decisions needed before implementation

## Required output

```text
# LEAP Strategic Reconciliation Pass — v1.6

## 1. Repo Reality Summary
## 2. Source-of-Truth Manifest Review
## 3. Documentation Lifecycle Review
## 4. Strategic Plan Alignment Review
## 5. Branch / Worktree / PR Drift Findings
## 6. Cross-Layer Impact Findings
## 7. Stale Assumptions and Stale Prompts
## 8. Duplicate / Divergent Architecture Findings
## 9. Drift Ledger Entries
## 10. Recommended Documentation Updates
## 11. Recommended Future Recon Passes
## 12. Human Decisions Needed
## 13. Technical Debt / Cleanup Recommendations
## 14. Gate Decision
## 15. Strategic Conclusion
```

Gate decisions:

```text
Safe for Recon
Reconcile Docs First
Resolve Branch Drift First
Needs Human Decision
Do Not Generate Prompt Yet
```

Do not generate implementation prompts unless explicitly requested and this pass concludes that prompt generation is safe.
