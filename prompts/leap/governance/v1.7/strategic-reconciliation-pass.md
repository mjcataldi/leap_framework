# LEAP Governance Prompt — Strategic Reconciliation Pass — v1.7

Run a LEAP v1.7 strategic reconciliation pass.

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
11. stale or missing model/reasoning guidance in future prompts
12. human decisions needed before implementation

## Required output

```text
# LEAP Strategic Reconciliation Pass — v1.7

## 1. Repo Reality Summary
## 2. Source-of-Truth Manifest Review
## 3. Documentation Lifecycle Review
## 4. Strategic Plan Alignment Review
## 5. Branch / Worktree / PR Drift Findings
## 6. Cross-Layer Impact Findings
## 7. Stale Assumptions and Stale Prompts
## 8. Duplicate / Divergent Architecture Findings
## 9. Model / Reasoning Guidance Findings
## 10. Drift Ledger Entries
## 11. Recommended Documentation Updates
## 12. Recommended Future Recon Passes
## 13. Human Decisions Needed
## 14. Technical Debt / Cleanup Recommendations
## 15. Gate Decision
## 16. Strategic Conclusion
```

## Model / reasoning guidance findings

Report whether any current or future implementation prompts are missing:

```text
- exact model
- reasoning level
- execution mode
- scope scale
- validation expectations
- commit guidance
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
