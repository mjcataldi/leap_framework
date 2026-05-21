# LEAP Framework

**LEAP — Layer Execution & Assembly Protocol** is a solution-level framework for turning rough software intent into pressure-tested direction, layered plans, and safe, bounded, implementation-ready AI coding prompts.

LEAP v1.6 is an adversarial gate-hardening release. It keeps the three-stage lifecycle while tightening readiness gates, source-of-truth manifests, documentation lifecycle control, drift ledgers, and coding-agent handoff contracts.

## Core idea

```text
Phase 0 Inception establishes what should be built, why, and whether it should be built at all.
Source-of-truth manifests define repo-specific truth, doc status, ownership, freshness, and conflict rules.
LEAP Recon reconciles strategy, docs, branch state, stale assumptions, and repo reality before implementation planning.
LEAP Prompt gives the coding agent a bounded handoff contract with scope, non-goals, verification, and stop conditions.
```

## Three-stage workflow

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

### Phase 0: LEAP Inception

Use Phase 0 for new software projects, major new product directions, unclear app ideas, and material feature bets.

Phase 0 uses readiness gates instead of fake-precision clarity scores:

```text
C0 Blocked → C1 Discovery Ready → C2 Concept Ready → C3 Pressure-Test Ready → C4 Layer-Planning Ready → C5 Coding-Prompt Ready
```

Phase 0 must pressure test no-build and simpler alternatives before allowing layer planning.

### Stage 1: LEAP Recon

Recon checks whether the project has enough source truth and repo reality to safely generate Build Units or implementation prompts.

Recon must inspect source-of-truth manifests, documentation lifecycle status, stale assumptions, repo reality, branch/worktree/PR drift, existing functionality, cross-layer impacts, layer boundaries, and human checkpoints.

### Stage 2: LEAP Prompt

LEAP Prompt converts approved Recon into a bounded implementation handoff for Codex-style or another AI coding agent.

A valid LEAP Prompt includes objective, current repo reality, source-of-truth instructions, scope, non-goals, constraints, implementation sequence, verification, stop conditions, branch/worktree/commit instructions, source-of-truth update policy, and completion report format.

## Current version

Current framework version: **LEAP v1.6**

See [`docs/leap-v1.6.md`](docs/leap-v1.6.md).

Previous versions:

- [`docs/leap-v1.5.md`](docs/leap-v1.5.md)
- [`docs/leap-v1.4.md`](docs/leap-v1.4.md)
- [`docs/leap-v1.3.md`](docs/leap-v1.3.md)
- [`docs/leap-v1.2.md`](docs/leap-v1.2.md)
- [`docs/leap-v1.1.md`](docs/leap-v1.1.md)

## Quick start

For a new software project or major new product direction, start with [`templates/leap-phase-0-template.md`](templates/leap-phase-0-template.md).

After Phase 0 is approved, use [`templates/leap-recon-template.md`](templates/leap-recon-template.md) to request a Recon pass for the first target layer or task.

After Recon is approved, use [`templates/leap-prompt-template.md`](templates/leap-prompt-template.md) to generate the final implementation prompt.

For repeatable workflows, use the operational prompt library under [`prompts/`](prompts/).

## Source-of-truth document model

Every serious LEAP-managed application should maintain a source-of-truth manifest. The manifest identifies canonical and active docs, draft/stale/archived/delete-candidate docs, source ownership, current branch, relevant PRs, repo reality, doc-code conflicts, and the human owner/approver.

Docs should be classified as:

```text
Canonical | Active | Draft | Stale | Archived | Delete Candidate | Unknown
```

Generated docs are Draft until explicitly ratified.

## Repository structure

```text
README.md
CHANGELOG.md
docs/
  leap-v1.6.md
  leap-v1.5.md
  leap-v1.4.md
  leap-v1.3.md
  leap-v1.3-prompt-library.md
  leap-v1.2.md
  leap-v1.1.md
  glossary.md
templates/
  leap-phase-0-template.md
  leap-recon-template.md
  leap-prompt-template.md
prompts/
  README.md
  leap/
    phase-0/
      v1.6/
      v1.5/
    recon/
      v1.6/
      v1.5/
      v1.3/
    implementation/
      v1.6/
      v1.5/
      v1.3/
    governance/
      v1.6/
      v1.5/
      v1.3/
examples/
  careero-layer5-recon-outline.md
```

## Short rule

```text
No clarity, no build.
No source truth, no Recon.
No repo reality, no prompt.
No non-goals, no agent handoff.
No stop conditions, no coding task.
```
