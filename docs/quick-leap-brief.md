# Quick LEAP Brief

Use this when the work is small enough that full Phase 0 and Recon would be heavier than the task, but you still want a safe AI coding-agent handoff.

The Quick LEAP Brief is the smallest useful LEAP workflow.

---

## When to use it

Use this for:

```text
- small UI fixes
- localized backend changes
- one Build Unit
- simple tests
- narrow refactors
- documentation updates
- low-risk behavior changes
```

Do not use this when the work involves:

```text
- unclear product direction
- major data model changes
- auth/session/permission changes
- billing or credit logic
- privacy/security-sensitive data
- destructive migrations
- multiple branches or agents
- stale docs or unclear source truth
```

Escalate those to Phase 0 or Recon.

---

## Copy-ready brief

```text
# Quick LEAP Brief — <Task Name>

## 1. Goal
- <What should change?>

## 2. Current State
- <What exists now?>
- <What files/docs are source truth?>

## 3. Scope
In scope:
- <Allowed changes>

Out of scope:
- <Disallowed changes>

Files/areas to inspect:
- <Files/directories/components>

Files/areas not to touch:
- <Forbidden files/directories/components>

## 4. Constraints
- Follow existing patterns.
- Do not introduce new dependencies unless explicitly approved.
- Do not change API/schema/auth/billing/AI behavior unless explicitly approved.
- Preserve backwards compatibility unless explicitly told otherwise.

## 5. Verification
Run/check:
- <tests/lint/typecheck/build/manual checks>

Done means:
- <observable acceptance criteria>

## 6. Stop Conditions
Stop and ask if:
- required files are missing
- existing code contradicts this brief
- the task requires touching forbidden files
- the task requires new dependencies, migrations, auth changes, billing changes, or sensitive-data handling
- verification cannot be run or is unclear
- acceptance criteria are impossible as written

## 7. Agent Execution Configuration
- Agent / Tool: <Codex / Claude Code / Cursor / other>
- Model: <exact model or recommendation>
- Reasoning Level: <low / medium / high / extended>
- Execution Mode: <implement-directly / implement-with-brief-plan>
- Scope Scale: <small task / Build Unit>
- Repository:
- Branch / Worktree:
- Permissions:
- Validation:
- Commit Guidance:
```

---

## Default settings

If the task is small and low risk:

```text
Reasoning Level: Medium
Execution Mode: implement-directly
Scope Scale: small task
```

If the task touches several files or a coherent Build Unit:

```text
Reasoning Level: High
Execution Mode: implement-with-brief-plan
Scope Scale: Build Unit
```

---

## Escalation rule

```text
If the brief starts needing product discovery, architecture decisions, source-truth reconciliation, or branch-drift review, stop using the Quick LEAP Brief and run Phase 0 or Recon.
```