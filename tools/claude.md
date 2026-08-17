# Claude

Primary tool for **design, review, and docs**. Weak as a replacement for the editor — paste snippets back, or switch to Cursor to apply.

Setup: [Day 1 tool lab](../../ai-workshop/day1/03-tools-setup-lab.md) · Prompts: [prompts.md](../prompts.md)

---

## Where it wins

| Use | Why |
|-----|-----|
| Architecture trade-offs | Long reasoning |
| API contract tables | Structured output |
| Senior-style code review | Checklists vs `ARCHITECTURE.md` |
| README / LEARNING.md draft | Clear prose — **you** edit |
| Explain unfamiliar code | Large paste (redact secrets) |

---

## Projects (claude.ai)

Create a project **AI Workshop** (or your hackathon name). Upload lab specs and architecture drafts — **not** `.env` or other people's data.

Keeps context across chats. Still re-paste the current `ARCHITECTURE.md` before a review.

---

## Signature prompts

**Design (no code):**

```
I'm building [X] for [users].
Constraints: Python FastAPI, 1-week timeline, pair.
Compare 2 approaches in a table (pros, cons, complexity).
Recommend one MVP. Output a Mermaid diagram.
No implementation code.
```

**Review:**

```
Senior engineer review vs ARCHITECTURE.md.
Format: Critical / Medium / Nice-to-have.
Also list architecture drift.

ARCHITECTURE:
[paste]

CODE:
[paste — no secrets]
```

---

## Limits

- May invent APIs — verify in official docs.
- No live access to your repo — paste, or use Cursor.
- Don't upload graded exams or confidential college data.

---

## Workflow with Cursor

1. **Claude** — plan + API design → you save `ARCHITECTURE.md`
2. **Cursor** — implement
3. **Claude** — review diff before push

Interview line: *“I use Claude for design and review; I implement in Cursor and can explain every decision.”*

Jobs: [architecture](../jobs/architecture.md) · [analyzing](../jobs/analyzing.md)
