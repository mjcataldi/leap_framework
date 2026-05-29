# LEAP Version

LEAP release versions should be managed by Git tags. If tags are missing, use Git history, `CHANGELOG.md`, and `docs/release-history.md` as the available release record until tags are created.

LEAP AGENTS.md templates are released as a separate Agent Pack because downstream repositories copy and customize those files.

Current Agent Pack:

```text
Version: 0.1.0
Release tag: leap-agent-pack-v0.1.0
Manifest: templates/leap-agent-pack-manifest.json
Update policy: notify
```

The first Agent Pack release tag should be created after the manifest and template metadata are committed.

Canonical framework document:

```text
docs/leap.md
```

Canonical Charter reference:

```text
docs/leap-charter.md
```

Release history is preserved through:

```text
CHANGELOG.md
docs/release-history.md
Git tags, when present
Git commit history
```

Active framework and prompt files should not use versioned filenames.

Agent Pack template files also keep stable paths. Version identity lives in the metadata block and manifest, not in the filename.
