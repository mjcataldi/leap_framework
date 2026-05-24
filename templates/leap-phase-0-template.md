# LEAP Phase 0 Inception Request Template

Use this template when starting a new software project, major new product direction, or feature whose user, problem, MVP boundary, risks, non-goals, or source of truth are unclear.

Phase 0 is for discovery, pressure testing, and baseline direction. It is not an implementation prompt.

```text
Run LEAP Phase 0 Inception under LEAP v1.7.

Phase 0 mode:
- Lite / Standard / Pro / Small Project Mode / you recommend

Initial idea:
- <Describe the app, tool, product, workflow, automation, or change. Rough is okay.>

Problem I think it solves:
- <Describe the problem, pain, inefficiency, or opportunity.>

Known context:
- Target users, if known:
- Current workflow or workaround, if known:
- Existing tools, competitors, or simpler alternatives I know about:
- Business/personal motivation:
- Technical preferences or constraints:
- Existing repo? yes/no/link if available:
- Timeline or urgency:
- Sensitive data, compliance, AI-behavior, monetization, or risk concerns:

Discovery settings:
- Ask only the questions needed to make the next safe gate decision.
- Use small Socratic rounds instead of a giant question dump.
- Do not generate an implementation plan yet.
- Do not generate a coding-agent prompt.
- Separate Known, Assumed, Unknown, Contested, Needs Decision, and Deprecated items.
- Use readiness gates C0–C5 instead of numeric clarity scores.
- Pressure test whether this should be an app at all.
- Consider simpler non-app alternatives such as manual workflow, spreadsheet, checklist, template, service, process change, integration, script, or no-code automation.
- Identify downstream model/reasoning considerations only as planning signals, not as final Codex execution settings.

Required Phase 0 workflow:
1. Intake classification
2. Raw idea preservation
3. Socratic discovery
4. Evidence labeling and assumption ledger
5. No-build / alternative-solution review
6. MVP boundary definition
7. Concrete non-goals
8. Documentation bootstrap recommendation
9. Source-of-truth manifest recommendation
10. Downstream model/reasoning considerations
11. Gate decision

Readiness gates:
- C0 Blocked: discovery questions only.
- C1 Discovery Ready: Phase 0 discovery note allowed.
- C2 Concept Ready: concept draft and assumption ledger allowed.
- C3 Pressure-Test Ready: no-build and MVP pressure test allowed.
- C4 Layer-Planning Ready: Recon/layer planning allowed after approval.
- C5 Coding-Prompt Ready: only after Recon/source truth/repo reality/scope/tests/stop conditions/model/reasoning level are clear.

Gate decision options:
- Continue Discovery
- Draft Concept Brief
- Pressure Test Further
- Narrow MVP First
- Proceed to Recon
- Do Not Build Yet

Return the Phase 0 output only.
If more information is needed, ask the next discovery round instead of producing implementation plans.
```

## Expected Phase 0 sections

```text
# LEAP Phase 0 Inception — <Project Name or Working Title>

## 1. Mode and Intake Classification
## 2. Original User Wording
## 3. Current Understanding
## 4. Evidence Labels
### Known
### Assumed
### Unknown
### Contested
### Needs Decision
### Deprecated
## 5. Socratic Discovery Questions, if needed
## 6. Readiness Gate
## 7. No-Build / Alternative-Solution Review
## 8. MVP Boundary Draft
## 9. Concrete Non-Goals
## 10. Risks and Constraints
## 11. Assumption Ledger
## 12. Starter Documentation Bootstrap Recommendation
## 13. Source-of-Truth Manifest Recommendation
## 14. Human Checkpoints Required
## 15. Downstream Model / Reasoning Considerations
## 16. Gate Decision / Next Step
```

## Downstream model / reasoning considerations

Phase 0 may flag likely downstream execution posture, but the final Codex model and reasoning level should be selected during Recon or Prompt generation after source truth and repo reality have been reviewed.

Use this section for early signals such as:

- likely LEAP process tier
- likely implementation risk
- expected scope scale
- sensitive data / AI behavior / architecture risk
- whether whole-layer work may require high or extended reasoning
