# LEAP Framework

**LEAP — Layer Execution & Assembly Protocol** is a solution-level framework for turning rough software intent into pressure-tested direction, layered plans, and safe, sequential, implementation-ready AI coding prompts.

LEAP is designed for systems that are built in layers, where each layer can be broken into independently committable **Build Units**.

## Core idea

```text
Phase 0 Inception establishes what should be built and why.
Solution strategy defines what the system needs.
Application source-of-truth documents define repo-specific reality and constraints.
Layer intent defines the next major capability phase.
Build Units define independently committable implementation subsections.
LEAP Recon decides how the layer should be built.
LEAP Prompt tells the coding agent how to build it.
```

## Three-stage workflow

```text
LEAP Phase 0 Inception → LEAP Recon → LEAP Prompt
```

### Phase 0: LEAP Inception

LEAP Inception is the mandatory project-start phase for new software projects or major new product directions.

It converts rough ideas into a baseline project direction through:

- idea intake
- Socratic discovery
- directional clarity scoring
- market and alternative-solution pressure testing
- MVP boundary definition
- strategic plan generation
- documentation bootstrap
- human approval before layer planning

LEAP must not generate implementation plans or coding-agent prompts from vague app ideas.

### Stage 1: LEAP Recon

LEAP Recon is the analysis, source-of-truth reconciliation, repo scan, pressure-test, Build Unit generation, sequencing, cross-layer impact review, and clarification stage.

It produces:

- Phase 0 / source-of-truth gate check
- solution and layer interpretation
- source-of-truth document review
- repo reality reconciliation
- strategic plan reconciliation
- cross-layer impact scan
- formal pressure-test findings
- generated or refined Build Unit inventory
- recommended build sequence
- dependency review
- architecture right-sizing review
- data/destructive-change review
- infrastructure escalation review
- layer boundary review
- execution log expectations
- coding-agent question forecast
- clarification questions for the user
- recommended prompt settings

### Stage 2: LEAP Prompt

LEAP Prompt converts the approved LEAP Recon into a comprehensive implementation prompt for Codex or another AI coding agent.

It includes:

- Phase 0 / source-of-truth gate status
- source-of-truth instructions
- branch and commit rules
- plan mode
- reasoning effort
- per-Build Unit execution contract
- architecture escalation policy
- destructive-change policy
- layer boundary policy
- source-of-truth update policy
- execution log policy
- cross-layer impact policy
- completion report formats
- final layer completion report

## Current version

Current framework version: **LEAP v1.4**

See [`docs/leap-v1.4.md`](docs/leap-v1.4.md).

Previous versions:

- [`docs/leap-v1.3.md`](docs/leap-v1.3.md)
- [`docs/leap-v1.2.md`](docs/leap-v1.2.md)
- [`docs/leap-v1.1.md`](docs/leap-v1.1.md)

## Quick start

For a new software project or major new product direction, start with [`templates/leap-phase-0-template.md`](templates/leap-phase-0-template.md).

After Phase 0 is approved, use [`templates/leap-recon-template.md`](templates/leap-recon-template.md) to request a Recon pass for the first target layer.

After Recon is approved, use [`templates/leap-prompt-template.md`](templates/leap-prompt-template.md) to generate the final implementation prompt.

## Source-of-truth document model

LEAP v1.4 supports application-specific source-of-truth documents, such as project charters, MVP boundaries, roadmap/status docs, domain model docs, execution logs, and architecture decision docs.

When provided, LEAP Recon should read these documents first, reconcile them against repo reality when repo access is available, and use them to avoid stale or duplicate implementation planning.

Every LEAP-managed application should maintain a `docs/source-of-truth.md` file that identifies the canonical strategy, MVP boundary, implementation strategy, layer map, and execution state.

Application-specific planning belongs in the application repo. Generic LEAP framework methodology belongs in this repo.

## Terminology

| Term | Meaning |
|---|---|
| Phase 0 Inception | Mandatory project-start workflow that turns rough intent into pressure-tested baseline direction before implementation planning. |
| Clarity Threshold | Directional readiness estimate used to decide whether LEAP should continue discovery, draft a concept brief, or allow implementation strategy. |
| No-Build Gate | Rule that blocks layer planning and coding-agent prompts until minimum project clarity, source-of-truth docs, and human approval exist. |
| Documentation Bootstrap | Initial lean docs scaffold created for a LEAP-managed application. |
| Layer | A major system capability or architectural phase. |
| Build Unit | A scoped subsection of a layer that can be implemented, tested, and committed independently. |
| Source-of-Truth Document | An application-specific roadmap/status/domain/architecture file that governs repo-specific decisions. |
| Repo Reality Reconciliation | Recon step that compares source-of-truth claims against current repository implementation. |
| Pressure-Test Findings | Formal assessment of repo reality, branch drift, layer boundaries, atomicity, dependencies, migrations, alignment, testability, grounding, user value, and solution viability. |
| LEAP Recon | Analysis and clarification stage before implementation prompt generation. |
| LEAP Prompt | Final implementation prompt artifact for an AI coding agent. |

## Repository structure

```text
README.md
CHANGELOG.md
docs/
  leap-v1.4.md
  leap-v1.3.md
  leap-v1.2.md
  leap-v1.1.md
  glossary.md
templates/
  leap-phase-0-template.md
  leap-recon-template.md
  leap-prompt-template.md
examples/
  careero-layer5-recon-outline.md
```
