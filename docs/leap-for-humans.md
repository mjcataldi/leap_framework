# LEAP for Humans

LEAP is for people who want to build software without letting confusion become code.

It is especially useful when AI coding agents are involved, because agents are very good at turning instructions into changes. They are not automatically good at knowing whether the instructions are complete, current, safe, or wise.

---

## The human problem LEAP solves

Humans often describe solutions from the outside:

```text
I want a dashboard.
I want an app that automates this.
I want AI to help users do that.
I want the platform to support this workflow.
```

Those statements may be directionally useful, but they are not yet implementation instructions.

The missing details matter:

```text
Who uses it?
What do they do today?
What is painful?
What is the smallest useful version?
What should stay manual for now?
What must never happen?
What data is sensitive?
What already exists in the codebase?
What does success look like?
```

LEAP helps uncover those missing details before implementation begins.

---

## Questions are the source of answers

LEAP uses questions because good questions expose the difference between:

```text
what someone imagines
```

and

```text
what the system must actually do
```

A good LEAP question is not random. It should clarify the next blocker.

Examples:

```text
Who is the first user?
What do they do today without this feature?
What is the first moment where this becomes useful?
What should the system refuse to do?
What is manual for now?
What would make this not worth building?
What part of the repo already handles this?
What would break if this changed?
```

---

## The Ideation Loop

LEAP's ideation loop is:

```text
Intent → Questions → Evidence labels → Assumptions → Pressure test → Revised intent → Gate decision
```

This loop continues while the next step is unsafe.

The goal is not endless discussion. The goal is to reach the next safe gate.

---

## Evidence labels

LEAP separates what is known from what is guessed.

```text
Known: confirmed by the user, repo, tests, or current docs
Assumed: plausible but not confirmed
Unknown: missing
Contested: sources conflict
Needs Decision: a human must choose
Deprecated: used to be true, but no longer governs
```

This matters because a polished assumption is still an assumption.

---

## Readiness gates

LEAP uses gates instead of fake precision scores.

```text
C0 Blocked: only ask questions
C1 Discovery Ready: enough to explore
C2 Concept Ready: enough to draft the concept
C3 Pressure-Test Ready: enough to challenge the idea
C4 Layer-Planning Ready: enough to plan the work
C5 Coding-Prompt Ready: enough to hand off to a coding agent
```

The important rule:

```text
A high confidence feeling does not override a hard blocker.
```

---

## What counts as a hard blocker?

Implementation planning should stop when any of these are missing:

```text
- primary user
- concrete problem
- current workflow or workaround
- MVP boundary
- concrete non-goals
- sensitive-data/risk profile when applicable
- source truth for existing projects
- repo reality for existing repos
- verification path
- human approval for risky decisions
- execution profile for the coding agent
```

---

## LEAP should feel practical

LEAP is not supposed to make small work heavy.

Use the smallest version of LEAP that controls the risk.

For a tiny fix, a short LEAP brief may be enough.

For a major feature, use Phase 0 and Recon.

For a whole layer, use full LEAP.

For multiple agents or sensitive areas, use full LEAP plus explicit ownership and stop conditions.

---

## The human-friendly summary

```text
Decide what problem matters.
Check what is already true.
Separate facts from guesses.
Make the work small enough to verify.
Tell the agent what not to touch.
Tell the agent when to stop.
Then build only the bounded task.
```