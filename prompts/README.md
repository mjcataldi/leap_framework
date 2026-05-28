# LEAP Prompt Library

This directory contains reusable operational prompts for running LEAP workflows.

The `templates/` directory contains compact request templates. The `prompts/` directory contains fuller copy-ready operational prompts for recurring work.

## Prompt categories

```text
prompts/
  README.md
  leap-phase-0-standard.md
  leap-recon-standard.md
  leap-prompt-standard.md
  leap-governance-pass-standard.md
```

## Current public workflow

Use the current top-level templates:

```text
templates/leap-phase-0-template.md
templates/leap-recon-template.md
templates/leap-prompt-template.md
```

Use the current adoption docs first when onboarding new users:

```text
docs/00_start_here.md
docs/leap-for-humans.md
docs/quick-leap-brief.md
docs/agent-profiles.md
docs/risk-taxonomy.md
```

## Categories

### Phase 0 prompts

Use Phase 0 prompts before Recon when project direction, target user, current workflow, MVP boundary, risks, non-goals, no-build alternatives, or source-of-truth baseline are unclear.

Phase 0 includes the Ideation Loop: targeted question cycles that turn vague human intent into buildable mechanisms.

### Recon prompts

Use Recon prompts before implementation. They inspect source-of-truth manifests, document lifecycle status, repository reality, branch/worktree/PR drift, strategic-plan alignment, stale assumptions, existing functionality, cross-layer impact, risk, destructive-change implications, and recommended agent execution configuration before creating implementation prompts.

### Implementation prompts

Use implementation prompts after Recon is complete and the Build Unit sequence has been approved or defaults have been accepted. These prompts are intended for Codex-style or another coding agent.

An implementation prompt is not agent-ready unless it includes an explicit agent/tool, model, reasoning level, execution mode, validation plan, and stop conditions.

### Governance prompts

Use governance prompts outside normal layer implementation when the repo needs reconciliation, roadmap correction, branch/worktree drift review, cross-layer impact review, stale-plan cleanup, stale-prompt cleanup, source-of-truth ownership cleanup, or agent/model/reasoning guidance cleanup.

## Current prompt files

The active prompt library uses canonical root-level files under `prompts/`.

Current files:

```text
prompts/leap-phase-0-standard.md
prompts/leap-recon-standard.md
prompts/leap-prompt-standard.md
prompts/leap-governance-pass-standard.md
```

Operational prompt files represent the current canonical LEAP workflow. Historical prompt versions are preserved through Git tags and Git history.

## LEAP process tier guidance

Use the smallest LEAP process tier that controls the risk:

```text
Standard — small, clear, low-risk tasks
Thinking Extended — Phase 0 discovery, MVP/non-goal work, moderate Recon, bounded prompt drafting
Pro Standard — existing repos, partial implementation, multiple docs, cross-layer review, significant refactor planning
Pro Extended — strategic pivots, stale docs, branch drift, parallel agents, privacy/security-sensitive workflows, high-risk AI behavior
```

## Agent reasoning-level guidance

Use the smallest agent reasoning level that controls the implementation risk:

```text
Low — tiny localized edits, typo fixes, obvious one-file changes
Medium — small bounded implementation, clear UI fixes, simple tests, isolated refactors
High — Build Units, sublayers, multi-file features, state workflows, cross-component UX, meaningful test updates
Extended — full-layer implementation, architecture-sensitive work, repo-wide refactors, parallel-agent sequencing, stale-doc reconciliation, destructive schema/data-model changes, sensitive AI behavior
```

LEAP process tier and agent reasoning level are related, but they are not the same thing. LEAP process tier controls how much framework analysis happens before prompt generation. Agent reasoning level controls how the implementation agent should be run after the prompt is generated.

## Public rule

```text
Ask until the idea becomes buildable.
Then stop asking and build only the bounded task.
```

Use the current templates when you need readiness gates, source-of-truth manifests, doc lifecycle status, drift ledgers, branch/worktree/PR review, strict coding-agent stop conditions, and explicit agent/model/reasoning execution settings.
