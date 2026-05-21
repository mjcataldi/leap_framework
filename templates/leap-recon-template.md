# LEAP Recon Request Template

Use this template to request a LEAP Recon pass after Phase 0 is complete or when an existing project already has sufficient source-of-truth documentation.

```text
Run LEAP Recon.

Phase 0 / project baseline status:
- Phase 0 complete? yes/no/not applicable because existing project
- Project charter path:
- MVP boundary path:
- Pressure-test summary path:
- Implementation strategy path:
- Source-of-truth index path:
- Layer map path:
- Execution log path:
- Known open questions:

Solution/system overview:
- Solution name:
- Solution type:
- High-level goal:
- Current state:
- Known constraints:

Application source-of-truth documents:
- <repo path or URL to project charter / MVP boundary / roadmap / status / domain / architecture docs>

Target layer:
- <Layer number + layer name in one line>

Buildout settings:
- Branch name: optional; generate default if omitted
- Buildout mode: Rapid POC / Standard / Production-safe / Refactor
- Production compatibility required: yes/no/unknown
- Destructive changes allowed: yes/no/you recommend
- One Build Unit per commit: yes/no
- Coding-agent plan required during implementation: yes/no/you recommend
- Reasoning effort: low/medium/high/extended/you recommend
- Source-of-truth updates required: yes/no/you recommend
- Execution log update required: yes/no/you recommend
- Cross-layer impact map update required: yes/no/you recommend

Optional existing Build Unit sketches:
[paste if available]

If Build Unit sketches are not supplied, generate the Build Units from the solution overview, source-of-truth documents, repo reality, and target layer.

Required gate:
Before generating Build Units, verify whether the Phase 0 baseline and source-of-truth documents are sufficient.
If the project is too vague, stop and recommend Phase 0 Inception instead of continuing.

Return only the LEAP Recon output first. Do not generate the LEAP Prompt yet.
At the end, ask any material clarification questions that should be answered before generating the LEAP Prompt.
Then remind me that I can say: “Generate the LEAP Prompt.”
```

## Expected Recon sections

```text
# LEAP Recon — <Target Layer>

## 1. Framework Interpretation
## 2. Phase 0 / Source-of-Truth Gate Check
## 3. Solution Context
## 4. Source-of-Truth Review
## 5. Repo Reality Reconciliation
## 6. Strategic Plan Reconciliation
## 7. Cross-Layer Impact Scan
## 8. Layer Intent
## 9. Pressure-Test Findings
## 10. Generated / Refined Build Unit Inventory
## 11. Recommended Build Sequence
## 12. Dependency Review
## 13. Architecture Right-Sizing Review
## 14. Data / Destructive-Change Review
## 15. Infrastructure Escalation Review
## 16. Layer Boundary Review
## 17. Execution Log Expectations
## 18. Coding-Agent Question Forecast
## 19. Recommended Prompt Settings
## 20. Clarification Questions Before LEAP Prompt Generation
## 21. Next Step
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

## Notes

Use this when the layer needs source-of-truth review, repo reality reconciliation, pressure testing, sequencing, cross-layer impact scanning, and Build Unit generation before creating the final implementation prompt.

If source-of-truth documents conflict with repo reality, repo reality should guide implementation planning, and the conflict should be reported in Recon.
