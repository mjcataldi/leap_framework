# LEAP Prompt Request Template

Use this template after LEAP Recon has been completed and the user has answered questions or approved safe defaults.

Do not use this template for vague app ideas. New projects must pass Phase 0 Inception and Recon before LEAP Prompt generation.

```text
Generate the LEAP Prompt for <Target Layer or Task> under LEAP v1.7.

Use the LEAP Recon findings above.
Use my answers/defaults below:
- <answer/default 1>
- <answer/default 2>

Preflight status:
- Phase 0 complete or not applicable:
- Source-of-truth manifest complete:
- Recon approved:
- Repo reality checked:
- Branch/worktree/PR drift reviewed:
- Human approvals granted:
- Codex model selected or recommended:
- Codex reasoning level selected or recommended:

Source-of-truth instructions:
Use these sources:
- <canonical / active source paths>

Do not use these sources:
- <draft / stale / archived / superseded source paths>

Codex execution configuration:
- Model: <exact model name or recommended default>
- Reasoning Level: <low / medium / high / extended>
- Execution Mode: <recon-only / plan-first / implement-directly / implement-with-brief-plan>
- Scope Scale: <small task / Build Unit / sublayer / entire layer / repo-wide maintenance>
- Repository:
- Branch / Worktree:
- Permissions:
- Validation:
- Commit Guidance:

Implementation target:
- Objective:
- User-visible outcome:
- Definition of done:
- In scope:
- Out of scope:
- Non-goals:
- Files/areas to inspect:
- Files/areas not to touch:

Required gate:
- Confirm source-of-truth review is complete.
- Confirm repo reality has been checked when repo access exists.
- Confirm scope, non-goals, verification, and stop conditions are defined.
- Confirm the final prompt includes an explicit model and reasoning level.
- If baseline direction, MVP boundary, source truth, Recon approval, implementation scope, verification plan, stop conditions, model, or reasoning level are missing, stop and explain what must be completed first.

Create the final implementation prompt as a canvas/textdoc artifact.
Do not include extra analysis inside the prompt unless it is operationally necessary for the coding agent.
```

## Expected LEAP Prompt sections

```text
# <Solution Name> — LEAP Prompt — <Target Layer or Task>

## 1. Codex Execution Configuration
## 2. Objective
## 3. Current Repo Reality
## 4. Source-of-Truth Instructions
## 5. Scope
## 6. Non-Goals
## 7. Constraints
## 8. Implementation Sequence
## 9. Verification
## 10. Stop Conditions
## 11. Branch / Worktree / Commit Instructions
## 12. Source-of-Truth Update Policy
## 13. Completion Report Format
```

## Required Codex Execution Configuration

Every LEAP Prompt must include this section near the top:

```text
## 1. Codex Execution Configuration

| Field | Value |
|---|---|
| Model | <exact model name or approved project default> |
| Reasoning Level | <low / medium / high / extended / project-approved enum> |
| Execution Mode | <recon-only / plan-first / implement-directly / implement-with-brief-plan> |
| Scope Scale | <small task / Build Unit / sublayer / entire layer / repo-wide maintenance> |
| Repository | <owner/repo or local repo name> |
| Branch / Worktree | <target branch/worktree> |
| Permissions | <allowed modifications> |
| Validation | <tests/lint/typecheck/build/manual checks> |
| Commit Guidance | <commit message convention or none> |
```

If the model or reasoning level is unknown, recommend one explicitly instead of leaving the field blank.

## Required stop conditions

Every LEAP Prompt should instruct the coding agent to stop and report instead of guessing when:

- required files or source documents are missing
- docs conflict with repo reality
- existing implementation contradicts the prompt
- implementation would violate explicit non-goals
- scope requires architecture not approved
- task requires touching forbidden files
- implementation requires a new dependency, migration, auth/permission change, billing change, AI behavior change, or sensitive-data handling not approved
- branch/worktree/PR drift creates unclear ownership
- required tests or verification paths are unavailable or unclear
- acceptance criteria are impossible as written
- requested model is unavailable and no approved fallback is provided
- requested reasoning level is unavailable and no approved fallback is provided
