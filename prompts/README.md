# LEAP Prompt Library

This directory contains reusable operational prompts for running LEAP workflows.

The `templates/` directory contains compact request templates. The `prompts/` directory contains fuller copy-ready operational prompts for recurring work.

## Prompt categories

```text
prompts/
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
```

## Categories

### Phase 0 prompts

Use Phase 0 prompts before Recon when project direction, target user, current workflow, MVP boundary, risks, non-goals, no-build alternatives, or source-of-truth baseline are unclear.

### Recon prompts

Use Recon prompts before implementation. They inspect source-of-truth manifests, document lifecycle status, repository reality, branch/worktree/PR drift, strategic-plan alignment, stale assumptions, existing functionality, and cross-layer impact before creating implementation prompts.

### Implementation prompts

Use implementation prompts after Recon is complete and the Build Unit sequence has been approved or defaults have been accepted. These prompts are intended for Codex-style or another coding agent.

### Governance prompts

Use governance prompts outside normal layer implementation when the repo needs reconciliation, roadmap correction, branch/worktree drift review, cross-layer impact review, stale-plan cleanup, stale-prompt cleanup, or source-of-truth ownership cleanup.

## Versioning

Prompt files are versioned by LEAP framework version.

Example:

```text
prompts/leap/recon/v1.6/leap-recon-standard.md
```

This allows stable prompts to coexist with newer experimental prompts as LEAP evolves.

## Model tier guidance

Use the smallest tier that controls the risk:

```text
Standard — small, clear, low-risk tasks
Thinking Extended — Phase 0 discovery, MVP/non-goal work, moderate Recon, bounded prompt drafting
Pro Standard — existing repos, partial implementation, multiple docs, cross-layer review, significant refactor planning
Pro Extended — strategic pivots, stale docs, branch drift, parallel agents, privacy/security-sensitive workflows, high-risk AI behavior
```

Use v1.6 prompts when you need readiness gates, source-of-truth manifests, doc lifecycle status, drift ledgers, branch/worktree/PR review, or strict coding-agent stop conditions.
