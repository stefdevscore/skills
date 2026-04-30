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

## Summary

Darwin improves work through controlled variation and selection.

The agent must preserve the strongest result so far, introduce meaningful
changes, keep only proven improvements, and change strategy when progress stalls.

---

## Core Rule

Preserve what works.<br>
Vary what does not.<br>
Keep only what improves.

---

## Process

For non-trivial tasks:

1. Produce a usable result
2. Identify what is working and what is weak
3. Create a materially different improvement attempt
4. Compare it against the current best
5. Keep the attempt only if it improves the result
6. Reuse any clearly valuable parts
7. Change strategy if improvement stalls

---

## Rules

### 1. Best Result

The first usable result becomes the Best Result.

The Best Result must be preserved until a clearly better result replaces it.

Never overwrite the Best Result with an unproven attempt.

---

### 2. Controlled Variation

Each attempt must make a meaningful change.

Valid changes:
- Better accuracy
- Better reasoning
- Better structure
- Better simplicity
- Better completeness
- Better fit to the user's goal
- Better implementation quality

Invalid changes:
- Rewording without improvement
- Added length without value
- Cosmetic formatting
- Repeating the same approach
- Novelty for its own sake

---

### 3. Selection

After each attempt, compare it to the Best Result.

Keep the attempt only if it is clearly better.

Discard it if it is worse, unclear, or merely different.

If an attempt has one useful part, preserve that part without adopting the whole attempt.

---

### 4. Escalation

If two attempts fail to improve the Best Result, change strategy.

A strategy change must alter the method, not just the wording.

Valid strategy changes:
- Simplify the solution
- Reframe the problem
- Use a different structure
- Check assumptions
- Decompose the task
- Generate a small set of alternative approaches
- Verify against examples, tests, or constraints

---

### 5. Convergence

Stop when:

- The Best Result satisfies the task
- Further changes are likely to be marginal
- The iteration limit is reached

Default iteration limit: 5.

Use fewer iterations for simple tasks. Prefer one pass for small tasks. Stop early when added work would not change the user-visible result.

---

## Output

Use the improvement loop internally by default.

Do not expose attempts, comparisons, or decision notes unless the user asks for
an iterative trace, alternatives, or review rationale.

Only use this format when the user asks for visible iteration or when review/debug rationale is needed:

### Best Result
[Current best result]

### Attempt
[New improvement attempt]

### Decision
Keep or discard:<br>
Reason:<br>
Preserved parts:<br>
Next change:

---

## Constraints

- Do not reward novelty alone
- Do not mistake verbosity for improvement
- Do not abandon working parts unnecessarily
- Do not keep iterating without meaningful change
- Do not continue from a weaker result
- Do not over-explore simple tasks

---

## Tagline

Preserve. Vary. Select.
