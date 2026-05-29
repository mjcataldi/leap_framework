# LEAP Framework

**LEAP - Layered Execution & Alignment Protocol** is a software delivery framework for turning rough intent into pressure-tested direction, source-grounded plans, and safe, bounded, implementation-ready AI coding-agent handoffs.

LEAP started as a practical response to AI-assisted software delivery: coding agents can move quickly, but speed is only useful when the idea is clear, the source truth is current, the repo reality is understood, and the implementation task is bounded.

The active repository presents the current canonical LEAP framework document and current operational prompts without versioned filenames. Historical versions are preserved through Git tags, Git history, `CHANGELOG.md`, and `docs/release-history.md`.

## Core idea

```text
People often begin with a feeling for what they want built.
LEAP turns that feeling into a testable delivery path.

LEAP Charter establishes or reconciles project direction, source-of-truth docs, roadmap, and implementation posture.
LEAP Recon investigates a focused area, gap, risk, feature, or architectural question.
LEAP Prompt produces Codex-ready instructions for analysis, documentation, implementation, or remediation.
Implementation executes the approved prompt in the repository.
Validation/Handoff verifies changes, checks docs/tests, summarizes work, and recommends follow-up prompts.
```

## Lifecycle

```text
LEAP Charter -> LEAP Recon -> LEAP Prompt -> Implementation -> Validation/Handoff
```

### LEAP Charter

Use LEAP Charter when project direction, source truth, documentation structure, roadmap, implementation posture, or existing-project alignment needs to be established or reconciled.

Greenfield Mode is for brand-new projects, early-stage ideas, or solutions that do not yet have a stable repo, roadmap, architecture, or documentation structure.

Brownfield Mode is for existing or mid-buildout projects where LEAP needs to inspect the repo, reconcile documentation, identify gaps, establish source-of-truth docs, and prepare future LEAP Recon, LEAP Prompt, or LHS work.

Brownfield reconciliation follows this policy:

```text
Canonicalize forward.
Archive backward.
Preserve traceability.
Never let stale docs compete with source-of-truth docs.
```

### LEAP Recon

Recon investigates a focused area, gap, risk, feature, or architectural question before implementation planning.

Recon must inspect source-of-truth manifests, documentation lifecycle status, stale assumptions, repo reality, branch/worktree/PR drift, existing functionality, cross-layer impacts, layer boundaries, human checkpoints, and the recommended agent execution configuration.

### LEAP Prompt

LEAP Prompt converts approved Charter and Recon findings into Codex-ready instructions for analysis, documentation, implementation, or remediation.

A valid LEAP Prompt includes objective, current repo reality, source-of-truth instructions, scope, non-goals, constraints, implementation sequence, verification, stop conditions, branch/worktree/commit instructions, source-of-truth update policy, completion report format, and a required Agent Execution Configuration block.

LEAP LHS is not a mandatory lifecycle stage. It is a structured LEAP Prompt format for layered implementation work using the House Standard. Use it when work is layered, staged, or large enough to require House Standard-style execution. Not every LEAP Prompt is an LHS prompt.

### Implementation

Implementation is the execution of the approved LEAP Prompt by Codex or another coding agent.

Implementation should stay within the approved scope, follow repo patterns, preserve non-goals, and stop when the prompt's stop conditions are met.

### Validation/Handoff

Validation/Handoff is the required completion step where Codex verifies changes, checks docs/tests, summarizes work, and recommends follow-up prompts.

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

Charter reference: [`docs/leap-charter.md`](docs/leap-charter.md).

Historical versions are preserved through Git tags, Git history, [`CHANGELOG.md`](CHANGELOG.md), and [`docs/release-history.md`](docs/release-history.md).

## Quick start

Start here:

- [`docs/00_start_here.md`](docs/00_start_here.md) - the plain-English front door
- [`docs/leap-charter.md`](docs/leap-charter.md) - Charter modes and brownfield documentation reconciliation
- [`docs/leap-for-humans.md`](docs/leap-for-humans.md) - the simple explanation of how LEAP thinks
- [`docs/quick-leap-brief.md`](docs/quick-leap-brief.md) - the smallest useful LEAP workflow

For a new software project, major new product direction, or existing project that needs documentation reconciliation, start with [`templates/leap-charter-template.md`](templates/leap-charter-template.md).

After Charter is approved, use [`templates/leap-recon-template.md`](templates/leap-recon-template.md) to request a Recon pass for the first focused area, target layer, feature, risk, or architectural question.

After Recon is approved, use [`templates/leap-prompt-template.md`](templates/leap-prompt-template.md) to generate the final implementation, documentation, analysis, or remediation prompt.

For repeatable workflows, use the operational prompt library under [`prompts/`](prompts/).

## Source-of-truth document model

Every serious LEAP-managed application should maintain a source-of-truth manifest. The manifest identifies canonical and active docs, draft/stale/archived/delete-candidate docs, source ownership, current branch, relevant PRs, repo reality, doc-code conflicts, and the human owner/approver.

Docs should be classified as:

```text
Canonical | Supporting | Current but poorly organized | Partially useful | Stale | Conflicting | Duplicate | Completed implementation plan | Misleading | Archived | Unknown
```

Generated docs are Draft until explicitly ratified. Archived docs are historical unless a current canonical document explicitly references them.

## Repository structure

```text
README.md
CHANGELOG.md
CONTRIBUTING.md
VERSION.md
docs/
  00_start_here.md
  leap-charter.md
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
  leap-charter-template.md
  leap-recon-template.md
  leap-prompt-template.md
prompts/
  README.md
  leap-charter-standard.md
  leap-recon-standard.md
  leap-prompt-standard.md
  leap-governance-pass-standard.md
```

Compatibility stubs remain at `templates/leap-phase-0-template.md` and `prompts/leap-phase-0-standard.md` for older links.

## Short rule

```text
No clarity, no build.
No source truth, no Recon.
No repo reality, no prompt.
No non-goals, no agent handoff.
No stop conditions, no coding task.
No execution profile, no agent-ready prompt.
Canonical docs first.
Archived docs are historical.
Ask until the idea becomes buildable, then stop asking and build only the bounded task.
```
