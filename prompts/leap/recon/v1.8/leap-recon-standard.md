# LEAP Recon — Standard Operational Prompt — v1.8

Run LEAP Recon under LEAP v1.8.

Recon is the source-of-truth, repo-reality, drift, dependency, risk, execution-configuration, and implementation-safety pass before prompt generation. It is not the coding-agent prompt.

## Required behavior

You must:

1. verify Phase 0 / baseline readiness before planning implementation
2. identify any residual Ideation Loop questions that must be answered first
3. require or construct a source-of-truth manifest
4. classify docs as Canonical, Active, Draft, Stale, Archived, Delete Candidate, or Unknown
5. inspect repo reality before implementation planning when repo access exists
6. treat repo reality as operational truth when docs conflict, unless a human decides otherwise
7. inspect branch, PR, and worktree drift when available
8. search for already-existing functionality before recommending new work
9. detect stale assumptions, stale docs, stale prompts, and stale layer claims
10. identify cross-layer impacts and downstream assumptions
11. evaluate risk, sensitive areas, and destructive-change implications
12. define or refine Build Units only after the above checks
13. identify human checkpoints
14. distinguish LEAP process tier from agent execution configuration
15. recommend the explicit agent/tool, model, reasoning level, execution mode, validation, and commit posture when prompt generation is allowed
16. end with a gate decision

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

## Risk review

Include a risk review:

```text
- Product risk: low / medium / high
- Source-truth risk: low / medium / high
- Architecture risk: low / medium / high
- Data/security/privacy risk: low / medium / high
- AI behavior risk: low / medium / high / not applicable
- Collaboration risk: low / medium / high
- Verification risk: low / medium / high
```

Sensitive-area rule:

```text
If the change can affect money, identity, privacy, data durability, legal exposure, or user trust, stop and ask.
```

## Required Agent Execution recommendation

If the gate decision is `Generate LEAP Prompt`, include:

```text
## Recommended Agent Execution Configuration

| Field | Recommendation | Rationale |
|---|---|---|
| Agent / Tool | <Codex / Claude Code / Cursor / other> | <why> |
| Model | <exact model name or project default> | <why> |
| Reasoning Level | <low / medium / high / extended> | <why> |
| Execution Mode | <plan-first / implement-directly / implement-with-brief-plan> | <why> |
| Scope Scale | <small task / Build Unit / sublayer / entire layer / repo-wide maintenance> | <why> |
| Repository | <repo> | <why> |
| Branch / Worktree | <branch/worktree> | <why> |
| Permissions | <allowed changes> | <why> |
| Validation | <tests/lint/typecheck/build/manual checks> | <why> |
| Commit Guidance | <commit convention> | <why> |
```

Do not leave agent/tool, model, or reasoning level blank. If unknown, recommend a safe default and label it as a recommendation.

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
## 4. Ideation Loop Residual Questions
## 5. Repo Reality Reconciliation
## 6. Branch / Worktree / PR Drift Review
## 7. Documentation Lifecycle Review
## 8. Strategic Plan Reconciliation
## 9. Existing Functionality Collision Check
## 10. Stale Assumption Scan
## 11. Cross-Layer Impact Scan
## 12. Layer Boundary Review
## 13. Generated / Refined Build Unit Inventory
## 14. Recommended Build Sequence
## 15. Dependency and Destructive-Change Review
## 16. Risk Taxonomy Review
## 17. Architecture Right-Sizing Review
## 18. Human Checkpoints Required
## 19. Execution Log / Drift Ledger Expectations
## 20. Coding-Agent Risk Forecast
## 21. Recommended Agent Execution Configuration
## 22. Clarification Questions Before LEAP Prompt Generation
## 23. Gate Decision / Next Step
```

Do not generate the implementation prompt unless explicitly requested and the gate decision allows it.