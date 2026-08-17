---
name: review-architecture
description: Reviews implementation against ARCHITECTURE.md. Use when the user asks for a design review, architecture drift check, pre-demo review, or whether code matches the API contract.
---

# Review against architecture

## Instructions

1. Read `ARCHITECTURE.md` (and the API contract table if present). If missing, say so and stop.
2. Read the implementation files the user mentioned (or `main.py`, `store.py`, tests).
3. Compare code to the design. Do not suggest new features.

## Output format

```markdown
## Critical (must fix before demo)
-

## Medium
-

## Nice-to-have
-

## Drift from ARCHITECTURE.md
- (bullet list; "none" if aligned)
```

Keep the whole review under 40 lines. No rewritten codebase — list edits only.
