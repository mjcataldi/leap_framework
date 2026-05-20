# Changelog

All notable changes to the LEAP Framework will be documented here.

## LEAP v1.2 — Source-of-truth and pressure-test hardening

### Added

- Added explicit source-of-truth document intake for application-specific roadmap, status, domain, and architecture files.
- Added source-of-truth review as a required LEAP Recon section.
- Added repo reality reconciliation as a required LEAP Recon section when repository access is available.
- Added a formal Recon pressure-test rubric covering:
  - repo reality
  - already-built collisions
  - branch drift
  - layer boundaries
  - Build Unit atomicity
  - dependencies
  - migrations and destructive changes
  - frontend/backend/API alignment
  - testability
  - truthfulness/source grounding
  - user value
- Added layer boundary review to reduce scope creep and prevent future-layer work from leaking into current-layer implementation.
- Added source-of-truth update policy for LEAP Prompts.
- Added application-repo vs LEAP-repo boundary guidance.
- Added stronger Build Unit fields for source-of-truth alignment, repo reality notes, existing models to reuse, migration risk, and testability.

### Changed

- Updated the README to point to LEAP v1.2 as the current version.
- Updated the LEAP Recon template to include source-of-truth documents, repo reality reconciliation, and pressure-test expectations.
- Updated the LEAP Prompt template to include source-of-truth instructions and update policy.
- Expanded the glossary with v1.2 terms.

### Notes

LEAP v1.2 keeps the same two-stage model as v1.1:

```text
LEAP Recon → LEAP Prompt
```

This is a minor-version hardening release, not a major framework redesign.

## LEAP v1.1 — Initial repository version

### Added

- Generalized LEAP from a Careero-specific workflow to a reusable solution-level framework.
- Established the two-stage workflow:
  - LEAP Recon
  - LEAP Prompt
- Replaced the earlier LHS terminology with **Build Unit**.
- Added Build Unit generation when the user supplies only solution context and target layer intent.
- Added default branch naming convention:
  - `layer<number>_<short_definition>`
- Added coding-agent question forecasting before prompt generation.
- Added clarification-question requirements before LEAP Prompt generation.
- Added required plan mode and reasoning effort recommendations.
- Added buildout-mode defaults:
  - Rapid POC
  - Standard
  - Production-safe
  - Refactor

### Notes

This is the first repository-backed version of LEAP.
