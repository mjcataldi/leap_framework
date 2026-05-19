# LEAP Framework

**LEAP — Layer Execution & Assembly Protocol** is a solution-level framework for turning layered system intent into safe, sequential, implementation-ready AI coding prompts.

LEAP is designed for systems that are built in layers, where each layer can be broken into independently committable **Build Units**.

## Core idea

```text
Solution strategy defines what the system needs.
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

LEAP Recon is the analysis, pressure-test, Build Unit generation, sequencing, and clarification stage.

It produces:

- solution and layer interpretation
- generated or refined Build Unit inventory
- recommended build sequence
- dependency review
- architecture right-sizing review
- data/destructive-change review
- infrastructure escalation review
- coding-agent question forecast
- clarification questions for the user
- recommended prompt settings

### Stage 2: LEAP Prompt

LEAP Prompt converts the approved LEAP Recon into a comprehensive implementation prompt for Codex or another AI coding agent.

It includes:

- branch and commit rules
- plan mode
- reasoning effort
- per-Build Unit execution contract
- architecture escalation policy
- destructive-change policy
- completion report formats
- final layer completion report

## Current version

Current framework version: **LEAP v1.1**

See [`docs/leap-v1.1.md`](docs/leap-v1.1.md).

## Quick start

Use [`templates/leap-recon-template.md`](templates/leap-recon-template.md) to request a Recon pass.

After Recon is approved, use [`templates/leap-prompt-template.md`](templates/leap-prompt-template.md) to generate the final implementation prompt.

## Terminology

| Term | Meaning |
|---|---|
| Layer | A major system capability or architectural phase. |
| Build Unit | A scoped subsection of a layer that can be implemented, tested, and committed independently. |
| LEAP Recon | Analysis and clarification stage before implementation prompt generation. |
| LEAP Prompt | Final implementation prompt artifact for an AI coding agent. |

## Repository structure

```text
README.md
CHANGELOG.md
docs/
  leap-v1.1.md
  glossary.md
templates/
  leap-recon-template.md
  leap-prompt-template.md
examples/
  careero-layer5-recon-outline.md
```
