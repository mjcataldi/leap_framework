# LEAP Governance Pass — Standard Operational Prompt — v1.9

Run a LEAP v1.9 strategic reconciliation pass.

Use this prompt when the repo, docs, branch state, implementation reality, and public framework language may have drifted.

This is a governance pass. It is not an implementation prompt.

## Required behavior

You must:

1. identify the current LEAP version and governing docs
2. inspect README, changelog, glossary, templates, and prompt library docs
3. identify stale terminology, especially outdated framework expansion or tool-specific language where tool-agnostic language is intended
4. check whether new docs are discoverable from the README
5. check whether templates and operational prompts are aligned with current framework rules
6. check whether the Ideation Loop and question-loop rules are represented consistently
7. check whether source-of-truth, repo reality, stop conditions, and execution profile requirements are preserved
8. check whether risk taxonomy, destructive-change, and sensitive-area guidance are present where needed
9. classify any drift found
10. recommend document updates, but do not rewrite files unless explicitly asked

## Drift categories

Use these categories:

```text
Strategy drift — framework direction or audience changed
Documentation drift — docs disagree with each other
Implementation drift — code or prompt artifacts do not match methodology
Branch drift — active branches or PRs conflict
Prompt drift — prompts assume stale files, old decisions, missing agent/tool, missing model, or missing reasoning level
Terminology drift — old terms remain after framework language changed
Adoption drift — public onboarding docs do not match current framework behavior
```

## Required output

```text
# LEAP Governance — Strategic Reconciliation Pass

## 1. Current Version and Governing Sources
## 2. Documentation Discovery Review
## 3. Terminology Alignment Review
## 4. Ideation Loop / Question-Loop Review
## 5. Source-of-Truth and Repo-Reality Review
## 6. Template and Operational Prompt Review
## 7. Risk / Sensitive Area / Destructive-Change Review
## 8. Agent Execution Configuration Review
## 9. Drift Ledger Candidates
## 10. Recommended Updates
## 11. Human Decisions Required
## 12. Gate Decision / Next Step
```

## Gate decisions

Use one of these decisions:

```text
No Action Needed
Update Docs
Update Templates
Update Prompt Library
Reconcile Terminology
Needs Human Decision
Run Full Framework Recon
```
