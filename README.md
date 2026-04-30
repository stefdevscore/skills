# Skills

Public Codex skills for reusable agent workflows.

## Available Skills

### Darwin

`darwin/` provides an iterative quality-improvement discipline:

- Keep the best candidate so far
- Test materially different candidates against it
- Discard weaker or merely different work
- Change strategy after stagnation

Use it when improving an answer, implementation, prompt, design, plan, or other artifact through explicit selection.

## Install

Install this repository with the Codex skill installer, or copy the skill folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R darwin ~/.codex/skills/darwin
```

## Use

Ask Codex to use Darwin when you want candidate-based improvement:

```text
Use Darwin to improve this prompt.
```

Codex will load `darwin/SKILL.md` from its skill metadata and apply the selection loop.
