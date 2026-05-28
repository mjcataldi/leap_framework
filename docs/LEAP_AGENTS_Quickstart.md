# LEAP AGENTS.md Quickstart

Use this starter guide to add LEAP to an AI coding-agent workflow with the least possible setup.

This guide assumes you want two instruction files:

1. A **global AGENTS.md** file that gives your coding agent the general LEAP operating model.
2. A **repo / project AGENTS.md** file that tells the agent how LEAP applies to one specific repository.

After those files are in place, run the repo-population prompt below once, then run a LEAP Recon prompt against the functionality you want to work on.

---

## LEAP reference links

Primary framework reference:

- [LEAP Framework — main branch](https://github.com/mjcataldi/leap_framework/tree/main)

Useful starting points:

- [Start Here](https://github.com/mjcataldi/leap_framework/blob/main/docs/00_start_here.md)
- [LEAP for Humans](https://github.com/mjcataldi/leap_framework/blob/main/docs/leap-for-humans.md)
- [Quick LEAP Brief](https://github.com/mjcataldi/leap_framework/blob/main/docs/quick-leap-brief.md)
- [Current LEAP Framework Document](https://github.com/mjcataldi/leap_framework/blob/main/docs/leap.md)
- [LEAP Recon Template](https://github.com/mjcataldi/leap_framework/blob/main/templates/leap-recon-template.md)
- [LEAP Prompt Template](https://github.com/mjcataldi/leap_framework/blob/main/templates/leap-prompt-template.md)

AGENTS.md Template links:

- [Global AGENTS.md template](https://github.com/mjcataldi/leap_framework/blob/main/templates/leap-global-AGENTS.md)
- [Repo AGENTS.md template](https://raw.githubusercontent.com/mjcataldi/leap_framework/main/templates/leap-repo-AGENTS.md)

---

## What the user does

There are three setup actions, then one first-use action.

### 1. Install the global AGENTS.md file

Download the global LEAP AGENTS.md template and place it in the global instruction location used by your coding agent.

Common locations:

| Agent / Tool                  | macOS / Linux                                         | Windows                                                           |
| ----------------------------- | ----------------------------------------------------- | ----------------------------------------------------------------- |
| Codex-style AGENTS.md         | `~/.codex/AGENTS.md`                                  | `%USERPROFILE%\.codex\AGENTS.md`                                  |
| Claude Code-style user memory | `~/.claude/CLAUDE.md` or tool-supported AGENTS import | `%USERPROFILE%\.claude\CLAUDE.md` or tool-supported AGENTS import |
| Other coding agents           | Use the tool's documented global instruction location | Use the tool's documented global instruction location             |

The global file should stay broad. It should explain LEAP behavior, source-of-truth discipline, Recon-first thinking, stop conditions, and safe agent handoff rules.

Do **not** put project-specific commands, architecture, secrets, or repo details in the global file.

---

### 2. Install the repo / project AGENTS.md file

Download the repo-level LEAP AGENTS.md template and place it at the root of the project repository:

```text
<repo-root>/AGENTS.md
```

This file starts as a template. It should be populated from the actual repository using the prompt in the next section.

The repo AGENTS.md file is where project-specific details belong, including:

- Project purpose
- Tech stack
- Local development commands
- Test, lint, typecheck, and build commands
- Source-of-truth docs
- Architecture notes
- Data model and API conventions
- Security and secrets rules
- Branch, worktree, and commit expectations
- LEAP-specific repo workflow rules

---

### 3. Run this prompt against the repo AGENTS.md file

Open the repository in your coding agent or code editor.

Attach, pin, or explicitly reference the repo-level `AGENTS.md` file.

Then run this prompt:

```text
You are helping adopt the LEAP Framework in this repository.

Target file:
- Update only the repo-level AGENTS.md file unless I explicitly approve another file change.

Framework reference:
- Use the LEAP Framework main branch as the stable reference:
  https://github.com/mjcataldi/leap_framework/tree/main

Goal:
Populate this repository's AGENTS.md file with project-specific operating context so future LEAP Recon and LEAP Prompt work can be accurate, bounded, and source-grounded.

Before editing:
1. Inspect the existing repository structure.
2. Read the existing repo-level AGENTS.md template.
3. Identify available source-of-truth documents, such as README files, docs, architecture notes, package files, build files, compose files, infrastructure files, test configuration, and CI files.
4. Infer only what the repository evidence supports.
5. Do not invent commands, architecture, services, credentials, environments, or workflows.

Populate the AGENTS.md file with:
- Project name and purpose
- Application type and current maturity
- Primary users or use cases, if the repo documents them
- Tech stack and major frameworks
- Repository layout
- Local setup commands
- Development commands
- Test, lint, typecheck, format, and build commands
- Database, storage, queue, cache, or external service dependencies
- Infrastructure and deployment notes
- Source-of-truth documents and their status if known
- Known stale, draft, archived, or conflicting documents if discoverable
- Security, secrets, and data-handling rules
- Coding conventions and architectural constraints
- Branch, worktree, PR, and commit conventions
- LEAP Recon expectations for this repo
- LEAP Prompt / implementation handoff expectations for this repo
- Stop conditions requiring human review

Rules:
- Preserve the intent of the LEAP template.
- Keep the file concise, practical, and useful to a coding agent.
- Prefer verified repository evidence over assumptions.
- If something is unknown, mark it as `TBD` and include the exact question the project owner should answer.
- Do not perform product implementation work.
- Do not refactor application code.
- Do not create new strategic docs unless I explicitly approve that separately.
- Do not remove useful template sections unless they clearly do not apply.

After editing:
Return a short completion report with:
1. Sections populated.
2. Evidence used.
3. Unknowns left as TBD.
4. Any contradictions or stale-doc risks found.
5. Recommended next LEAP Recon target.
```

The output of this step should be an updated repo-specific `AGENTS.md` file.

---

### 4. Run a LEAP Recon base prompt on the functionality

After the repo AGENTS.md file is populated, run a Recon pass before asking the coding agent to implement anything.

Use this base prompt:

```text
Run a LEAP Recon pass for the following functionality:

[DESCRIBE THE FEATURE, LAYER, BUGFIX, WORKFLOW, OR FUNCTIONAL AREA HERE]

Use these sources in order:
1. The repo-level AGENTS.md file.
2. The current repository state.
3. The LEAP Framework main branch:
   https://github.com/mjcataldi/leap_framework/tree/main
4. Any source-of-truth docs identified in AGENTS.md.

Recon rules:
- Do not implement code changes.
- Do not generate the final coding-agent implementation prompt yet.
- Inspect the repo before making recommendations.
- Verify what exists now before proposing work.
- Identify stale, missing, or conflicting docs.
- Identify cross-layer or cross-module impacts.
- Identify risks, assumptions, blockers, and human decision points.
- Separate known facts from recommendations.
- Keep scope bounded to the requested functionality.
- Recommend the smallest safe Build Units or LEAP LHS prompts.

Return the Recon report with:
1. Requested functionality summary.
2. Current repo reality.
3. Relevant source-of-truth docs.
4. Existing implementation map.
5. Gaps and conflicts.
6. Risks and edge cases.
7. Suggested Build Units / LHS breakdown.
8. Recommended agent execution configuration.
9. Stop conditions.
10. Questions that must be answered before implementation, if any.
11. Clear recommendation on whether this is ready for a LEAP Prompt.
```

Only after Recon is accepted should the user generate a final LEAP Prompt for implementation.

---

## Done state

The project is ready for normal LEAP use when:

- The global AGENTS.md or equivalent global instruction file is installed.
- The repo-level `AGENTS.md` file exists at the repository root.
- The repo-level `AGENTS.md` file has been populated from actual repo evidence.
- Unknowns are marked as `TBD`, not guessed.
- A LEAP Recon pass has been run for the first functionality target.
- The next implementation task has a bounded scope, non-goals, validation expectations, and stop conditions.

---

## Short rule

```text
Global AGENTS.md teaches the agent how to think with LEAP.
Repo AGENTS.md teaches the agent how LEAP applies to this project.
Recon verifies reality before implementation.
Prompt only after Recon.
```
