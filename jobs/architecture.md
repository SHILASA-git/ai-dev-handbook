# Architecture and design

Never skip design because AI writes code fast. Bad architecture still ships — just quicker.

REFINE: Understand → Design → Implement → Review → Refine. Template: [templates/ARCHITECTURE.md](../templates/ARCHITECTURE.md)

Claude: [tools/claude.md](../tools/claude.md) · Prompts: [prompts.md](../prompts.md)

---

## You own vs AI helps

| Step | You own | AI helps |
|------|---------|----------|
| Understand | Users, scope, non-goals | Clarifying questions, user stories |
| Design | Trade-offs | Mermaid, API table, folder tree |
| Implement | Correctness | Cursor / Copilot |
| Review | Final judgment | Drift checklist |
| Refine | What not to build | “What's over-engineered?” |

---

## Design questions (before codegen)

1. Who uses this? Roughly how many?
2. What must persist vs can live in memory?
3. What is MVP this week vs later?
4. What fails first under load? (name it; don't provision cloud)

Building-block names (know them): client, API, database, cache, load balancer, queue, CDN.

---

## Artifact every project

Copy [templates/ARCHITECTURE.md](../templates/ARCHITECTURE.md). Fill problem, Mermaid, components, API table, trade-offs, “at 10x scale”, security notes.

Day 1 lab: [task tracker](../../ai-workshop/day1/04-lab-task-tracker.md) — `ARCHITECTURE.md` before heavy coding.

---

## Signature prompt (Claude — no code)

```
Design architecture for [project] MVP.
Users: [who], scale: [e.g. 100]
Stack: Python FastAPI, [in-memory / sqlite / files]

Output:
1. Mermaid (UI → API → storage)
2. Component table: name | responsibility | file hint
3. REST API table: method, path, body, success, errors
4. Trade-offs (why this MVP)
5. At 10x scale: 5 bullets (no implementation)

No code.
```

Then Cursor: `Create ARCHITECTURE.md from this. Do not write implementation yet.`

---

## Interview line

> “I designed the API and architecture first with Claude, implemented with Cursor and Copilot, then refined after a review pass for edge cases and security.”
