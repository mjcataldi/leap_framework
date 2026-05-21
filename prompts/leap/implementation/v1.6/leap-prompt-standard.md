# LEAP Prompt — Standard Implementation Prompt — v1.6

Generate the LEAP Prompt under LEAP v1.6.

The LEAP Recon pass must already be complete, and the user must have approved the required decisions or accepted safe defaults.

A LEAP Prompt is a bounded coding-agent handoff contract. It must not ask the agent to infer product behavior, silently resolve source conflicts, or improvise architecture.

## Required preflight

Confirm before writing the prompt:

```text
- Phase 0 complete or not applicable
- Source-of-truth manifest complete
- Recon approved
- Repo reality checked when repo access exists
- Branch/worktree/PR drift reviewed
- Scope and non-goals defined
- Files/areas to inspect defined
- Files/areas not to touch defined
- Acceptance criteria defined
- Verification path defined
- Stop conditions defined
```

If any item is missing, stop and explain what must happen first.

## Required prompt sections

```text
# <Solution Name> — LEAP Prompt — <Target Layer or Task>

## 1. Objective
- Objective:
- User-visible outcome:
- Definition of done:

## 2. Current Repo Reality
- Target branch:
- Base branch:
- Existing implementation summary:
- Known doc-code conflicts:
- Existing functionality to reuse:

## 3. Source-of-Truth Instructions
Use these sources:
- <canonical / active sources>

Do not use these sources:
- <draft / stale / archived / superseded sources>

If any source conflict appears, stop and report.

## 4. Scope
- In scope:
- Out of scope:
- Non-goals:
- Files/areas to inspect:
- Files/areas not to touch:

## 5. Constraints
- Existing patterns to follow:
- Dependencies allowed/disallowed:
- Architecture constraints:
- Data/privacy/security constraints:
- API/schema/state constraints:
- AI behavior constraints, if relevant:
- UX/accessibility constraints, if relevant:

## 6. Implementation Sequence
- Suggested sequence:
- Build Unit order:
- One Build Unit per commit where feasible:
- Edge cases:
- Error handling:
- Backward compatibility:

## 7. Verification
- Tests to run:
- Manual checks:
- Expected result:
- Verification evidence to report:

## 8. Stop Conditions
Stop and report instead of guessing if:
- required files or sources are missing
- docs conflict with repo reality
- existing implementation contradicts this prompt
- implementation would violate non-goals
- task requires architecture not approved
- task requires touching forbidden files
- task requires new dependency, migration, auth/permission change, billing change, AI behavior change, or sensitive-data handling not approved
- branch/worktree drift creates unclear ownership
- verification cannot be performed or is undefined
- acceptance criteria are impossible as written

## 9. Source-of-Truth Update Policy
- Docs to update:
- Execution log / drift ledger update required:
- Cross-layer impact map update required:

## 10. Completion Report Format
Return:
- Summary of changes
- Files changed
- Tests/checks run
- Deviations from prompt
- Assumptions made
- Stop conditions encountered
- Docs updated or needing update
- Follow-up required
```

Do not include broad cleanup instructions unless cleanup is explicitly scoped and testable.
