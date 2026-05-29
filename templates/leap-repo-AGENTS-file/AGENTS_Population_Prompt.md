# Repository AGENTS.md Population Prompt

Repository path:

```text
templates/leap-repo-AGENTS-file/AGENTS_Population_Prompt.md
```

Use this prompt when using the **separate global AGENTS.md + repo AGENTS.md method**.

This prompt assumes:

1. The global LEAP `AGENTS.md` file has already been installed in the coding agent's global instruction location.
2. The repository-level LEAP `AGENTS.md` template has already been placed at the root of the target repository.
3. The code assistant has access to the target repository and can inspect its files.

Copy/paste the prompt below into the code assistant for the target repository.

```text
You are helping adopt the LEAP Framework in this repository using a separate repository-level AGENTS.md file.

Target file:
- AGENTS.md at the repository root.

Framework reference:
- Use the LEAP Framework main branch as the stable reference:
  /

Goal:
Populate this repository's AGENTS.md file with project-specific operating context so future LEAP Charter, LEAP Recon, LEAP Prompt, and LEAP LHS work can be accurate, bounded, and source-grounded.

Scope:
- Update only the repository-level AGENTS.md file unless I explicitly approve another file change.
- Do not modify any global AGENTS.md file or system-wide instruction file.
- Do not perform product implementation work.

Before editing:
1. Inspect the existing repository structure.
2. Read the existing repository-level AGENTS.md template.
3. Start with docs/00_start_here.md when present.
4. Identify available source-of-truth documents, such as README files, docs, architecture notes, package files, build files, compose files, infrastructure files, test configuration, and CI files.
5. Classify docs as canonical, supporting, stale, conflicting, duplicate, archived, or unknown when evidence supports it.
6. Infer only what the repository evidence supports.
7. Do not invent commands, architecture, services, credentials, environments, workflows, business rules, or deployment assumptions.

Populate the AGENTS.md file with:
- Project name and purpose.
- Application type and current maturity, if discoverable.
- Primary users or use cases, if documented.
- Tech stack and major frameworks.
- Repository layout.
- Local setup commands.
- Development commands.
- Test, lint, typecheck, format, and build commands.
- Database, storage, queue, cache, or external service dependencies.
- Infrastructure and deployment notes.
- Source-of-truth documents and their status if known.
- Known stale, draft, archived, duplicate, or conflicting documents if discoverable.
- Guidance to start with docs/00_start_here.md when present.
- Guidance to treat canonical docs as source of truth.
- Guidance to treat archived docs as historical unless explicitly referenced by canonical docs.
- LEAP Charter expectations for this repo.
- LEAP Recon expectations for this repo.
- LEAP Prompt / implementation handoff expectations for this repo.
- LEAP LHS expectations if layered House Standard-style work is likely.
- Guidance that LEAP Prompt is the instruction artifact family.
- Guidance that LEAP LHS is used only when staged implementation is warranted by implementation gravity.
- Guidance not to treat LHS as a mandatory stage after every LEAP Prompt.
- Security, secrets, and data-handling rules.
- Coding conventions and architectural constraints.
- Branch, worktree, PR, and commit conventions.
- Stop conditions requiring human review.

Rules:
- Preserve the intent of the LEAP repository AGENTS.md template.
- Keep the file concise, practical, and useful to a coding agent.
- Prefer verified repository evidence over assumptions.
- If something is unknown, mark it as TBD and include the exact question the project owner should answer.
- Do not refactor application code.
- Do not make risky runtime implementation changes during Charter work.
- Create LEAP Recon or LEAP Prompt recommendations instead of making risky implementation changes.
- Do not create new strategic docs unless I explicitly approve that separately.
- Do not remove useful template sections unless they clearly do not apply.

After editing, return a short completion report with:
1. Sections populated.
2. Evidence used.
3. Unknowns left as TBD.
4. Any contradictions or stale-doc risks found.
5. Any recommended LEAP Charter Brownfield reconciliation.
6. Recommended next LEAP Recon, LEAP Prompt, or LEAP LHS target.
```
