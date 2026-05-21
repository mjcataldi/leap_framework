# LEAP Phase 0 — Standard Operational Prompt — v1.5

Run LEAP Phase 0 Inception.

You are operating under LEAP v1.5.

The purpose of this pass is to determine whether the idea is clear, useful, safe, and bounded enough to proceed to Recon. It is not an implementation prompt.

## Required LEAP v1.5 behavior

You must:

1. preserve the user's original idea wording
2. choose or recommend Phase 0 mode: Lite, Standard, or Pro
3. ask only the questions needed to make the next safe gate decision
4. separate Known, Assumed, Unknown, Contested, and Needs Decision items
5. identify the target user, problem, current workflow, pain, product thesis, MVP boundary, non-goals, risks, and success criteria
6. pressure test whether software is needed at all
7. consider simpler alternatives such as manual workflow, spreadsheet, checklist, template, service, process change, integration, script, or no-code automation
8. treat clarity scoring as a planning signal, not an objective measurement
9. block implementation planning when hard blockers remain
10. end with a gate decision

## Gate decisions

Use one of these decisions:

```text
Proceed to Recon
Pressure Test Further
Narrow MVP First
Needs Human Decision
Do Not Build Yet
```

## Required output

```text
# LEAP Phase 0 Inception — <Project Name or Working Title>

## 1. Phase 0 Mode
## 2. Idea Intake Summary
## 3. Current Understanding
## 4. Evidence Labels
### Known
### Assumed
### Unknown
### Contested
### Needs Decision
## 5. Socratic Discovery Questions, if needed
## 6. Clarity Assessment
## 7. Pressure-Test Findings
## 8. MVP Boundary Draft
## 9. Explicit Non-Goals
## 10. Risks and Constraints
## 11. Starter Documentation Bootstrap Recommendation
## 12. Source-of-Truth Recommendation
## 13. Human Checkpoints Required
## 14. Gate Decision
## 15. Next Questions or Approval Request
```

Do not generate Recon, Build Units, architecture, implementation strategy, or coding-agent prompts unless the gate decision allows it and the user explicitly approves moving forward.
