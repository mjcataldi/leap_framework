# LEAP Prompt Request Template

Use this template after LEAP Recon has been completed and the user has answered questions or approved safe defaults.

Do not use this template for vague app ideas or unreconciled brownfield docs. New projects must pass LEAP Charter and Recon before LEAP Prompt generation unless the baseline is explicitly not applicable.

```text
Generate the LEAP Prompt for <Target Layer or Task> using the current LEAP framework.

Use the LEAP Recon findings above.
Use my answers/defaults below:
- <answer/default 1>
- <answer/default 2>

Preflight status:
- LEAP Charter complete or not applicable:
- Prompt type selected:
- LHS decision gate completed:
- Ideation Loop complete or remaining questions resolved:
- Source-of-truth manifest complete:
- Recon approved:
- Repo reality checked:
- Branch/worktree/PR drift reviewed:
- Human approvals granted:
- Agent/tool selected or recommended:
- Model selected or recommended:
- Reasoning level selected or recommended:

Source-of-truth instructions:
Use these sources:
- <canonical / active source paths>

Do not use these sources:
- <draft / stale / archived / superseded source paths>

Archived docs are historical unless a canonical document explicitly references them.

Agent execution configuration:
- Prompt Type: Standard LEAP Prompt / LHS Prompt / Fix Prompt / Refactor Prompt / Validation Prompt / other clearly named type
- LHS Decision: Use LHS / Do not use LHS
- Agent / Tool: <Codex / Claude Code / Cursor / other>
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
- Destructive changes allowed: yes/no/allowed only in specified areas
- Rollback/data preservation requirements:

Required gate:
- Confirm LEAP Charter / source-of-truth review is complete.
- Confirm repo reality has been checked when repo access exists.
- Confirm scope, non-goals, verification, stop conditions, and execution profile are defined.
- Confirm whether implementation gravity warrants LHS.
- Confirm the final prompt includes an explicit agent/tool, model, and reasoning level.
- If baseline direction, MVP boundary, source truth, Recon approval, implementation scope, verification plan, stop conditions, agent/tool, model, or reasoning level are missing, stop and explain what must be completed first.

Create the final implementation prompt as a canvas/textdoc artifact if supported by the working environment.
Do not include extra analysis inside the prompt unless it is operationally necessary for the coding agent.
```

## Expected LEAP Prompt sections

```text
# <Solution Name> — LEAP Prompt — <Target Layer or Task>

## 1. Prompt Type and LHS Decision
## 2. Agent Execution Configuration
## 3. Objective
## 4. Current Repo Reality
## 5. Source-of-Truth Instructions
## 6. Scope
## 7. Non-Goals
## 8. Constraints
## 9. Implementation Sequence
## 10. Verification
## 11. Stop Conditions
## 12. Branch / Worktree / Commit Instructions
## 13. Source-of-Truth Update Policy
## 14. Completion Report Format
```

## Required Agent Execution Configuration

Every LEAP Prompt must include this section near the top:

```text
## 1. Prompt Type and LHS Decision

- Prompt type: <Standard LEAP Prompt / LHS Prompt / Fix Prompt / Refactor Prompt / Validation Prompt / other clearly named type>
- LHS decision: <Use LHS / Do not use LHS>
- Rationale:

## 2. Agent Execution Configuration

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
```

If the agent/tool, model, or reasoning level is unknown, recommend one explicitly instead of leaving the field blank.

Use LHS only when the work needs staged implementation, commit boundaries, tests, docs, compatibility checks, rollback awareness, or multi-area coordination.

## Required stop conditions

Every LEAP Prompt should instruct the coding agent to stop and report instead of guessing when:

- required files or source documents are missing
- docs conflict with repo reality
- existing implementation contradicts the prompt
- implementation would violate explicit non-goals
- scope requires architecture not approved
- task requires touching forbidden files
- implementation requires a new dependency, migration, auth/permission change, billing change, AI behavior change, or sensitive-data handling not approved
- destructive changes are required but not explicitly authorized
- branch/worktree/PR drift creates unclear ownership
- required tests or verification paths are unavailable or unclear
- acceptance criteria are impossible as written
- requested agent/tool is unavailable and no approved fallback is provided
- requested model is unavailable and no approved fallback is provided
- requested reasoning level is unavailable and no approved fallback is provided
- archived docs appear to be treated as current source truth
