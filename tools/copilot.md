# GitHub Copilot

Primary tool for **inline speed** while you are already in the file. Weak for whole-repo architecture.

Setup: [Day 1 tool lab](../../ai-workshop/day1/03-tools-setup-lab.md) · Prompts: [prompts.md](../prompts.md)

---

## Keyboard

| Action | Mac | Windows / Linux |
|--------|-----|-----------------|
| Accept | Tab | Tab |
| Dismiss | Esc | Esc |
| Next suggestion | Option + ] | Alt + ] |
| Previous | Option + [ | Alt + [ |

Chat commands on a **selection**: `/explain` · `/fix` · `/tests`

---

## Comment as prompt

Copilot sees the current file (and sometimes open tabs) — not the whole repo unless Chat has codebase context.

```python
# GET /tasks/{id} - return Task or raise HTTPException 404
@app.get("/tasks/{task_id}")
def get_task(task_id: int):
```

```python
# pytest: POST /tasks with empty title returns 422
def test_create_empty_title():
```

Accept **partially**. Edit names. Check against your API table.

---

## Good uses

- pytest boilerplate
- Pydantic models from a JSON example
- Repetitive CRUD once the first endpoint is correct
- Docstrings after the signature

## Bad uses

- Architecture decisions
- Unknown PyPI packages it invents
- Crypto / auth you cannot explain
- Commit messages you didn't read (edit them)

---

## vs Cursor Agent

| Copilot | Cursor Agent |
|---------|----------------|
| You drive file-by-file | AI edits multiple files |
| Lower risk | Faster — review more |

Use Copilot when you are **in flow** typing. Use Cursor when you are **delegating a feature** from `ARCHITECTURE.md`.

Job: [coding](../jobs/coding.md)
