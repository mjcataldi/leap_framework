# LEAP Prompt — Standard Implementation Prompt

Generate the LEAP Prompt using the current LEAP framework.

The LEAP Recon pass must already be complete, and the user must have approved the required decisions or accepted safe defaults.

A LEAP Prompt is a bounded coding-agent handoff contract. It must not ask the agent to infer product behavior, silently resolve source conflicts, improvise architecture, or guess the execution profile.

## Required preflight

Confirm before writing the prompt:

```text
- Phase 0 complete or not applicable
- Ideation Loop complete or residual questions resolved
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
- Destructive-change permission stated
- Agent / Tool selected or recommended
- Model selected or recommended
- Reasoning level selected or recommended
```

If any item is missing, stop and explain what must happen first.

## Required prompt sections

```text
# <Solution Name> — LEAP Prompt — <Target Layer or Task>

## 1. Agent Execution Configuration

| Field | Value |
|---|---|
| Agent / Tool | <Codex / Claude Code / Cursor / other> |
| Model | <exact model name or approved project default> |
| Reasoning Level | <low / medium / high / extended / project-approved enum> |
| Execution Mode | <recon-only / plan-first / implement-directly / implement-with-brief-plan> |
| Scope Scale | <small task / Build Unit / sublayer / entire layer / repo-wide maintenance> |
| Repository | <owner/repo or local repo name> |
| Branch / Worktree | <target branch/worktree> |
| Permissions | <allowed modifications> |
| Validation | <tests/lint/typecheck/build/manual checks> |
| Commit Guidance | <commit message convention or none> |

## 2. Objective
- Objective:
- User-visible outcome:
- Definition of done:

## 3. Current Repo Reality
- Target branch:
- Base branch:
- Existing implementation summary:
- Known doc-code conflicts:
- Existing functionality to reuse:

## 4. Source-of-Truth Instructions
Use these sources:
- <canonical / active sources>

Do not use these sources:
- <draft / stale / archived / superseded sources>

If any source conflict appears, stop and report.

## 5. Scope
- In scope:
- Out of scope:
- Non-goals:
- Files/areas to inspect:
- Files/areas not to touch:

## 6. Constraints
- Existing patterns to follow:
- Dependencies allowed/disallowed:
- Architecture constraints:
- Data/privacy/security constraints:
- API/schema/state constraints:
- AI behavior constraints, if relevant:
- UX/accessibility constraints, if relevant:
- Destructive changes: allowed / not allowed / allowed only in these areas:
- Rollback/data preservation requirements:

## 7. Implementation Sequence
- Suggested sequence:
- Build Unit order:
- One Build Unit per commit where feasible:
- Edge cases:
- Error handling:
- Backward compatibility:

## 8. Verification
- Tests to run:
- Manual checks:
- Expected result:
- Verification evidence to report:

## 9. Stop Conditions
Stop and report instead of guessing if:
- required files or sources are missing
- docs conflict with repo reality
- existing implementation contradicts this prompt
- implementation would violate non-goals
- task requires architecture not approved
- task requires touching forbidden files
- task requires new dependency, migration, auth/permission change, billing change, AI behavior change, or sensitive-data handling not approved
- destructive changes are required but not explicitly authorized
- branch/worktree drift creates unclear ownership
- verification cannot be performed or is undefined
- acceptance criteria are impossible as written
- requested agent/tool is unavailable and no approved fallback is provided
- requested model is unavailable and no approved fallback is provided
- requested reasoning level is unavailable and no approved fallback is provided

## 10. Branch / Worktree / Commit Instructions
- Branch/worktree:
- Commit guidance:
- One Build Unit per commit:
- Merge/order notes:

## 11. Source-of-Truth Update Policy
- Docs to update:
- Execution log / drift ledger update required:
- Cross-layer impact map update required:

## 12. Completion Report Format
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

## Reasoning-level selection guidance

Use the smallest reasoning level that controls the implementation risk:

```text
Low — tiny localized edits, typo fixes, obvious one-file changes
Medium — small bounded implementation, clear UI fixes, simple tests, isolated refactors
High — Build Units, sublayers, multi-file features, state workflows, cross-component UX, meaningful test updates
Extended — full-layer implementation, architecture-sensitive work, repo-wide refactors, parallel-agent sequencing, stale-doc reconciliation, destructive schema/data-model changes, sensitive AI behavior
```

Do not include broad cleanup instructions unless cleanup is explicitly scoped and testable.
