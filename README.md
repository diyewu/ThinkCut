# ThinkCut

[中文说明](README.zh-CN.md)

ThinkCut is a Codex skill that turns fuzzy ideas into clear decisions, key assumptions, pressure-tested risks, and minimal validation actions.

It is useful when a user has a product idea, feature decision, strategy question, execution plan, content direction, or any proposal that feels promising but still too vague to act on.

## What It Does

ThinkCut helps an agent move from:

```text
"I want to build a travel buddy mini program."
```

to:

```text
Decision:
Do not build the full mini program yet.

Key assumption:
Travelers will trust a lightweight matching flow enough to meet strangers.

Stress Pass:
Existing alternatives such as group chats, social posts, and travel communities may already solve the need well enough.

Minimal validation:
Run a manual matching test with 20 travel buddy requests before building the app.
```

The goal is not to brainstorm more ideas. The goal is to cut through ambiguity and produce the next useful decision.

## Workflow

ThinkCut uses a five-step workflow:

1. **Problem Calibration**
   Restate the user's vague idea as a concrete decision.

2. **Assumption Mapping**
   Separate facts, assumptions, conventions, and missing evidence.

3. **Stress Pass**
   Pressure-test the branches that could break the idea.

4. **Minimal Validation**
   Choose the smallest action that can test the riskiest assumption.

5. **Decision Brief**
   Produce a compact brief with judgment, risks, validation, success criteria, and next action.

## Methods Used

ThinkCut combines:

- Socratic questioning for problem calibration
- First-principles thinking for assumption mapping
- Bounded stress testing for risk discovery
- Ockham's razor for reducing complexity
- Decision records for making the next action clear

## Install

Clone the repository and copy the skill into your local Codex skills directory:

```bash
git clone https://github.com/diyewu/ThinkCut.git
cd ThinkCut
mkdir -p ~/.codex/skills/thinkcut
rsync -a --exclude .git ./ ~/.codex/skills/thinkcut/
```

Restart Codex after installation so the new skill can be picked up.

If you are installing from the current implementation branch:

```bash
git clone -b codex/implement-thinkcut https://github.com/diyewu/ThinkCut.git
cd ThinkCut
mkdir -p ~/.codex/skills/thinkcut
rsync -a --exclude .git ./ ~/.codex/skills/thinkcut/
```

## Usage

Invoke it explicitly:

```text
$thinkcut I want to build a travel buddy mini program. Turn it into key assumptions, a stress pass, and a minimal validation plan.
```

Other examples:

```text
$thinkcut Should I build this feature?
```

```text
$thinkcut Pressure-test my product plan and give me the smallest validation step.
```

```text
$thinkcut I have a content idea. Help me decide whether it is worth doing.
```

## Output Shape

ThinkCut usually ends with a compact decision brief:

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

## Repository Structure

```text
ThinkCut/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── LICENSE
├── README.md
└── README.zh-CN.md
```

## License

ThinkCut is licensed under the Apache License, Version 2.0. See [LICENSE](LICENSE).
