# LEAP Version

LEAP release versions should be managed by Git tags. If tags are missing, use Git history, `CHANGELOG.md`, and `docs/maintainer/release-history.md` as the available release record until tags are created.

LEAP AGENTS.md templates are released from the separate LEAP Agent Pack repository because downstream repositories copy and customize those files.

Current framework baseline:

```text
Version: 0.1.9
Release tag: leap-v0.1.9
Status: historical baseline; current branch changes remain unreleased
```

Current Agent Pack:

```text
Version: 0.1.0
Release tag: leap-agent-pack-v0.1.0
Repository: https://github.com/mjcataldi/leap_agent_pack
Manifest: manifests/latest.json
Update policy: notify
```

The first Agent Pack release tag should be created in the Agent Pack repository after its manifest and template metadata are committed.

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
docs/maintainer/release-history.md
Git tags, when present
Git commit history
```

Active framework and prompt files should not use versioned filenames.

Agent Pack template files live in `https://github.com/mjcataldi/leap_agent_pack`. Version identity lives in the Agent Pack metadata block and manifests, not in LEAP Framework filenames.
