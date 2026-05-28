# LEAP Phase 0 Inception Request Template

Use this template when starting a new software project, major new product direction, or feature whose user, problem, MVP boundary, risks, non-goals, or source of truth are unclear.

Phase 0 is for discovery, ideation, pressure testing, and baseline direction. It is not an implementation prompt.

```text
Run LEAP Phase 0 Inception using the current LEAP framework.

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

Ideation settings:
- Use the Ideation Loop to clarify vague intent before implementation planning.
- Ask the fewest questions needed to make the next safe gate decision.
- If hard blockers remain, ask another small question round instead of generating implementation plans.
- Questions should expose the gap between what I imagine and what the system must mechanically do.

Discovery settings:
- Use small Socratic rounds instead of a giant question dump.
- Do not generate an implementation plan yet.
- Do not generate a coding-agent prompt.
- Separate Known, Assumed, Unknown, Contested, Needs Decision, and Deprecated items.
- Use readiness gates C0–C5 instead of numeric clarity scores.
- Pressure test whether this should be an app at all.
- Consider simpler non-app alternatives such as manual workflow, spreadsheet, checklist, template, service, process change, integration, script, or no-code automation.
- Identify downstream agent/model/reasoning considerations only as planning signals, not as final execution settings.

Required Phase 0 workflow:
1. Intake classification
2. Raw idea preservation
3. Ideation Loop question pass
4. Socratic discovery
5. Evidence labeling and assumption ledger
6. No-build / alternative-solution review
7. MVP boundary definition
8. Concrete non-goals
9. Documentation bootstrap recommendation
10. Source-of-truth manifest recommendation
11. Downstream agent/model/reasoning considerations
12. Gate decision

Readiness gates:
- C0 Blocked: discovery questions only.
- C1 Discovery Ready: Phase 0 discovery note allowed.
- C2 Concept Ready: concept draft and assumption ledger allowed.
- C3 Pressure-Test Ready: no-build and MVP pressure test allowed.
- C4 Layer-Planning Ready: Recon/layer planning allowed after approval.
- C5 Coding-Prompt Ready: only after Recon/source truth/repo reality/scope/tests/stop conditions/execution profile are clear.

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
## 4. Ideation Loop Status
## 5. Evidence Labels
### Known
### Assumed
### Unknown
### Contested
### Needs Decision
### Deprecated
## 6. Socratic Discovery Questions, if needed
## 7. Readiness Gate
## 8. No-Build / Alternative-Solution Review
## 9. MVP Boundary Draft
## 10. Concrete Non-Goals
## 11. Risks and Constraints
## 12. Assumption Ledger
## 13. Starter Documentation Bootstrap Recommendation
## 14. Source-of-Truth Manifest Recommendation
## 15. Human Checkpoints Required
## 16. Downstream Agent / Model / Reasoning Considerations
## 17. Gate Decision / Next Step
```

## Downstream agent / model / reasoning considerations

Phase 0 may flag likely downstream execution posture, but the final agent, model, and reasoning level should be selected during Recon or Prompt generation after source truth and repo reality have been reviewed.

Use this section for early signals such as:

- likely LEAP process tier
- likely implementation risk
- expected scope scale
- sensitive data / AI behavior / architecture risk
- whether whole-layer work may require high or extended reasoning
