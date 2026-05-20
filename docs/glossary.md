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
- Layer 7 — Opportunity Model Strategy

## Build Unit

A scoped subsection of a layer that can be implemented, tested, and committed independently.

A Build Unit should be:

- specific enough for implementation
- large enough to represent a coherent domain capability
- small enough to be one commit in most cases
- sequenced against earlier Build Units
- explicit about exclusions and boundaries
- aligned to source-of-truth documents when provided
- checked against repo reality when repo access is available

## Source-of-Truth Document

An application-specific roadmap, layer status, domain model, architecture, or implementation-status document that governs repo-specific planning.

LEAP uses source-of-truth documents to avoid relying on stale chat history and to prevent rebuilding capabilities that already exist.

## Source-of-Truth Review

A LEAP Recon section that extracts relevant decisions, constraints, current-status claims, and required documentation updates from application-specific source-of-truth documents.

## Repo Reality Reconciliation

A LEAP Recon section that compares source-of-truth claims against the actual repository state when repo access is available.

If repo reality conflicts with the source-of-truth document, repo reality should guide implementation planning, and the documentation conflict should be reported.

## Pressure-Test Findings

A LEAP Recon section that evaluates whether the target layer and Build Units are safe, useful, properly bounded, and implementable.

LEAP v1.2 pressure testing includes:

- repo reality check
- already-built collision check
- branch drift check
- layer boundary check
- Build Unit atomicity check
- dependency check
- migration/destructive-change check
- frontend/backend/API alignment check
- testability check
- truthfulness/source-grounding check where applicable
- user value check

## LEAP Recon

The analysis, source-of-truth reconciliation, pressure-test, Build Unit generation/refinement, sequencing, and clarification stage.

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

## Layer Boundary Review

A LEAP Recon section that separates what belongs in the target layer from work that belongs in prior or future layers.

This helps prevent scope creep and accidental implementation of integrations, automation, productization, or marketplace features before their intended layer.

## Source-of-Truth Update Policy

A LEAP Prompt section that tells the coding agent whether and when to update application-specific roadmap/status documents after implementation changes reality.

Generic LEAP methodology should not be updated from an application implementation prompt unless the prompt explicitly targets the LEAP repository.

## Coding-agent question forecast

A LEAP Recon section that predicts the questions a coding agent might otherwise ask during implementation.

The goal is to answer material questions before the coding run begins.
