# LEAP Recon — Standard Operational Prompt — v1.6

Run LEAP Recon under LEAP v1.6.

Recon is the source-of-truth, repo-reality, drift, dependency, and implementation-safety pass before prompt generation. It is not the coding-agent prompt.

## Required behavior

You must:

1. verify Phase 0 / baseline readiness before planning implementation
2. require or construct a source-of-truth manifest
3. classify docs as Canonical, Active, Draft, Stale, Archived, Delete Candidate, or Unknown
4. inspect repo reality before implementation planning when repo access exists
5. treat repo reality as operational truth when docs conflict, unless a human decides otherwise
6. inspect branch, PR, and worktree drift when available
7. search for already-existing functionality before recommending new work
8. detect stale assumptions, stale docs, stale prompts, and stale layer claims
9. identify cross-layer impacts and downstream assumptions
10. define or refine Build Units only after the above checks
11. identify human checkpoints
12. recommend the smallest sufficient model tier
13. end with a gate decision

## Required source-of-truth manifest check

```text
# Source-of-Truth Manifest Check

- Project:
- Date:
- Target branch:
- Base branch:
- Current layer / task:
- Canonical strategic docs:
- Canonical architecture docs:
- Active ADRs / decision records:
- Active layer plan:
- Execution log path:
- Cross-layer impact map path:
- Stale / archived docs:
- Do-not-use docs:
- Open branches / PRs affecting this work:
- Repo reality summary:
- Known doc-code conflicts:
- Human owner / approver:
- Last reviewed:
```

## Required repo-reality inspection

Inspect, when available:

```text
- target branch and base branch
- open PRs and relevant branches
- recent commits
- routes and API surfaces
- database schema and migrations
- generated types and shared contracts
- existing UI components, hooks, utilities, services, and text
- tests, fixtures, scripts, package/dependency files
- auth/session/permission logic
- docs/execution logs/cross-layer impact map
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
Resolve Branch Drift First
Do Not Build Yet
```

## Required output

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
## 19. Recommended Model Tier
## 20. Clarification Questions Before LEAP Prompt Generation
## 21. Gate Decision / Next Step
```

Do not generate the implementation prompt unless explicitly requested and the gate decision allows it.
