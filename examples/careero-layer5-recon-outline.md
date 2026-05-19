# Example — Careero Layer 5 LEAP Recon Outline

This example shows how LEAP can organize a layer where Build Unit sketches already exist.

## Solution/system overview

- **Solution name:** Careero
- **Solution type:** Job-search workflow and career-navigation platform
- **High-level goal:** Help users manage opportunities, evaluate role fit, generate truthful application materials, and track application progress across parallel search tracks.
- **Current state:** Layers 0–4 define product foundation, platform, intake/parsing, evaluation/artifacts, and application workflow.
- **Known constraints:** User-first, AI-grounded, no fabrication, calm UX, avoid marketplace drift.

## Target layer

- Layer 5 — Intelligence, Insights & Optimization

## Generated branch

```text
layer5_insights_optimization
```

If the user already has a branch named `layer5`, use that instead.

## Buildout mode

```yaml
buildout_mode: Rapid POC
plan_required: false
reasoning_effort: high
destructive_changes_allowed: true
production_compatibility_required: false
one_build_unit_per_commit: true
```

## Example Build Units

1. Search Analytics Engine
2. Opportunity Intelligence
3. Artifact Performance Intelligence
4. STRIDE Insight Expansion
5. Recruiter & Source Intelligence
6. Compensation & Market Intelligence
7. Search Health & Sustainability
8. Recommendation & Guidance Engine
9. Historical Learning System
10. Insight Governance & Explainability

## Example Recon question forecast

1. Should recommendations be persisted, computed on demand, or both?
   - Recommended default: Persist user-visible recommendations that can be dismissed/reviewed; compute transient recommendations on demand.

2. Should duplicate opportunity detection use simple heuristics or semantic similarity infrastructure?
   - Recommended default: Start with simple heuristics; report vector database as future infrastructure only if needed.

3. Should analytics rely on existing workflow records or introduce an analytics event model?
   - Recommended default: Use existing records first; add an `AnalyticsEvent` only when missing activity cannot be derived cleanly.

4. Should search-health guidance include emotional language?
   - Recommended default: Use gentle, non-clinical product guidance only. No diagnosis, shame, streaks, or daily-goal pressure.

## Next step reminder

At the end of LEAP Recon, remind the user:

```text
When you are ready, say: “Generate the LEAP Prompt.”
```
