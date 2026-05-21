# LEAP Prompt — Standard Implementation Prompt — v1.5

Generate the LEAP Prompt.

You are operating under LEAP v1.5.

The LEAP Recon pass has already completed, and the user has approved or accepted the required defaults.

The implementation prompt must:

- preserve one Build Unit per commit where feasible
- require repository inspection before each Build Unit
- preserve layer boundaries
- preserve source-of-truth alignment
- require strategic reconciliation after implementation when reality changes
- require execution-log updates when appropriate
- require cross-layer impact review
- preserve separation between strategic docs and execution telemetry
- include explicit objective, scope, constraints, verification, and stop conditions
- prevent the coding agent from inventing missing requirements

## Required task packet

Every LEAP Prompt must include:

```text
## Task
- Objective:
- User-visible outcome:
- Source of truth:

## Scope
- In scope:
- Out of scope:
- Non-goals:
- Files/areas to inspect:
- Files/areas not to touch:

## Constraints
- Existing patterns to follow:
- Dependencies allowed/disallowed:
- Architecture constraints:
- Data/privacy/security constraints:
- AI behavior constraints, if relevant:

## Implementation Guidance
- Suggested sequence:
- Edge cases:
- Error handling:
- Accessibility/UX notes, if relevant:
- Backward compatibility:

## Verification
- Tests to run:
- Manual checks:
- Expected result:

## Stop Conditions
- Stop if docs conflict with code.
- Stop if scope requires architecture not approved.
- Stop if sensitive data handling is unclear.
- Stop if implementation requires a new dependency, migration, auth/permission change, billing change, or AI behavior change not approved.

## Output Required
- Summary of changes.
- Tests run.
- Files changed.
- Deviations from prompt.
- Docs that need updating.
```

## Required governance rules

### Strategic reconciliation

If implementation changes repo reality, layer status, architecture assumptions, or downstream expectations:

- update the affected application-specific strategic documents
- report stale assumptions
- identify downstream impact
- recommend future Recon passes where appropriate

### Execution logs

If the application repo contains or should contain execution logs and the task is not trivial:

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

### Stop conditions

The coding agent must stop and report instead of guessing when:

- docs conflict with repo reality
- implementation would violate non-goals
- unapproved architecture, dependency, migration, auth, permissions, billing, monetization, AI behavior, or sensitive-data decisions are required
- branch/worktree drift creates unclear file ownership
- verification cannot be performed or is undefined

## Required LEAP Prompt sections

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
