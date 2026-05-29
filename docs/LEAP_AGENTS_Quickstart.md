# LEAP AGENTS.md Quickstart

Use this starter guide to add LEAP to a local repository with the least possible friction.

This Quickstart defaults to the **Master Repo AGENTS.md local-trial method**. This method uses one repository-root `AGENTS.md` file that contains both:

1. A locked global LEAP operating section.
2. An editable repository-specific section.

This lets users test LEAP inside one local repository before installing anything system-wide.

For users who prefer the traditional two-file approach, see:

- [Separate Global + Repo AGENTS.md Method](/docs/LEAP_AGENTS_Separate_Global_and_Repo_Method.md)

## User Actions

There are two setup actions, then one first-use action.

### 1. Install the Master Repo AGENTS.md file

Download the [Master Repo AGENTS.md local-trial template](/templates/leap-repo-AGENTS-file-complete/AGENTS.md) and place it at the root of the project repository:

```text
<repo-root>/AGENTS.md
```

This file intentionally combines two scopes:

1. **Locked Global Section** - reusable LEAP operating behavior.
2. **Editable Repository Section** - project-specific AGENTS.md content that should be populated from the current repository.

This is the recommended starter method because it lets the user test LEAP in one repository without changing global system behavior.

### 2. Populate the editable repo section

Open the repository in the user's coding agent or code editor.

Then use the [Master Repo AGENTS.md population prompt](/templates/leap-repo-AGENTS-file-complete/AGENTS_Population_Prompt.md).

The prompt instructs the code assistant to:

- Preserve the locked global section.
- Preserve the section boundary markers.
- Update only the editable repository section.
- Start with `docs/00_start_here.md` when present.
- Populate project-specific values from actual repository evidence.
- Identify canonical, stale, archived, duplicate, or conflicting docs when discoverable.
- Mark unknowns as `TBD` instead of guessing.

The output of this step should be a populated repository-root `AGENTS.md` file.

### 3. Run LEAP Charter or Recon

If project direction, source truth, docs, roadmap, or implementation posture are unclear, run LEAP Charter first:

```text
Run LEAP Charter for this repository.
Use Brownfield Mode if existing docs need reconciliation.
```

If the project baseline is already clear, run a Recon pass before asking the coding agent to implement anything:

```text
Run LEAP Recon for the following functionality:

[DESCRIBE THE FEATURE, LAYER, BUGFIX, WORKFLOW, OR FUNCTIONAL AREA HERE]
```

The Master Repo AGENTS.md file provides the operating rules for Charter and Recon. The user should not need to paste the full standard prompts when using standard AGENTS.md behavior.

Only after Recon is accepted should the user generate a final LEAP Prompt for implementation.

## Done state

The project is ready for normal LEAP use when:

- The Master Repo `AGENTS.md` file exists at the repository root.
- The locked global section is still intact.
- The editable repository section has been populated from actual repo evidence.
- Unknowns are marked as `TBD`, not guessed.
- Canonical docs and archived/stale docs are identified when discoverable.
- LEAP Charter has reconciled project direction and docs if needed.
- A LEAP Recon pass has been run for the first functionality target.
- The next implementation task has bounded scope, non-goals, validation expectations, and stop conditions.

## Short rule

```text
Master Repo AGENTS.md lets users test LEAP locally before installing global instructions.
The locked global section teaches the agent how to think with LEAP.
The editable repo section teaches the agent how LEAP applies to this project.
Charter establishes or reconciles source truth.
Recon verifies reality before implementation.
Prompt only after Recon.
Validation/Handoff closes the loop.
```

## LEAP reference links

Primary framework reference:

- [LEAP Framework - main branch](/)

Useful starting points:

- [Start Here](/docs/00_start_here.md)
- [LEAP Charter](/docs/leap-charter.md)
- [LEAP for Humans](/docs/leap-for-humans.md)
- [Quick LEAP Brief](/docs/quick-leap-brief.md)
- [Current LEAP Framework Document](/docs/leap.md)
- [LEAP Charter Template](/templates/leap-charter-template.md)
- [LEAP Recon Template](/templates/leap-recon-template.md)
- [LEAP Prompt Template](/templates/leap-prompt-template.md)

AGENTS.md local-trial template links:

- [Master Repo AGENTS.md local-trial template](/templates/leap-repo-AGENTS-file-complete/AGENTS.md)
- [Master Repo AGENTS.md population prompt](/templates/leap-repo-AGENTS-file-complete/AGENTS_Population_Prompt.md)

Optional advanced setup:

- [Separate Global + Repo AGENTS.md Method](/docs/LEAP_AGENTS_Separate_Global_and_Repo_Method.md)
