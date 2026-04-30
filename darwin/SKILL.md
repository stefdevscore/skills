# Darwin

## Summary

Darwin forces an agent to improve through selection.

The agent must maintain the best result so far, test new candidates against it, and discard anything that does not improve the outcome.

---

## Core Rule

Keep the best.  
Discard worse.  
Change strategy when stuck.

---

## Process

For non-trivial tasks:

1. Create a candidate
2. Compare it to the current best
3. Keep it only if it is clearly better
4. Discard it if it is worse or merely different
5. Change strategy after repeated failure

---

## Rules

### 1. Best Candidate

The first usable result becomes the Best Candidate.

The Best Candidate must always be preserved.

---

### 2. Candidate Generation

Each new candidate must make a material change.

Valid changes:
- Better structure
- Better reasoning
- Better accuracy
- Better simplicity
- Better fit to the user’s goal

Invalid changes:
- Rewording
- Added length without added value
- Cosmetic formatting
- Repeating the same approach

---

### 3. Selection

After each candidate, decide:

- Is it clearly better than the Best Candidate?

If yes:
- Replace the Best Candidate

If no:
- Discard it

Never continue from a weaker candidate.

---

### 4. Stagnation

If two candidates fail to improve the Best Candidate:

- Stop using the current approach
- Change strategy

A strategy change must alter the method, not just the wording.

---

### 5. Stop

Stop when:

- The Best Candidate satisfies the task, or
- Further changes are unlikely to improve it, or
- The iteration limit is reached

Default iteration limit: 5.

---

## Output Format

### Best Candidate
[Current best result]

### Candidate
[New attempt]

### Decision
Keep or discard:  
Reason:  
Next change:

---

## Constraints

- Do not reward novelty alone
- Do not mistake verbosity for improvement
- Do not overwrite the best result with a weaker one
- Do not keep iterating without material change

---

## Tagline

Keep the best. Discard the rest.
