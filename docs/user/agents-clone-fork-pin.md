# LEAP AGENTS.md Clone, Fork, and Pin Guide

This guide explains how users can adopt LEAP AGENTS.md templates from the canonical repository, a pinned release, or an organization fork.

## Basic Download

Use this path when you want the current stable LEAP Agent Pack with minimal setup.

1. Choose the latest stable Agent Pack release tag, such as `leap-agent-pack-v0.1.0`.
2. Download the desired AGENTS.md template from `templates/`.
3. Place it in the target location.
4. Populate the project section from repository evidence.
5. Preserve metadata and section markers.

Future update checks should notify only. They should not overwrite the file.

## Clone and Pin

Use this path when you want repeatable installs from a known LEAP release.

```bash
git clone https://github.com/mjcataldi/leap_framework.git
cd leap_framework
git checkout leap-agent-pack-v0.1.0
```

Copy the selected template from that tag into the downstream location.

If the downstream project should not receive routine update recommendations, set:

```yaml
update_policy: pinned
```

Pinned files may still report newer Agent Pack releases as informational.

## Organization Fork

Use this path when an organization customizes LEAP templates.

Recommended metadata behavior:

- `upstream_repo` stays the canonical LEAP repository.
- `source_repo` points to the organization fork.
- Fork-specific Agent Pack tags should be used when templates diverge.
- Downstream project customization remains inside project/local sections.

This separates three layers:

1. Canonical upstream LEAP.
2. Organization fork template policy.
3. Downstream project or local customization.

## Fork Update Rule

When `source_repo` and `upstream_repo` differ, compare installed files against the fork first. Treat canonical upstream as advisory unless the user explicitly asks to migrate back to upstream.

Do not replace forked or downstream content automatically.
