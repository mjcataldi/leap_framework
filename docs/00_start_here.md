# Start Here: LEAP in Plain English

**LEAP — Layered Execution & Alignment Protocol** helps you avoid asking an AI coding agent to build from confusion.

AI coding agents can move quickly. That is useful only when the idea is clear, the source documents are current, the repo state is understood, and the task is small enough to verify.

LEAP helps with the messy middle between:

```text
"I have an idea"
```

and:

```text
"Here is a bounded implementation task an AI coding agent can safely run."
```

---

## The simple version

LEAP asks:

```text
What are we trying to build?
Who is it for?
What problem does it solve?
What already exists?
What should not be built?
What could go wrong?
What should the agent stop and ask about?
How do we prove the work is done?
```

If those answers are unclear, LEAP keeps asking focused questions before creating an implementation prompt.

Questions are not a delay. Questions are how LEAP turns a vague idea into a buildable system.

---

## Why LEAP exists

People often start with a picture in their head of what a solution should be.

That picture can feel complete, but the missing pieces are often connected by emotion, urgency, assumptions, or taste rather than logic and mechanisms.

A coding agent cannot safely build from that.

LEAP helps expose the gaps before implementation begins.

---

## The three LEAP stages

### 1. Phase 0 Inception

Use Phase 0 when the idea is still fuzzy.

Phase 0 clarifies:

```text
- the user
- the problem
- the current workaround
- the smallest useful outcome
- non-goals
- risks
- simpler alternatives
- whether this should be built at all
```

### 2. LEAP Recon

Use Recon when there is already a project, repo, layer, or plan.

Recon checks:

```text
- what the docs say
- what the repo actually does
- what is stale
- what already exists
- what branches or PRs may conflict
- what shared contracts may be affected
- what Build Units should be sequenced
```

### 3. LEAP Prompt

Use LEAP Prompt only after Phase 0 and/or Recon are clear enough.

A LEAP Prompt tells the coding agent:

```text
- the objective
- what is in scope
- what is not in scope
- what files to inspect
- what files not to touch
- what constraints apply
- what tests/checks to run
- when to stop instead of guessing
- what execution profile to use
```

---

## The Ideation Loop

LEAP does not assume the first version of an idea is ready to build.

It loops:

```text
Idea → Questions → Assumptions → Pressure test → Better idea → Gate decision
```

The loop continues until the next safe step is clear.

Use the loop when:

```text
- the problem is vague
- the user is unclear
- the workflow is not known
- the MVP is too broad
- non-goals are missing
- risks are hand-waved
- source truth is missing
- the agent would need to guess
```

---

## The shortest useful LEAP checklist

Before giving work to an AI coding agent, answer:

```text
1. What is the goal?
2. What is the current state?
3. What is in scope?
4. What is out of scope?
5. What files/docs are source truth?
6. What should the agent not touch?
7. What tests/checks prove success?
8. When should the agent stop and ask?
9. What model/reasoning/execution profile should be used?
```

If you cannot answer these, run Phase 0 or Recon first.

---

## When to use full LEAP

Use full LEAP for:

```text
- new products
- major features
- AI-heavy workflows
- multi-file changes
- existing repos with stale docs
- data model changes
- API changes
- auth/session/permission changes
- billing or credit logic
- privacy/security-sensitive features
- multiple people or agents working in parallel
```

Use Small Project Mode for:

```text
- tiny fixes
- obvious one-file changes
- text edits
- low-risk UI cleanup
- tasks with clear acceptance criteria
```

---

## The LEAP rule of thumb

```text
Ask until the idea becomes buildable.
Then stop asking and build only the bounded task.
```

LEAP should reduce chaos, not create ceremony.

If the framework is slower than the low-risk work itself, use a lighter mode.