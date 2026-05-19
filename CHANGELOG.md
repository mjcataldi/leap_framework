# Changelog

All notable changes to the LEAP Framework will be documented here.

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
