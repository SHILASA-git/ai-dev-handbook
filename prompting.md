# Prompting

How you ask matters more than which model you pick. Same bug, three prompt strengths — that is the Day 1 lab.

---

## Anatomy of a strong prompt

| Part | Example |
|------|---------|
| **Role / context** | “FastAPI Task Tracker, in-memory store, student MVP” |
| **Task** | “Add PUT `/tasks/{id}` only” |
| **Constraints** | “No new dependencies. Match `ARCHITECTURE.md`.” |
| **Output shape** | “Minimal diff. Show files you will touch first.” |

Paste **file names, expected vs actual, and traceback**. Do not paste secrets.

---

## Quality ladder (use this live)

**Level 1 (weak):** `Fix my code`

**Level 2:** `Fix 404 handling in GET /tasks/{id}`

**Level 3 (strong):**

```
File: main.py (FastAPI)
Bug: POST /tasks returns 200 but body is empty
Expected: 201 + created task with id
Constraints: in-memory store, no new deps
Show minimal diff only
```

If the model rambles: add “3 bullets, then the patch.”

---

## Sequence (not one mega-prompt)

1. **No code yet** — clarifying questions, MVP vs non-goals.
2. **Design** — Mermaid + API table → you save `ARCHITECTURE.md`.
3. **One feature** — one endpoint or one function.
4. **Review** — does code match the design?
5. **Refine** — smallest fix, then run.

---

## Verify loop

| Kind of answer | You must |
|----------------|----------|
| Code | Run it. Read the diff. |
| Fact / API / status code | Open **official docs**. Tick or reject one claim. |
| Architecture | You choose the trade-off. AI lists options. |

Hallucinations are normal. Confident ≠ correct.

---

## Anti-patterns

| Don't | Do instead |
|-------|------------|
| “Build entire app” | One endpoint per prompt |
| Paste `.env` with real keys | Describe variable **names** only |
| “Make it production ready” | A 5-item checklist you can finish today |
| Accept a 500-line Agent diff | File-by-file; run tests after each accept |
| Skip `ARCHITECTURE.md` | Design prompt first, always |
| Trust a blog-style ChatGPT answer | Official docs next |

Copy-paste library: [prompts.md](prompts.md) · What the editor packs around your prompt: [how-editors-work.md](how-editors-work.md)
