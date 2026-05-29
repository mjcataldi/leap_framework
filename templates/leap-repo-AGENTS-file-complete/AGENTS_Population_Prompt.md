# LEAP Master Repo AGENTS.md Population Prompt

Use this prompt inside a code assistant after placing the combined master `AGENTS.md` file at the root of a repository.

Copy/paste the prompt below into the code assistant for that repository.

```text
You are helping adopt the LEAP Framework in this repository using a combined local-trial AGENTS.md file.

Target file:
- `AGENTS.md` at the repository root.

Important structure:
- The file contains a locked global LEAP section and an editable repository section.
- The locked global section is delimited by:
  - `<!-- LEAP_MASTER_GLOBAL_SECTION_START: DO NOT EDIT DURING REPO POPULATION -->`
  - `<!-- LEAP_MASTER_GLOBAL_SECTION_END -->`
- The editable repository section is delimited by:
  - `<!-- LEAP_MASTER_REPO_SECTION_START: EDIT THIS SECTION ONLY DURING REPO POPULATION -->`
  - `<!-- LEAP_MASTER_REPO_SECTION_END -->`

Goal:
Populate only the editable repository section so this repo has accurate project-specific LEAP operating context for LEAP Charter, LEAP Recon, LEAP Prompt, and LEAP LHS work.

Do not modify:
- The locked global section.
- The section boundary markers.
- Application code.
- Tests.
- Product docs.
- Configuration files.
- Any file other than the root `AGENTS.md`, unless I explicitly approve a separate change.

Before editing:
1. Inspect the existing repository structure.
2. Read the full root `AGENTS.md` file.
3. Treat the locked global section as read-only LEAP behavior.
4. Treat the editable repository section as the repo-specific AGENTS.md template to populate.
5. Start with docs/00_start_here.md when present.
6. Identify available source-of-truth documents, such as README files, docs, architecture notes, package files, build files, compose files, infrastructure files, test configuration, and CI files.
7. Classify docs as canonical, supporting, stale, conflicting, duplicate, archived, or unknown when evidence supports it.
8. Infer only what the repository evidence supports.
9. Do not invent commands, architecture, services, credentials, environments, workflows, business rules, or deployment assumptions.

Update only the editable repository section with:
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
- Security, secrets, and data-handling rules.
- Coding conventions and architectural constraints.
- Branch, worktree, PR, and commit conventions.
- Stop conditions requiring human review.

Rules:
- Preserve the combined master AGENTS.md structure.
- Preserve the locked global section exactly.
- Preserve all section boundary markers exactly.
- Keep the repo section concise, practical, and useful to a coding agent.
- Prefer verified repository evidence over assumptions.
- If something is unknown, mark it as `TBD` and include the exact question the project owner should answer.
- Do not perform product implementation work.
- Do not make risky runtime implementation changes during Charter work.
- Create LEAP Recon or LEAP Prompt recommendations instead of making risky implementation changes.
- Do not refactor application code.
- Do not create new strategic docs unless I explicitly approve that separately.
- Do not remove useful repo-template sections unless they clearly do not apply.

After editing, return a short completion report with:
1. Confirmation that the locked global section was not changed.
2. Sections populated in the editable repo section.
3. Evidence used.
4. Unknowns left as `TBD`.
5. Any contradictions or stale-doc risks found.
6. Any recommended LEAP Charter Brownfield reconciliation.
7. Recommended next LEAP Recon, LEAP Prompt, or LEAP LHS target.
```
