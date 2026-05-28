# LEAP Framework

**LEAP — Layered Execution & Alignment Protocol** is a software delivery framework for turning rough intent into pressure-tested direction, source-grounded plans, and safe, bounded, implementation-ready AI coding-agent handoffs.

LEAP started as a practical response to AI-assisted software delivery: coding agents can move quickly, but speed is only useful when the idea is clear, the source truth is current, the repo reality is understood, and the implementation task is bounded.

The active repository presents the current canonical LEAP framework document and current operational prompts without versioned filenames. Historical versions are preserved through Git tags, Git history, `CHANGELOG.md`, and `docs/release-history.md`.

## Core idea

```text
People often begin with a feeling for what they want built.
LEAP turns that feeling into a testable delivery path.

Phase 0 Inception clarifies what should be built, who it serves, why it matters, and whether it should be built at all.
The Ideation Loop keeps asking targeted questions until the solution is clear enough to reason about mechanically.
Source-of-truth manifests define repo-specific truth, doc status, ownership, freshness, and conflict rules.
LEAP Recon reconciles strategy, docs, branch state, stale assumptions, and repo reality before implementation planning.
LEAP Prompt gives the coding agent a bounded handoff contract with scope, non-goals, verification, stop conditions, branch/worktree/commit instructions, source-of-truth update policy, completion report format, and explicit agent execution settings.
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

Phase 0 also includes the **Ideation Loop**: repeated, targeted question cycles that expose gaps between the user's imagined solution and the mechanisms required to deliver it. LEAP continues the loop while hard blockers remain.

### Stage 1: LEAP Recon

Recon checks whether the project has enough source truth and repo reality to safely generate Build Units or implementation prompts.

Recon must inspect source-of-truth manifests, documentation lifecycle status, stale assumptions, repo reality, branch/worktree/PR drift, existing functionality, cross-layer impacts, layer boundaries, human checkpoints, and the recommended agent execution configuration.

### Stage 2: LEAP Prompt

LEAP Prompt converts approved Recon into a bounded implementation handoff for Codex-style or another AI coding agent.

A valid LEAP Prompt includes objective, current repo reality, source-of-truth instructions, scope, non-goals, constraints, implementation sequence, verification, stop conditions, branch/worktree/commit instructions, source-of-truth update policy, completion report format, and a required Agent Execution Configuration block.

## Agent execution configuration

Every agent-ready LEAP Prompt must explicitly state:

```text
- Agent / Tool
- Model
- Reasoning Level
- Execution Mode
- Scope Scale
- Repository
- Branch / Worktree
- Permissions
- Validation
- Commit Guidance
```

A prompt is not ready for a coding agent unless it tells the user exactly which execution profile to use. If the exact model or reasoning level is unknown, LEAP must recommend one instead of leaving the field blank.

## Current framework

Canonical framework document: [`docs/leap.md`](docs/leap.md).

Historical versions are preserved through Git tags, Git history, [`CHANGELOG.md`](CHANGELOG.md), and [`docs/release-history.md`](docs/release-history.md).

## Quick start

Start here:

- [`docs/00_start_here.md`](docs/00_start_here.md) — the plain-English front door
- [`docs/leap-for-humans.md`](docs/leap-for-humans.md) — the simple explanation of how LEAP thinks
- [`docs/quick-leap-brief.md`](docs/quick-leap-brief.md) — the smallest useful LEAP workflow

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
CONTRIBUTING.md
VERSION.md
docs/
  00_start_here.md
  leap-for-humans.md
  quick-leap-brief.md
  leap.md
  release-history.md
  glossary.md
  agent-profiles.md
  risk-taxonomy.md
  examples/
    small-build-unit.md
    full-layer-recon.md
templates/
  leap-phase-0-template.md
  leap-recon-template.md
  leap-prompt-template.md
prompts/
  README.md
  leap-phase-0-standard.md
  leap-recon-standard.md
  leap-prompt-standard.md
  leap-governance-pass-standard.md
```

## Short rule

```text
No clarity, no build.
No source truth, no Recon.
No repo reality, no prompt.
No non-goals, no agent handoff.
No stop conditions, no coding task.
No execution profile, no agent-ready prompt.
Ask until the idea becomes buildable, then stop asking and build only the bounded task.
```
