# LEAP Recon Request Template

Use this template to request a LEAP Recon pass after Phase 0 is complete or when an existing project already has sufficient source-of-truth documentation.

```text
Run LEAP Recon under LEAP v1.5.

Phase 0 / project baseline status:
- Phase 0 complete? yes/no/not applicable because existing project
- Phase 0 mode used: Lite / Standard / Pro / unknown / not applicable
- Gate decision from Phase 0:
- Project charter path:
- MVP boundary path:
- Pressure-test summary path:
- Implementation strategy path:
- Source-of-truth index path:
- Layer map path:
- Execution log path:
- Known open questions:
- Human approvals already granted:

Solution/system overview:
- Solution name:
- Solution type:
- High-level goal:
- Current state:
- Known constraints:

Application source-of-truth documents:
- <repo path or URL to project charter / MVP boundary / roadmap / status / domain / architecture docs>

Source-of-truth expectations:
- Identify canonical, supporting, archived, and unknown-status docs.
- Identify document owners and last meaningful update if available.
- Identify stale or conflicting assumptions before planning implementation.

Target layer or target task:
- <Layer number + layer name, or bounded task name>

Repo / branch context:
- Repository:
- Base branch:
- Target branch/worktree, if known:
- Recent changes or active branches to inspect, if known:
- Areas likely affected:
- Areas not to touch:

Buildout settings:
- Branch name: optional; generate default if omitted
- Buildout mode: Rapid POC / Standard / Production-safe / Refactor
- Model-effort tier: Standard / Pro Standard / Pro Extended / you recommend
- Production compatibility required: yes/no/unknown
- Destructive changes allowed: yes/no/you recommend
- One Build Unit per commit: yes/no
- Coding-agent plan required during implementation: yes/no/you recommend
- Source-of-truth updates required: yes/no/you recommend
- Execution log update required: yes/no/you recommend
- Cross-layer impact map update required: yes/no/you recommend

Optional existing Build Unit sketches:
[paste if available]

If Build Unit sketches are not supplied, generate the Build Units from the solution overview, source-of-truth documents, repo reality, and target layer.

Required gate:
Before generating Build Units, verify whether the Phase 0 baseline and source-of-truth documents are sufficient.
If the project is too vague, stop and recommend Phase 0 Inception instead of continuing.
If docs and repo reality conflict, stop or flag the conflict before generating a coding-agent prompt.

Return only the LEAP Recon output first. Do not generate the LEAP Prompt yet.
At the end, ask any material clarification questions that should be answered before generating the LEAP Prompt.
Then remind me that I can say: “Generate the LEAP Prompt.”
```

## Expected Recon sections

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

## Gate behavior

Recon should stop and recommend Phase 0 if any of these are missing for a new project:

- target user
- problem statement
- MVP boundary
- explicit non-goals
- risk profile for sensitive data
- source-of-truth index
- human approval to begin layer planning

Recon should stop or require a human decision if implementation would require guessing about:

- architecture
- auth or permissions
- billing, monetization, ranking, or incentives
- sensitive data
- destructive migrations
- external integrations
- AI behavior that affects user trust or user-facing claims
- source-of-truth conflicts
- overlapping parallel-agent scopes

## Notes

Use this when the layer needs source-of-truth review, repo reality reconciliation, pressure testing, sequencing, cross-layer impact scanning, and Build Unit generation before creating the final implementation prompt.

If source-of-truth documents conflict with repo reality, repo reality should guide implementation planning, and the conflict should be reported in Recon.
