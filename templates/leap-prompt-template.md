# LEAP Prompt Request Template

Use this template after LEAP Recon has been completed and the user has answered questions or approved defaults.

```text
Generate the LEAP Prompt for <Target Layer>.

Use the LEAP Recon findings above.
Use my answers/defaults below:
- <answer/default 1>
- <answer/default 2>

Application source-of-truth documents:
- <repo path or URL to roadmap/status/domain/architecture docs>

Create the final implementation prompt as a canvas/textdoc artifact.
Do not include extra analysis inside the prompt unless it is operationally necessary for the coding agent.
```

## Expected LEAP Prompt sections

```text
# <Solution Name> — LEAP Prompt — <Target Layer>

## Purpose
## Prompt Settings
## Source-of-Truth Instructions
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
## Final Layer Completion Report
```

## Required source-of-truth behavior

Every LEAP Prompt that references application-specific source-of-truth documents should instruct the coding agent to:

- read the source-of-truth documents before implementation
- treat those documents as application-specific planning authority unless repo reality contradicts them
- update the relevant application-specific source-of-truth document when implementation changes layer status or build sequence
- avoid placing generic LEAP framework changes in the application repo
- report generic LEAP framework follow-ups separately for the LEAP repo
