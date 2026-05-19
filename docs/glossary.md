# LEAP Glossary

## LEAP

**Layer Execution & Assembly Protocol**.

A framework for turning a layered solution concept into sequenced, governed, implementation-ready AI coding prompts.

## Solution

The system, product, platform, internal tool, data system, AI application, or infrastructure initiative being built.

## Layer

A major capability phase or architectural slice of the solution.

Examples:

- Layer 2 — Intake & Parsing
- Layer 4 — Application Workflow
- Layer 5 — Intelligence, Insights & Optimization
- Layer 6 — Intelligent Decisioning

## Build Unit

A scoped subsection of a layer that can be implemented, tested, and committed independently.

A Build Unit should be:

- specific enough for implementation
- large enough to represent a coherent domain capability
- small enough to be one commit in most cases
- sequenced against earlier Build Units
- explicit about exclusions and boundaries

## LEAP Recon

The analysis, pressure-test, Build Unit generation/refinement, sequencing, and clarification stage.

Recon is run before generating the implementation prompt.

## LEAP Prompt

The final implementation prompt artifact given to Codex or another AI coding agent.

It tells the coding agent how to build the layer sequentially and safely.

## Buildout mode

The execution posture for the layer.

Supported defaults:

- Rapid POC
- Standard
- Production-safe
- Refactor

## Architecture right-sizing

The rule that implementation should neither force new work into a bad architecture nor overbuild speculative infrastructure.

## Hand-jamming

Forcing a new capability into an unsuitable existing architecture because it is convenient in the short term.

LEAP discourages hand-jamming when the current architecture crosses a reasonable tipping point.

## Coding-agent question forecast

A LEAP Recon section that predicts the questions a coding agent might otherwise ask during implementation.

The goal is to answer material questions before the coding run begins.
