# LEAP Prompt — Standard Implementation Prompt — v1.3

Generate the LEAP Prompt.

You are operating under LEAP v1.3.

The LEAP Recon pass has already completed.

The implementation prompt must:

- preserve one Build Unit per commit where feasible
- require repository inspection before each Build Unit
- preserve layer boundaries
- preserve source-of-truth alignment
- require strategic reconciliation after implementation
- require execution-log updates
- require cross-layer impact review
- preserve separation between strategic docs and execution telemetry

## Required governance rules

### Strategic reconciliation

If implementation changes repo reality, layer status, architecture assumptions, or downstream expectations:

- update the affected application-specific strategic documents
- report stale assumptions
- identify downstream impact
- recommend future Recon passes where appropriate

### Execution logs

If the application repo contains or should contain execution logs:

- create or update the appropriate execution log
- record implementation discoveries
- record technical debt
- record follow-on work
- record cross-layer impacts

### Cross-layer impact review

If shared entities, workflows, APIs, contracts, orchestration systems, analytics, or lifecycle systems are modified:

- inspect the cross-layer impact map if available
- identify impacted layers
- report stale downstream assumptions
- recommend required follow-up reconciliation

## Required LEAP Prompt sections

```text
# <Solution Name> — LEAP Prompt — <Target Layer>

## Purpose
## Prompt Settings
## Source-of-Truth Instructions
## Strategic Reconciliation Policy
## Execution Log Policy
## Cross-Layer Impact Policy
## Branch / Commit Instructions
## Plan Mode
## Destructive Change Policy
## Architecture Right-Sizing Policy
## Infrastructure Escalation Policy
## Layer Boundary Policy
## General Engineering Requirements
## Governance / Safety Requirements
## Per-Build Unit Execution Contract
## Per-Build Unit Completion Report
## Refined Build Unit Implementation Sequence
## Source-of-Truth Update Policy
## Post-Implementation Reconciliation Checklist
## Final Layer Completion Report
```
