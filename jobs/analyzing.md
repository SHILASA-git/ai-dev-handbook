# Analyzing

Compare options, review a repo, or catch **architecture drift**. Analysis is a judgment call — AI drafts the list, you pick.

Tools: [Claude](../tools/claude.md) · [Cursor](../tools/cursor.md) Chat (read-only) · [prompts.md](../prompts.md)

---

## Tool order

| Question | Tool |
|----------|------|
| 2–3 design options, pros/cons | **Claude** |
| “What does this repo do?” | Cursor Chat `@codebase` — **no edits** |
| Pre-demo / pre-PR review | **Claude** vs `ARCHITECTURE.md` |
| “What's over-engineered for MVP?” | **Claude** |
| Apply the 3 fixes | **Cursor** after you agree |

Optional: copy the [review-architecture skill](../templates/cursor/skills/review-architecture/SKILL.md) into the project.

---

## Checklist

- [ ] You pasted current `ARCHITECTURE.md` (or `@` it)
- [ ] Review format is Critical / Medium / Nice-to-have
- [ ] You ignore Nice-to-have before a demo
- [ ] You can say the trade-off in one sentence without the chat

---

## Signature prompts

**Repo (Cursor, read only):**

```
@codebase @README.md
Summarize this repo in 5 bullets.
What's missing for a classmate demo?
No code changes.
```

**Review (Claude):**

```
Senior engineer review.

ARCHITECTURE:
[paste]

CODE:
[paste]

## Critical
## Medium
## Nice-to-have
## Drift from architecture
```

---

## Common failures

- Asking Cursor Agent to “improve everything” — that is coding, not analysis.
- Accepting a rewrite instead of a prioritized list.
- Reviewing without the API table — you will miss contract bugs.

Next: [coding.md](coding.md) for the Critical items only.
