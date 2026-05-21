# LEAP Prompt Request Template

Use this template after LEAP Recon has been completed and the user has answered questions or approved defaults.

Do not use this template for vague app ideas. New projects must pass Phase 0 Inception and Recon before LEAP Prompt generation.

```text
Generate the LEAP Prompt for <Target Layer or Task> under LEAP v1.5.

Use the LEAP Recon findings above.
Use my answers/defaults below:
- <answer/default 1>
- <answer/default 2>

Phase 0 / baseline documents:
- Project charter:
- MVP boundary:
- Pressure-test summary:
- Implementation strategy:
- Source-of-truth index:
- Layer map:

Application source-of-truth documents:
- <repo path or URL to roadmap/status/domain/architecture docs>

Implementation target:
- Objective:
- User-visible outcome:
- In scope:
- Out of scope:
- Non-goals:
- Files/areas to inspect:
- Files/areas not to touch:

Required gate:
- Confirm Phase 0 and Recon are approved before generating the implementation prompt.
- Confirm source-of-truth review is complete.
- Confirm repo reality has been checked when repo access exists.
- Confirm scope, verification, and stop conditions are defined.
- If baseline direction, MVP boundary, source-of-truth docs, Recon approval, implementation scope, verification plan, or stop conditions are missing, stop and explain what must be completed first.

Create the final implementation prompt as a canvas/textdoc artifact.
Do not include extra analysis inside the prompt unless it is operationally necessary for the coding agent.
```

## Expected LEAP Prompt sections

```text
# <Solution Name> — LEAP Prompt — <Target Layer or Task>

## Purpose
## Prompt Settings
## Phase 0 / Source-of-Truth Gate Status
## Source-of-Truth Instructions
## Task
## Scope
## Constraints
## Implementation Guidance
## Verification
## Stop Conditions
## Strategic Reconciliation Policy
## Execution Log Policy
## Cross-Layer Impact Policy
## Branch / Worktree / Commit Instructions
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

## Required source-of-truth behavior

Every LEAP Prompt that references application-specific source-of-truth documents should instruct the coding agent to:

- read the source-of-truth documents before implementation
- treat those documents as application-specific planning authority unless repo reality contradicts them
- update the relevant application-specific source-of-truth document when implementation changes layer status or build sequence
- create or update the execution log when implementation work is performed and the work is not trivial
- update the cross-layer impact map when shared entities, workflows, or downstream assumptions change
- avoid placing generic LEAP framework changes in the application repo
- report generic LEAP framework follow-ups separately for the LEAP repo

## Required stop conditions

Every LEAP Prompt should instruct the coding agent to stop and report instead of guessing when:

- docs conflict with repo reality
- scope requires architecture not approved
- sensitive data handling is unclear
- implementation requires a new dependency, migration, auth/permission change, billing change, or AI behavior change not approved
- implementation would violate explicit non-goals
- required tests or verification paths are unavailable or unclear
- parallel-agent scopes overlap unexpectedly

## No-build gate reminder

LEAP Prompt generation is blocked when:

- Phase 0 has not been completed for a new project
- MVP boundary is missing
- explicit non-goals are missing
- source-of-truth index is missing
- the target layer has not passed Recon
- the user has not approved moving from Recon to Prompt
- implementation scope is unbounded
- stop conditions are missing
