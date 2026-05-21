# LEAP Framework

**LEAP — Layer Execution & Assembly Protocol** is a solution-level framework for turning rough software intent into pressure-tested direction, layered plans, and safe, bounded, implementation-ready AI coding prompts.

LEAP is designed for systems that are built in layers, where each layer can be broken into independently committable **Build Units**. LEAP v1.5 tightens the framework into a gate-based, source-of-truth-aware, model-effort-aware workflow that keeps coding agents from turning vague intent into overbuilt software.

## Core idea

```text
Phase 0 Inception establishes what should be built and why.
Phase 0 now runs in Lite, Standard, or Pro mode and ends with a gate decision.
Solution strategy defines what the system needs.
Application source-of-truth documents define repo-specific reality, constraints, and doc ownership.
Layer intent defines the next major capability phase.
Build Units define independently committable implementation subsections.
LEAP Recon reconciles strategy, docs, branch state, stale assumptions, and repo reality.
LEAP Prompt gives the coding agent a bounded task packet with constraints, verification, and stop conditions.
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
- known / assumed / unknown / contested / needs-decision evidence labels
- directional clarity scoring as a planning signal, not a false-precision score
- market and alternative-solution pressure testing
- simpler non-app solution review
- MVP boundary definition
- explicit non-goals
- strategic plan generation
- lean documentation bootstrap
- human approval before layer planning

Phase 0 ends with one gate decision:

```text
Proceed to Recon | Pressure Test Further | Narrow MVP First | Needs Human Decision | Do Not Build Yet
```

LEAP must not generate implementation plans or coding-agent prompts from vague app ideas.

### Stage 1: LEAP Recon

LEAP Recon is the analysis, source-of-truth reconciliation, repo scan, pressure-test, Build Unit generation, sequencing, cross-layer impact review, stale-assumption scan, and clarification stage.

It produces:

- Phase 0 / source-of-truth gate check
- solution and layer interpretation
- source-of-truth document review
- canonical / supporting / archived doc classification
- repo reality reconciliation
- branch and worktree drift review when available
- strategic plan reconciliation
- stale-doc and stale-assumption findings
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
- human checkpoint requirements
- clarification questions for the user
- recommended model-effort and prompt settings

### Stage 2: LEAP Prompt

LEAP Prompt converts the approved LEAP Recon into a comprehensive implementation prompt for Codex-style or another AI coding agent.

It includes:

- Phase 0 / source-of-truth gate status
- source-of-truth instructions
- branch, worktree, and commit rules
- model-effort guidance
- task objective and user-visible outcome
- explicit in-scope and out-of-scope boundaries
- files or areas to inspect and files or areas not to touch
- non-goals
- implementation constraints
- verification plan
- stop conditions
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

Current framework version: **LEAP v1.5**

See [`docs/leap-v1.5.md`](docs/leap-v1.5.md).

Previous versions:

- [`docs/leap-v1.4.md`](docs/leap-v1.4.md)
- [`docs/leap-v1.3.md`](docs/leap-v1.3.md)
- [`docs/leap-v1.2.md`](docs/leap-v1.2.md)
- [`docs/leap-v1.1.md`](docs/leap-v1.1.md)

## Quick start

For a new software project or major new product direction, start with [`templates/leap-phase-0-template.md`](templates/leap-phase-0-template.md). Choose Lite, Standard, or Pro Inception based on ambiguity and risk.

After Phase 0 is approved, use [`templates/leap-recon-template.md`](templates/leap-recon-template.md) to request a Recon pass for the first target layer.

After Recon is approved, use [`templates/leap-prompt-template.md`](templates/leap-prompt-template.md) to generate the final implementation prompt.

For repeatable workflows, use the operational prompt library under [`prompts/`](prompts/).

## Source-of-truth document model

LEAP v1.5 supports application-specific source-of-truth documents, such as project charters, MVP boundaries, roadmap/status docs, domain model docs, execution logs, and architecture decision docs.

When provided, LEAP Recon should read these documents first, classify them as canonical / supporting / archived, reconcile them against repo reality when repo access is available, and use them to avoid stale or duplicate implementation planning.

Every LEAP-managed application should maintain a `docs/source-of-truth.md` file that identifies the canonical strategy, MVP boundary, implementation strategy, layer map, execution state, doc owner, freshness expectations, and conflict-resolution rule.

Application-specific planning belongs in the application repo. Generic LEAP framework methodology belongs in this repo.

## Terminology

| Term | Meaning |
|---|---|
| Phase 0 Inception | Mandatory project-start workflow that turns rough intent into pressure-tested baseline direction before implementation planning. |
| Phase 0 Mode | Lite, Standard, or Pro discovery depth selected by ambiguity, risk, and blast radius. |
| Gate Decision | The explicit Phase 0 / Recon decision that determines whether LEAP proceeds, narrows scope, pressure-tests further, waits for human input, or stops. |
| Evidence Label | Known, Assumed, Unknown, Contested, or Needs Decision. Used to prevent polished guesses from becoming implementation truth. |
| Clarity Threshold | Directional readiness estimate used to decide whether LEAP should continue discovery, draft a concept brief, or allow implementation strategy. Not a precise score. |
| No-Build Gate | Rule that blocks layer planning and coding-agent prompts until minimum project clarity, source-of-truth docs, and human approval exist. |
| Documentation Bootstrap | Lean docs scaffold created for a LEAP-managed application, with required and conditional docs separated. |
| Layer | A major system capability or architectural phase. |
| Build Unit | A scoped subsection of a layer that can be implemented, tested, and committed independently. |
| Source-of-Truth Document | An application-specific roadmap/status/domain/architecture file that governs repo-specific decisions. |
| Repo Reality Reconciliation | Recon step that compares source-of-truth claims against current repository implementation. |
| Pressure-Test Findings | Formal assessment of app necessity, simpler alternatives, repo reality, branch drift, layer boundaries, atomicity, dependencies, migrations, alignment, testability, grounding, user value, and solution viability. |
| Model-Effort Tier | Standard, Pro Standard, or Pro Extended process depth selected by ambiguity, risk, and blast radius. |
| Stop Condition | A rule that tells the coding agent to stop instead of guessing when requirements, docs, repo reality, security, privacy, or architecture are unclear. |
| LEAP Recon | Analysis and clarification stage before implementation prompt generation. |
| LEAP Prompt | Final bounded implementation prompt artifact for an AI coding agent. |

## Repository structure

```text
README.md
CHANGELOG.md
docs/
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
      v1.5/
    recon/
      v1.5/
      v1.3/
    implementation/
      v1.5/
      v1.3/
    governance/
      v1.5/
      v1.3/
examples/
  careero-layer5-recon-outline.md
```
