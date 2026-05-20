# LEAP Prompt Library

This directory contains reusable operational prompts for running LEAP workflows.

The `templates/` directory contains compact request templates. The `prompts/` directory contains fuller copy-ready operational prompts for recurring work.

## Prompt categories

```text
prompts/
  leap/
    recon/
      v1.3/
    implementation/
      v1.3/
    governance/
      v1.3/
```

## Categories

### Recon prompts

Use Recon prompts before implementation. They are designed to inspect source-of-truth documents, repository reality, branch drift, strategic-plan alignment, and cross-layer impact before creating implementation prompts.

### Implementation prompts

Use implementation prompts after Recon is complete and the Build Unit sequence has been approved or defaults have been accepted. These prompts are intended for Codex or another coding agent.

### Governance prompts

Use governance prompts outside normal layer implementation when the repo needs reconciliation, roadmap correction, branch drift review, cross-layer impact review, or stale-plan cleanup.

## Versioning

Prompt files are versioned by LEAP framework version.

Example:

```text
prompts/leap/recon/v1.3/leap-recon-standard.md
```

This allows stable prompts to coexist with newer experimental prompts as LEAP evolves.

## Usage guidance

Use the shortest suitable prompt that preserves the required governance. For quick requests, the templates may be enough. For repeatable or high-stakes workflows, use the full prompt files.
