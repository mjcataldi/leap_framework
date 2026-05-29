<!--
LEAP_DOC_METADATA:
  audience: maintainer, agent
  doc_type: release-governance
  authority: canonical-for-agent-pack
  applies_to: leap-framework-repo
END_LEAP_DOC_METADATA
-->

# LEAP AGENTS.md Versioning

LEAP AGENTS.md templates are distributed as a versioned **LEAP Agent Pack**.

The Agent Pack is the release unit for reusable AGENTS.md template assets. It is separate from the broader LEAP framework release stream because downstream projects copy these templates into their own repositories and may keep project-specific edits for a long time.

## Current Agent Pack

- Agent Pack version: `0.1.0`
- Release tag: `leap-agent-pack-v0.1.0`
- Channel: `stable`
- Manifest: `templates/leap-agent-pack-manifest.json`
- Update policy: notify only

The first release tag should be created after the Agent Pack manifest and template metadata are committed. Until that tag exists, release provenance is documented but not yet tag-verifiable.

## Template Metadata

Each distributable AGENTS.md template should include a small machine-readable metadata block near the top of the file.

```md
<!--
LEAP_AGENT_TEMPLATE:
  schema_version: 1
  template_id: leap-master-repo-agents
  template_role: combined
  agent_pack_version: 0.1.0
  release_tag: leap-agent-pack-v0.1.0
  template_channel: stable
  source_repo: https://github.com/mjcataldi/leap_framework
  upstream_repo: https://github.com/mjcataldi/leap_framework
  source_path: templates/leap-repo-AGENTS-file-complete/AGENTS.md
  update_policy: notify
  managed_section_version: 1
  minimum_supported_leap_version: current
END_LEAP_AGENT_TEMPLATE
-->
```

The Markdown metadata identifies the installed template lineage. The manifest is the source of truth for release commit, checksums, and migration notes.

## Template IDs

| Template ID | Role | Canonical path |
| --- | --- | --- |
| `leap-global-agents` | Global user or machine-level guidance | `templates/leap-global-AGENTS-file/AGENTS.md` |
| `leap-repo-agents` | Repository-level project guidance | `templates/leap-repo-AGENTS-file/AGENTS.md` |
| `leap-master-repo-agents` | Combined local-trial template | `templates/leap-repo-AGENTS-file-complete/AGENTS.md` |

Use the plural filename `AGENTS.md`. A singular `AGENT.md` file is not a LEAP template name.

## Managed Sections

AGENTS.md files should separate LEAP-managed content from downstream project and local content.

```md
<!-- LEAP_MANAGED_SECTION_BEGIN -->
Core LEAP-managed instructions.
<!-- LEAP_MANAGED_SECTION_END -->

<!-- LEAP_PROJECT_SECTION_BEGIN -->
Project-specific repository guidance.
<!-- LEAP_PROJECT_SECTION_END -->

<!-- LEAP_LOCAL_OVERRIDES_BEGIN -->
Local team or developer-specific notes.
<!-- LEAP_LOCAL_OVERRIDES_END -->
```

The combined local-trial template also keeps the older `LEAP_MASTER_GLOBAL_SECTION_*` and `LEAP_MASTER_REPO_SECTION_*` markers as compatibility aliases. Do not remove those markers in Agent Pack `0.1.x`.

The global template may omit the project section because project-specific guidance belongs in repository-level AGENTS.md files.

## Update Policy

Agent Pack updates are notify/manual-merge only.

- The managed section may be updated only after user approval.
- The project section must be preserved by default.
- The local overrides section must never be overwritten by LEAP updates.
- If managed content differs from the manifest checksum, treat it as local managed changes and require manual review.

## Release Tags

LEAP should use two tag streams:

- Framework tags: `leap-vX.Y.Z`
- Agent Pack tags: `leap-agent-pack-vX.Y.Z`

Agent Pack semantic versioning:

- PATCH: wording fixes, link fixes, non-behavioral doc edits, or manifest checksum correction.
- MINOR: backward-compatible metadata fields, new optional sections, new templates, or improved update guidance.
- MAJOR: marker changes requiring migration, instruction-priority changes, removal of compatibility markers, or breaking metadata schema changes.

## Manifest

The Agent Pack manifest is an inspectable JSON source of truth for template paths, checksums, release metadata, migration notes, and update policy.

Checksums are calculated from UTF-8 text after normalizing CRLF line endings to LF. This keeps update detection stable across operating systems.

Use `templates/leap-agent-pack-manifest.json` for the current pack. Future release snapshots may be added later if the repository needs archived JSON manifests per release.
