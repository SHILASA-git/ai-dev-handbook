# Cursor

Primary tool for **multi-file implementation** once `ARCHITECTURE.md` exists.

Setup: [Day 1 tool lab](../../ai-workshop/day1/03-tools-setup-lab.md) · What `@` actually does: [how-editors-work.md](../how-editors-work.md) · Safety: [marketplace.md](../marketplace.md) · Prompts: [prompts.md](../prompts.md)

---

## Modes

| Mode | Use for |
|------|---------|
| **Tab** | Next line in a file you already understand |
| **Chat** | Questions, small edits, “explain this file” |
| **Agent / Composer** | Multi-file features, refactors, tests |

Agent edits your disk. You still Accept, run, and revert with Git.

---

## Context tags

```
@filename.py     — this file
@folder/         — this directory
@codebase        — search the project
@ARCHITECTURE.md — force the design into context
```

**Strong prompt:**

```
@ARCHITECTURE.md @main.py
Implement ONLY POST /tasks and GET /tasks from the API contract.
In-memory storage. No new dependencies.
Show which files you will change, then the diff.
```

---

## Rules and skills

- Copy [templates/cursor/rules/python-student.mdc](../templates/cursor/rules/python-student.mdc) into `.cursor/rules/` on each new repo.
- Optional skill: [review-architecture](../templates/cursor/skills/review-architecture/SKILL.md).
- Marketplace / MCP: off until you need them — [marketplace.md](../marketplace.md).

---

## Agent habits

1. **Small tasks** — one feature per prompt.
2. **Review diffs** file by file.
3. **Run** `uvicorn` / `pytest` / the script after each Accept.
4. **Revert** a bad run with Git. Don't argue with a ruined tree.

---

## When Cursor wins

- Refactor across files
- Scaffold from `ARCHITECTURE.md`
- Fix an error with terminal output pasted
- Add tests that match the API table

## Switch away

- Long design / career / README prose → **Claude**
- Single-line completion while typing → **Copilot**
- “What is CORS?” with sources to check → **ChatGPT or Gemini**, then docs

Job pages: [coding](../jobs/coding.md) · [debugging](../jobs/debugging.md)
