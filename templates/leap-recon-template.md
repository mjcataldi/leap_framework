# LEAP Recon Request Template

Use this template to request a LEAP Recon pass after Phase 0 is complete or when an existing project already has sufficient source-of-truth documentation.

```text
Run LEAP Recon under LEAP v1.9.

Phase 0 / project baseline status:
- Phase 0 complete? yes/no/not applicable because existing project
- Phase 0 mode used: Lite / Standard / Pro / Small Project Mode / unknown / not applicable
- Gate decision from Phase 0:
- Ideation Loop status: complete / still unclear / not applicable
- Human approvals already granted:
- Known open questions:

Source-of-truth manifest:
- Manifest path or pasted manifest:
- Project charter path:
- MVP boundary path:
- Pressure-test summary path:
- Implementation strategy path:
- Layer map path:
- Execution log path:
- Cross-layer impact map path:
- Stale / archived / do-not-use docs:

Solution/system overview:
- Solution name:
- Solution type:
- High-level goal:
- Current state:
- Known constraints:

Target layer or target task:
- <Layer number + layer name, or bounded task name>

Repo / branch context:
- Repository:
- Base branch:
- Target branch/worktree, if known:
- Open PRs or active branches to inspect, if known:
- Areas likely affected:
- Areas not to touch:

Buildout settings:
- Buildout mode: Rapid POC / Standard / Production-safe / Refactor
- LEAP process tier: Standard / Thinking Extended / Pro Standard / Pro Extended / you recommend
- Agent / Tool: Codex / Claude Code / Cursor / other / you recommend
- Model: <exact model name or you recommend>
- Reasoning level: Low / Medium / High / Extended / you recommend
- Execution mode: recon-only / plan-first / implement-directly / implement-with-brief-plan / you recommend
- Production compatibility required: yes/no/unknown
- Destructive changes allowed: yes/no/you recommend
- One Build Unit per commit: yes/no
- Source-of-truth updates required: yes/no/you recommend
- Execution log / drift ledger update required: yes/no/you recommend
- Cross-layer impact map update required: yes/no/you recommend

Required gate:
- Verify whether the Phase 0 baseline and source-of-truth manifest are sufficient.
- Confirm whether more Ideation Loop questions are needed before planning implementation.
- Classify docs as Canonical, Active, Draft, Stale, Archived, Delete Candidate, or Unknown.
- Inspect repo reality before implementation planning when repo access exists.
- Search for already-existing functionality before recommending new work.
- Recommend an explicit Agent Execution Configuration before LEAP Prompt generation.
- If docs and repo reality conflict, report the conflict before generating a coding-agent prompt.
- If branch/worktree/PR drift affects ownership or merge order, require resolution before prompt generation.
- If agent/tool, model, or reasoning level is missing, recommend safe defaults based on scope, ambiguity, and implementation risk.

Return only the LEAP Recon output first. Do not generate the LEAP Prompt yet.
At the end, ask any material clarification questions that should be answered before generating the LEAP Prompt.
Then remind me that I can say: “Generate the LEAP Prompt.”
```

## Expected Recon sections

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

## Recommended Agent Execution Configuration section

```text
## 21. Recommended Agent Execution Configuration

| Field | Recommendation | Rationale |
|---|---|---|
| Agent / Tool | <Codex / Claude Code / Cursor / other> | <why> |
| Model | <exact model name or project default> | <why> |
| Reasoning Level | <low / medium / high / extended> | <why> |
| Execution Mode | <plan-first / implement-directly / implement-with-brief-plan> | <why> |
| Scope Scale | <small task / Build Unit / sublayer / entire layer / repo-wide maintenance> | <why> |
| Validation | <tests/lint/typecheck/build/manual checks> | <why> |
```

## Recon confidence guidance

Use confidence as a heuristic, not as a blocker override:

```text
New product / Layer 0 baseline: 90–95%
Whole layer: 80–90%
Sublayer: 75–85%
Single Build Unit / LEAP LHS: 60–75%, default around 67%
Tiny local fix: 50–60%, if no shared contracts are touched
```

Hard blockers override confidence impressions.
