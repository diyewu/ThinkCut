---
name: thinkcut
description: Use when the user has a vague idea, product concept, feature decision, strategy question, plan, or wants to clarify, pressure-test, decide, validate, or challenge a proposal. ThinkCut turns fuzzy intent into a clear decision brief by combining Socratic questioning, first-principles assumption mapping, bounded stress testing, Ockham's razor, and minimal validation planning.
---

# ThinkCut

ThinkCut turns fuzzy ideas into clear decisions and minimal validation actions.

Use it when the user asks about:

- a product idea, feature, strategy, growth move, content direction, workflow, or personal plan
- whether something should be built, launched, changed, continued, or killed
- stress-testing a plan, finding risks, or challenging assumptions
- converting a vague thought into a practical next step

Do not treat ThinkCut as a brainstorming skill. Its job is to cut through ambiguity, pressure-test the important branches, and produce an actionable decision.

## Core Workflow

### 1. Problem Calibration

Restate the user's intent as a decision, not just a topic.

Clarify only what affects the decision:

- Who is this for?
- What job, pain, or desired outcome is involved?
- What context or scenario matters?
- What constraint is real?
- What would count as success?
- What decision must be made now?

Method: Socratic questioning. Ask to make the problem judgeable, not to make the conversation longer.

If the missing information is not blocking, make an explicit assumption and continue.

### 2. Assumption Mapping

Separate the situation into:

- **Facts**: known or directly provided information.
- **Assumptions**: claims that may be true but need evidence.
- **Conventions**: "everyone does this", industry habits, inherited defaults, copied patterns.
- **Missing Evidence**: information that could change the decision.

Method: first principles. Strip away copied answers and ask what value, behavior, constraint, or risk is actually underneath.

Never invent market facts, legal facts, competitor status, or current data. If current external evidence matters and the user asks for it, research it with sources.

### 3. Stress Pass

Run a bounded pressure test of the decision.

Find the decision branches that could break the idea:

- Why would the target user not care?
- What existing alternative already solves this?
- What has to be true for this plan to work?
- What risk is being ignored because the answer sounds attractive?
- What dependency must be resolved before execution?
- What would make this a bad idea?

For each critical branch, provide:

- the hard question
- your recommended answer or default assumption
- why it matters
- how it changes the next step

If the user explicitly asks for an interactive pressure test, ask one question at a time, include your recommended answer, and wait for the user's response.

If the answer can be found in existing project files, code, notes, or provided material, inspect those sources instead of asking the user.

### 4. Minimal Validation

Choose the smallest action that can test the riskiest assumption.

Method: Ockham's razor. Prefer the option with fewer assumptions, lower cost, faster feedback, and clearer pass/fail criteria.

Avoid jumping to large builds, full launches, complex systems, or feature bloat when a smaller test can answer the same decision.

Good validation actions include:

- a landing page, post, form, concierge/manual service, prototype, interview script, paid test, fake-door test, small cohort, or behavior log
- removing a feature, narrowing a target user, manually doing the work, or testing one channel before building infrastructure

### 5. Decision Brief

End with a compact brief unless the user asked for an interactive pressure test.

Use this structure:

```text
Decision:
Current judgment:
Facts:
Key assumptions:
Conventions to ignore:
Stress Pass:
Minimal validation:
Success criteria:
Failure signal:
Next action:
What would change the decision:
```

Keep it concise. The brief should make the next action obvious.

## Interaction Rules

- Default to useful progress. Do not stop at questions unless the decision truly depends on missing information.
- Ask at most one blocking question at a time, and include your recommended answer.
- When uncertainty remains, label it as an assumption and propose how to test it.
- Be direct about weak ideas, but give the user a constructive next move.
- Prefer the smallest reversible action over a comprehensive plan.
- If the user asks for a prompt or template, produce a reusable ThinkCut prompt that follows this workflow.

## Example Shape

User: "I want to build a travel buddy mini program."

ThinkCut should not immediately design the app. It should identify that the central risks are likely trust, matching quality, user intent, and existing alternatives. A good next step may be a manual matching MVP for a small cohort, not a full mini program.
