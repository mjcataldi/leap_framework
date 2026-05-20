# LEAP Recon Request Template

Use this template to request a LEAP Recon pass.

```text
Run LEAP Recon.

Solution/system overview:
- Solution name:
- Solution type:
- High-level goal:
- Current state:
- Known constraints:

Application source-of-truth documents:
- <repo path or URL to roadmap/status/domain/architecture docs>

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

Optional existing Build Unit sketches:
[paste if available]

If Build Unit sketches are not supplied, generate the Build Units from the solution overview, source-of-truth documents, repo reality, and target layer.

Return only the LEAP Recon output first. Do not generate the LEAP Prompt yet.
At the end, ask any material clarification questions that should be answered before generating the LEAP Prompt.
Then remind me that I can say: “Generate the LEAP Prompt.”
```

## Expected Recon sections

```text
# LEAP Recon — <Target Layer>

## 1. Framework Interpretation
## 2. Solution Context
## 3. Source-of-Truth Review
## 4. Repo Reality Reconciliation
## 5. Layer Intent
## 6. Pressure-Test Findings
## 7. Generated / Refined Build Unit Inventory
## 8. Recommended Build Sequence
## 9. Dependency Review
## 10. Architecture Right-Sizing Review
## 11. Data / Destructive-Change Review
## 12. Infrastructure Escalation Review
## 13. Layer Boundary Review
## 14. Coding-Agent Question Forecast
## 15. Recommended Prompt Settings
## 16. Clarification Questions Before LEAP Prompt Generation
## 17. Next Step
```

## Notes

Use this when the layer needs source-of-truth review, repo reality reconciliation, pressure testing, sequencing, and Build Unit generation before creating the final implementation prompt.

If source-of-truth documents conflict with repo reality, repo reality should guide implementation planning, and the conflict should be reported in Recon.
