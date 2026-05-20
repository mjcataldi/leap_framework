# LEAP Framework

**LEAP — Layer Execution & Assembly Protocol** is a solution-level framework for turning layered system intent into safe, sequential, implementation-ready AI coding prompts.

LEAP is designed for systems that are built in layers, where each layer can be broken into independently committable **Build Units**.

## Core idea

```text
Solution strategy defines what the system needs.
Application source-of-truth documents define repo-specific reality and constraints.
Layer intent defines the next major capability phase.
Build Units define independently committable implementation subsections.
LEAP Recon decides how the layer should be built.
LEAP Prompt tells the coding agent how to build it.
```

## Two-stage workflow

```text
LEAP Recon → LEAP Prompt
```

### Stage 1: LEAP Recon

LEAP Recon is the analysis, source-of-truth reconciliation, pressure-test, Build Unit generation, sequencing, and clarification stage.

It produces:

- solution and layer interpretation
- source-of-truth document review
- repo reality reconciliation
- formal pressure-test findings
- generated or refined Build Unit inventory
- recommended build sequence
- dependency review
- architecture right-sizing review
- data/destructive-change review
- infrastructure escalation review
- layer boundary review
- coding-agent question forecast
- clarification questions for the user
- recommended prompt settings

### Stage 2: LEAP Prompt

LEAP Prompt converts the approved LEAP Recon into a comprehensive implementation prompt for Codex or another AI coding agent.

It includes:

- source-of-truth instructions
- branch and commit rules
- plan mode
- reasoning effort
- per-Build Unit execution contract
- architecture escalation policy
- destructive-change policy
- layer boundary policy
- source-of-truth update policy
- completion report formats
- final layer completion report

## Current version

Current framework version: **LEAP v1.2**

See [`docs/leap-v1.2.md`](docs/leap-v1.2.md).

Previous version: [`docs/leap-v1.1.md`](docs/leap-v1.1.md).

## Quick start

Use [`templates/leap-recon-template.md`](templates/leap-recon-template.md) to request a Recon pass.

After Recon is approved, use [`templates/leap-prompt-template.md`](templates/leap-prompt-template.md) to generate the final implementation prompt.

## Source-of-truth document model

LEAP v1.2 supports application-specific source-of-truth documents, such as roadmap/status docs, domain model docs, and architecture decision docs.

When provided, LEAP Recon should read these documents first, reconcile them against repo reality when repo access is available, and use them to avoid stale or duplicate implementation planning.

Application-specific planning belongs in the application repo. Generic LEAP framework methodology belongs in this repo.

## Terminology

| Term | Meaning |
|---|---|
| Layer | A major system capability or architectural phase. |
| Build Unit | A scoped subsection of a layer that can be implemented, tested, and committed independently. |
| Source-of-Truth Document | An application-specific roadmap/status/domain/architecture file that governs repo-specific decisions. |
| Repo Reality Reconciliation | Recon step that compares source-of-truth claims against current repository implementation. |
| Pressure-Test Findings | Formal Recon assessment of repo reality, branch drift, layer boundaries, atomicity, dependencies, migrations, alignment, testability, grounding, and user value. |
| LEAP Recon | Analysis and clarification stage before implementation prompt generation. |
| LEAP Prompt | Final implementation prompt artifact for an AI coding agent. |

## Repository structure

```text
README.md
CHANGELOG.md
docs/
  leap-v1.2.md
  leap-v1.1.md
  glossary.md
templates/
  leap-recon-template.md
  leap-prompt-template.md
examples/
  careero-layer5-recon-outline.md
```
