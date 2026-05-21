# LEAP Phase 0 Inception Request Template

Use this template when starting a new software project or a major new product direction.

Phase 0 is for discovery, pressure testing, and baseline direction. It is not an implementation prompt.

```text
Run LEAP Phase 0 Inception.

Initial idea:
- <Describe the app, tool, product, workflow, or automation you want to build. Rough is okay.>

Problem I think it solves:
- <Describe the problem, pain, inefficiency, or opportunity.>

Known context:
- Target users, if known:
- Current workflow or workaround, if known:
- Existing tools or competitors I know about:
- Business/personal motivation:
- Technical preferences or constraints:
- Existing repo? yes/no/link if available:
- Timeline or urgency:
- Sensitive data, compliance, or risk concerns:

Discovery settings:
- Ask Socratic questions in rounds of 5 to 8 questions.
- Do not generate an implementation plan yet.
- Do not generate a coding-agent prompt.
- Separate confirmed facts from assumptions.
- Pressure test whether this should be an app at all.

Required Phase 0 workflow:
1. Idea Intake
2. Socratic Discovery
3. Clarity Scoring
4. Market / Alternative Solution Pressure Test
5. MVP Boundary Definition
6. Strategic Plan Generation
7. Documentation Bootstrap Recommendation
8. Approval Gate to Begin Layer Planning

Clarity threshold:
- Below 67% clarity: continue discovery.
- 67% to 79% clarity: draft concept brief and continue pressure testing.
- 80% or higher clarity: implementation strategy and layer planning allowed after approval.
- Coding-agent prompts are forbidden until the approval gate is passed.

Return the Phase 0 output only.
If more information is needed, ask the next discovery round instead of producing implementation plans.
```

## Expected Phase 0 sections

```text
# LEAP Phase 0 Inception — <Project Name or Working Title>

## 1. Idea Intake Summary
## 2. Current Understanding
## 3. Confirmed Facts
## 4. Assumptions
## 5. Socratic Discovery Questions
## 6. Clarity Assessment
## 7. Pressure-Test Findings
## 8. MVP Boundary Draft
## 9. Explicit Non-Goals
## 10. Risks and Constraints
## 11. Starter Documentation Bootstrap
## 12. Source-of-Truth Recommendation
## 13. Recommendation
## 14. Approval Gate / Next Questions
```

## Notes

Use this template before LEAP Recon when the project direction is not yet documented.

If the user starts with a vague request like “I want to build a cool app,” stay in Phase 0 discovery mode.

Do not allow LEAP Recon, layer planning, or LEAP Prompt generation until Phase 0 has produced enough baseline clarity and the user explicitly approves moving forward.
