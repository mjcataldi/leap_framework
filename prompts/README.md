# LEAP Prompt Library

This directory contains reusable operational prompts for running LEAP workflows.

The `templates/` directory contains compact request templates. The `prompts/` directory contains fuller copy-ready operational prompts for recurring work.

## Prompt categories

```text
prompts/
  leap/
    phase-0/
      v1.7/
      v1.6/
      v1.5/
    recon/
      v1.7/
      v1.6/
      v1.5/
      v1.3/
    implementation/
      v1.7/
      v1.6/
      v1.5/
      v1.3/
    governance/
      v1.7/
      v1.6/
      v1.5/
      v1.3/
```

## Categories

### Phase 0 prompts

Use Phase 0 prompts before Recon when project direction, target user, current workflow, MVP boundary, risks, non-goals, no-build alternatives, or source-of-truth baseline are unclear.

### Recon prompts

Use Recon prompts before implementation. They inspect source-of-truth manifests, document lifecycle status, repository reality, branch/worktree/PR drift, strategic-plan alignment, stale assumptions, existing functionality, cross-layer impact, and recommended Codex execution configuration before creating implementation prompts.

### Implementation prompts

Use implementation prompts after Recon is complete and the Build Unit sequence has been approved or defaults have been accepted. These prompts are intended for Codex-style or another coding agent.

A v1.7 implementation prompt is not Codex-ready unless it includes an explicit model and reasoning level.

### Governance prompts

Use governance prompts outside normal layer implementation when the repo needs reconciliation, roadmap correction, branch/worktree drift review, cross-layer impact review, stale-plan cleanup, stale-prompt cleanup, source-of-truth ownership cleanup, or model/reasoning guidance cleanup.

## Versioning

Prompt files are versioned by LEAP framework version.

Example:

```text
prompts/leap/recon/v1.7/leap-recon-standard.md
```

This allows stable prompts to coexist with newer experimental prompts as LEAP evolves.

## LEAP process tier guidance

Use the smallest LEAP process tier that controls the risk:

```text
Standard — small, clear, low-risk tasks
Thinking Extended — Phase 0 discovery, MVP/non-goal work, moderate Recon, bounded prompt drafting
Pro Standard — existing repos, partial implementation, multiple docs, cross-layer review, significant refactor planning
Pro Extended — strategic pivots, stale docs, branch drift, parallel agents, privacy/security-sensitive workflows, high-risk AI behavior
```

## Codex reasoning-level guidance

Use the smallest Codex reasoning level that controls the implementation risk:

```text
Low — tiny localized edits, typo fixes, obvious one-file changes
Medium — small bounded implementation, clear UI fixes, simple tests, isolated refactors
High — Build Units, sublayers, multi-file features, state workflows, cross-component UX, meaningful test updates
Extended — full-layer implementation, architecture-sensitive work, repo-wide refactors, parallel-agent sequencing, stale-doc reconciliation, destructive schema/data-model changes, sensitive AI behavior
```

LEAP process tier and Codex reasoning level are related, but they are not the same thing. LEAP process tier controls how much framework analysis happens before prompt generation. Codex reasoning level controls how the implementation agent should be run after the prompt is generated.

Use v1.7 prompts when you need readiness gates, source-of-truth manifests, doc lifecycle status, drift ledgers, branch/worktree/PR review, strict coding-agent stop conditions, and explicit Codex model/reasoning execution settings.
