# LEAP Code Assistant Recon-Only Request Template

Use this template when working inside a code assistant such as Codex, Cursor, Claude Code, or another agentic development environment where the assistant already has access to the target codebase.

This template is for **LEAP Recon only**. It should inspect the current repo, identify risks, map likely Build Units, and determine whether implementation is safe to plan.

It is not an implementation prompt.

---

## When to use this template

Use this template when:

```text
- the code assistant already has access to the target repo
- you have one solution with a small feature set or one bounded feature area
- you want repo-aware analysis before implementation
- you want to identify existing functionality, source truth, risks, stop conditions, and Build Units
- you do not want the agent to modify files yet
```

Do not use this template when:

```text
- the product idea is still vague
- the target user, problem, MVP, non-goals, or risks are unclear
- the assistant cannot inspect the repo
- you want implementation to begin immediately
```

If the idea is still unclear, run a LEAP Layer 0 / Phase 0 pass first.

---

## Copy-ready prompt (COPY THIS BELOW!)

```text
Run a LEAP Recon on this codebase.

Use the LEAP Framework from:
https://github.com/mjcataldi/leap_framework

Target feature or functionality:
<DESCRIBE THE FEATURE OR FUNCTIONALITY>

You already have access to the target codebase.

Do not implement anything.
Do not modify files.
Do not generate the implementation prompt yet.
Do not make product, architecture, schema, auth, security, privacy, billing, or AI-behavior decisions silently.

Inspect the repo and return a LEAP Recon report that identifies:

- current repo reality
- source-of-truth docs and any stale, missing, or conflicting docs
- existing functionality related to the target feature
- files, routes, models, schemas, components, services, tests, configs, and dependencies likely involved
- whether the feature touches auth, sessions, security, privacy, billing, AI behavior, data models, APIs, or user data
- risks, sensitive areas, and destructive-change concerns
- recommended Build Units
- files or areas that should not be touched
- stop conditions
- tests/checks likely required
- questions that must be answered before generating a LEAP Prompt
- recommended Codex/agent execution configuration for the eventual implementation prompt

If you cannot access required files, source documents, routes, schemas, tests, or configs, stop and say what is missing.

Return only the LEAP Recon report.
```

---

## Expected Recon output

```text
# LEAP Recon — <Target Feature or Functionality>

## 1. Framework Interpretation
## 2. Source-of-Truth Manifest Check
## 3. Phase 0 / Baseline Gate Check
## 4. Repo Reality Reconciliation
## 5. Documentation Lifecycle Review
## 6. Existing Functionality Collision Check
## 7. Stale Assumption Scan
## 8. Cross-Layer Impact Scan
## 9. Layer / Feature Boundary Review
## 10. Generated / Refined Build Unit Inventory
## 11. Recommended Build Sequence
## 12. Dependency and Destructive-Change Review
## 13. Risk Taxonomy Review
## 14. Human Checkpoints Required
## 15. Coding-Agent Risk Forecast
## 16. Recommended Agent Execution Configuration
## 17. Clarification Questions Before LEAP Prompt Generation
## 18. Gate Decision / Next Step
```

---

## Gate decision options

Use one of these gate decisions:

```text
Generate LEAP Prompt
Continue Phase 0
Pressure Test Further
Narrow Scope First
Needs Human Decision
Reconcile Docs First
Resolve Branch Drift First
Do Not Build Yet
```

---

## Recommended Agent Execution Configuration section

If the gate decision is `Generate LEAP Prompt`, include:

```text
## Recommended Agent Execution Configuration

| Field | Recommendation | Rationale |
|---|---|---|
| Agent / Tool | <Codex / Cursor / Claude Code / other> | <why> |
| Model | <exact model name or project default> | <why> |
| Reasoning Level | <low / medium / high / extended> | <why> |
| Execution Mode | <plan-first / implement-directly / implement-with-brief-plan> | <why> |
| Scope Scale | <small task / Build Unit / sublayer / entire layer / repo-wide maintenance> | <why> |
| Repository | <repo name> | <why> |
| Branch / Worktree | <branch/worktree> | <why> |
| Permissions | <allowed changes> | <why> |
| Validation | <tests/lint/typecheck/build/manual checks> | <why> |
| Commit Guidance | <commit convention> | <why> |
```

---

## Stop conditions

The code assistant must stop and report instead of guessing if:

```text
- required files or source documents are missing
- repo reality conflicts with the prompt
- docs conflict with repo reality
- existing implementation contradicts the requested feature
- implementation would violate explicit non-goals
- the feature requires product decisions not yet approved
- the feature requires architecture changes not yet approved
- the feature requires schema, migration, auth, permission, billing, privacy, security, or AI-behavior changes not yet approved
- destructive changes appear necessary but are not explicitly authorized
- branch/worktree/PR drift creates unclear ownership
- tests or validation paths are missing or unclear
- the acceptance criteria are impossible as written
```

---

## Usage note

This template is intentionally lightweight. It is designed to get a user from “I want to try LEAP on this feature” to a useful repo-aware Recon pass quickly.

If the Recon reveals that the user, problem, MVP boundary, non-goals, or risks are unclear, escalate to LEAP Layer 0 / Phase 0 before generating an implementation prompt.
