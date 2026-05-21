# LEAP Recon Request Template

Use this template to request a LEAP Recon pass after Phase 0 is complete or when an existing project already has sufficient source-of-truth documentation.

```text
Run LEAP Recon under LEAP v1.6.

Phase 0 / project baseline status:
- Phase 0 complete? yes/no/not applicable because existing project
- Phase 0 mode used: Lite / Standard / Pro / Small Project Mode / unknown / not applicable
- Gate decision from Phase 0:
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
- Model tier: Standard / Thinking Extended / Pro Standard / Pro Extended / you recommend
- Production compatibility required: yes/no/unknown
- Destructive changes allowed: yes/no/you recommend
- One Build Unit per commit: yes/no
- Source-of-truth updates required: yes/no/you recommend
- Execution log / drift ledger update required: yes/no/you recommend
- Cross-layer impact map update required: yes/no/you recommend

Required gate:
- Verify whether the Phase 0 baseline and source-of-truth manifest are sufficient.
- Classify docs as Canonical, Active, Draft, Stale, Archived, Delete Candidate, or Unknown.
- Inspect repo reality before implementation planning when repo access exists.
- Search for already-existing functionality before recommending new work.
- If docs and repo reality conflict, report the conflict before generating a coding-agent prompt.
- If branch/worktree/PR drift affects ownership or merge order, require resolution before prompt generation.

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
