---
name: darwin
description: >
  Pragmatic iterative improvement discipline that preserves what works,
  varies what does not, tests changes against the current best result, and
  escalates strategy only when progress stalls. Use when Codex is asked to
  refine, improve, iterate on, compare attempts for, or recover weak output in
  an answer, plan, implementation, design, prompt, or other artifact without
  open-ended rewriting.
---

# Darwin

Darwin improves work through controlled variation and selection.

## Scope

Use this skill to improve an existing or first-pass artifact by preserving the
strongest result, trying materially different changes, and keeping only proven
improvements.

This skill covers answers, plans, prompts, implementation approaches, designs,
documentation, and other reviewable work products. It does not replace domain
tests, source review, or user requirements.

## When to use

Use Darwin when the user asks to refine, improve, iterate, compare attempts, or
recover weak output.

Prefer a single improvement pass for small tasks. Use multiple attempts only
when the artifact is important, ambiguous, or visibly below the target quality.

## Inputs

- Current task or artifact to improve.
- User constraints, acceptance criteria, or known failure modes.
- Optional examples, tests, rubric, or prior attempts.

If no artifact exists yet, produce the first usable result and treat it as the
initial best result.

## Outputs

By default, output only the final improved result.

Expose attempts, comparisons, or decision notes only when the user asks for an
iteration trace, alternatives, or review rationale.

## Steps / Procedure

1. Produce or identify the first usable result.
2. Treat that result as the current best.
3. Identify what works and what is weak.
4. Create a materially different attempt that targets a real weakness.
5. Compare the attempt against the current best.
6. Keep the attempt only when it is clearly better.
7. Preserve any useful part of a rejected attempt without adopting the whole.
8. Change strategy after two failed improvement attempts.
9. Stop when the result satisfies the task or further gains look marginal.

Default iteration limit: 5.

Valid changes include better accuracy, reasoning, structure, simplicity,
completeness, user fit, and implementation quality. Invalid changes include
cosmetic rewording, extra length without value, repeated approaches, and novelty
for its own sake.

## Examples

User: "Use Darwin to improve this prompt."

Response behavior: create a best prompt, test one or more targeted variations
against the user's goal, keep only the stronger version, and return the final
prompt unless the user asks for the comparison trail.

User: "Improve this plan and implement it."

Response behavior: preserve the working parts of the plan, replace weak or
missing steps, validate the improved plan against the repo, then execute it.

## Limitations / Failure modes

- Do not reward novelty alone.
- Do not mistake verbosity for improvement.
- Do not abandon working parts unnecessarily.
- Do not iterate without a meaningful change.
- Do not continue from a weaker result.
- Do not over-explore simple tasks.

## Security / Tool access

Darwin requires no special tools. Use normal task-appropriate tools only when
they are needed to verify, compare, or implement an improvement.

Never invent evidence. If a comparison depends on tests, source files, or live
state, verify those inputs before treating an attempt as better.
