# LEAP AGENTS.md Update Guide

Use this guide during LEAP Recon when checking whether a downstream `AGENTS.md` file is current.

Do not automatically overwrite a downstream AGENTS.md file. Report the status, explain the risk, and recommend a manual update path.

## Update Sources

Use these sources in order:

1. Local `AGENTS.md` metadata block.
2. Local managed/project/local section markers.
3. `templates/leap-agent-pack-manifest.json` from the selected LEAP source.
4. The selected release tag, when available.
5. Current LEAP docs and changelog for migration notes.

## Status Classification

| Status | Detection | Recon message |
| --- | --- | --- |
| Current | Metadata version/tag matches latest stable and managed checksum matches | No update needed. |
| Outdated | Older pack version, managed section unchanged | A newer Agent Pack exists; propose a manual managed-section update. |
| Outdated with local changes | Older version plus managed checksum mismatch | Do not overwrite; produce manual merge guidance. |
| Pinned | `update_policy: pinned` or pinned release tag | Respect the pin; report newer versions only as informational. |
| Unversioned LEAP-style file | LEAP markers/headings exist, metadata missing | Recommend metadata migration before update checks. |
| Non-LEAP AGENTS.md | No LEAP metadata or recognizable markers | Do not modify; ask whether the user wants LEAP adoption. |
| Missing AGENTS.md | No file at target | Offer install from the latest stable template. |
| Forked/custom source | `source_repo` differs from `upstream_repo` | Compare against the fork source first; upstream is advisory only. |
| Unknown or malformed metadata | Parse failure or missing required fields | Stop and ask for human review. |

## Manual Update Procedure

1. Identify the installed template ID and source repo.
2. Load the matching template from the selected Agent Pack release.
3. Compare only the LEAP-managed section first.
4. Preserve the project section by default.
5. Preserve the local overrides section always.
6. If the local managed section has changed, produce a merge note instead of replacing it.
7. Summarize the result in Validation/Handoff.

## Recon Output

A Recon pass should report:

- Installed template ID and Agent Pack version.
- Selected comparison source.
- Current status classification.
- Managed section checksum match or mismatch.
- Whether project/local sections are present.
- Recommended next step.

No Recon status authorizes automatic overwrite.
