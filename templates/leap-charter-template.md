# LEAP Charter Request Template

Use this template when starting a new solution or reconciling an existing project before LEAP Recon, LEAP Prompt, implementation, Validation, or Handoff.

LEAP Charter establishes or reconciles project direction, source-of-truth docs, roadmap posture, implementation posture, and readiness for the next LEAP step. It replaces the active use of the older "Phase 0" label.

LEAP Charter is scan-first and question-second. After the LEAP `AGENTS.md` files are initialized, the preferred invocation should be simple:

```text
Run LEAP Charter.
```

or:

```text
Run LEAP Charter for this repo.
```

The user should not have to fill out a full intake form upfront. The agent should infer as much as possible from the repo and docs, then ask only the questions needed to safely complete the Charter baseline.

## Charter operating model

When a repository or project files are available, the agent must inspect available evidence before asking questions.

Scan and infer from:

- Global `AGENTS.md`
- Repo/project `AGENTS.md`
- Existing documentation
- Repository structure
- Source code and configuration
- Tests
- Scripts
- Package/build files
- CI/CD files
- README content
- Existing roadmap, product, architecture, implementation, validation, and handoff docs

Do not treat missing user-supplied context as a blocker until the repo and docs have been inspected.

## Charter discovery flow

The agent should internally work through the following discovery flow.

### 1. Charter mode

Determine the most likely mode from evidence:

- Greenfield
- Brownfield
- Documentation reconciliation
- Roadmap/source-of-truth reset
- Existing implementation with planning drift
- Agent should recommend

If the mode cannot be determined with reasonable confidence, ask the user in the Discovery Questions section.

### 2. Starting signal

Infer why Charter is being run.

Examples:

- New solution needing baseline docs
- Existing repo needing LEAP documentation alignment
- Existing project with stale, missing, duplicated, or conflicting docs
- Existing implementation ahead of planning docs
- Roadmap needing reconciliation
- Legacy Phase 0 material needing transition to LEAP Charter

If the starting signal cannot be inferred, ask the user in the Discovery Questions section.

### 3. Known context

Populate known context from evidence instead of asking the user to complete it upfront.

Attempt to infer:

- Solution or repo name
- Target users or stakeholders
- Current project purpose
- Current workflow or workaround
- Current implementation posture
- Existing source-of-truth docs
- Missing docs
- Stale docs
- Duplicated or conflicting docs
- Known roadmap, product, architecture, or implementation drift
- Existing decisions
- Open decisions
- Technical preferences or constraints
- Timeline or urgency
- Sensitive data, compliance, AI-behavior, monetization, or risk concerns
- Current readiness for LEAP Recon, LEAP Prompt, Validation, or Handoff

Do not leave these as blank intake fields for the user. Fill what can be filled from evidence. Mark uncertain items clearly. Move unresolved material questions into Discovery Questions.

### 4. Discovery questions

Ask the fewest questions needed to make the next safe gate decision.

Discovery Questions should only include items that materially affect:

- Project direction
- Source-of-truth decisions
- Documentation reconciliation
- Roadmap posture
- MVP or current scope boundary
- Risk posture
- Readiness gate
- Recommended next LEAP step

If no blocking questions remain, state:

```text
No blocking Charter questions remain based on the current repo and documentation scan.
```

## Charter settings

```text
Run LEAP Charter using the current LEAP framework.

Charter settings:
- Scan first and ask questions second.
- Infer Charter mode, starting signal, and known context from repo/docs evidence when available.
- Do not ask the user to complete upfront known-context fields unless no repo or files are available.
- Move unresolved known-context items into Discovery Questions.
- Ask the fewest questions needed to make the next safe gate decision.
- Use the Ideation Loop only to clarify vague intent or unresolved material context before implementation planning.
- Separate Known, Assumed, Unknown, Contested, Needs Decision, and Deprecated items.
- Use readiness gates C0-C5 instead of numeric clarity scores.
- Pressure test whether this should be custom software at all where relevant.
- If Brownfield, inspect and classify existing docs before treating them as source truth.
- If Brownfield, apply this policy:
  Canonicalize forward. Archive backward. Preserve traceability. Never let stale docs compete with source-of-truth docs.
- Do not generate runtime implementation changes unless explicitly asked.
- Capture runtime work as follow-up LEAP Recon, LEAP Prompt, or LEAP LHS recommendations.
- Use LHS only when staged repo/docs work is warranted by implementation gravity. Charter does not use LHS by default.

Required Charter workflow:
1. Scan available repo, docs, and AGENTS guidance.
2. Preserve the raw invocation or starting signal.
3. Determine Charter mode.
4. Infer known context from evidence.
5. Label evidence and assumptions.
6. Identify missing, stale, duplicated, conflicting, or drifted docs.
7. Identify repo/code/config/test evidence that disagrees with docs.
8. Ask discovery questions only for unresolved material context.
9. Run no-build / alternative-solution review where relevant.
10. Define MVP boundary or current scope boundary.
11. Define concrete non-goals.
12. Recommend documentation baseline and source-of-truth posture.
13. Create gap and drift register.
14. Create Brownfield migration map if existing docs are reconciled.
15. Recommend next LEAP Recon, LEAP Prompt, Validation, Handoff, or LHS.
16. Make readiness gate decision.

Return the LEAP Charter output only.
If more information is needed, ask the next discovery round instead of producing implementation plans.
```

## Fallback mode when no repo/files are available

Use this only when no repository or project files are available to scan.

```text
Run LEAP Charter using the current LEAP framework.

No repo or project files are available to scan.

Minimal starting context:
- Solution or working title:
- Greenfield / Brownfield / you recommend:
- Brief project description:
- Known docs, roadmap notes, or source-of-truth concerns:
- Known constraints, risks, or sensitive areas:
```

## Expected Charter sections

```text
# LEAP Charter - <Project Name or Working Title>

## 1. Mode and Starting Signal
## 2. Repository and Documentation Scan Summary
## 3. Current Understanding
## 4. Evidence Labels
### Known
### Assumed
### Unknown
### Contested
### Needs Decision
### Deprecated
## 5. Discovery Questions, if needed
## 6. Readiness Gate
## 7. Source-of-Truth Inventory and Recommendation
## 8. Gap and Drift Register
## 9. Scope Boundary and Non-Goals
## 10. Risks and Constraints
## 11. No-Build / Alternative-Solution Review, if relevant
## 12. Migration Map, if Brownfield
## 13. Prompt Backlog Recommendations
## 14. Recommended Next LEAP Recon / LEAP Prompt / LEAP LHS / Validation / Handoff
## 15. Gate Decision / Next Step
```

## LEAP LHS note

LEAP LHS is a structured LEAP Prompt format for layered implementation work using the House Standard. It is useful when work is layered, staged, or large enough to require House Standard-style execution. Not every LEAP Prompt is an LHS prompt.

Greenfield Charter should usually avoid LHS during early product shaping, naming, ideation, MVP definition, or strategic discovery. Brownfield Charter may use or recommend LHS only after the reconciliation plan is clear and repo-changing documentation work needs staged execution, commit boundaries, tests/docs checks, or source-truth validation.
