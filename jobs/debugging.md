# Debugging

Paste the **full traceback**, say what you expected, ask for a **minimal** fix, then **run it**. Don't debug by generating a new app.

Tools: [Claude](../tools/claude.md) (diagnose) → [Cursor](../tools/cursor.md) (apply) · Copilot `/fix` on a selection

---

## Tool order

1. Reproduce once. Copy the traceback.
2. **Claude or Cursor Chat:** root cause in plain English + smallest patch.
3. **Cursor:** apply that patch only; add one test that would have caught it.
4. Run again. If still broken, **narrow** (“only line 12”, “404 not 500”).

Copilot `/fix` is fine when the broken function is already on screen.

---

## Checklist

- [ ] Full traceback, not “it doesn't work”
- [ ] Expected vs actual (status code, body, file moved or not)
- [ ] No `.env` in the paste
- [ ] Fix is small — not a refactor
- [ ] You ran the command again after Accept

---

## Signature prompts

**Diagnose (Claude):**

```
Traceback:
[paste]

Code:
[paste relevant file]

1. Root cause in plain English
2. Minimal fix only
3. How to prevent this class of bug
```

**Apply (Cursor):**

```
@main.py
Apply this fix: [paste Claude's minimal fix]
Add one test that would have caught this bug.
```

---

## Common failures

| Symptom | Likely |
|---------|--------|
| `ModuleNotFoundError` | venv not activated |
| Agent “fixes” the wrong file | Missing `@filename` |
| Invented library in the patch | “stdlib + fastapi only” |
| CORS / blank UI | Serving `file://` instead of FastAPI `/` |

Prompt quality: [prompting.md](../prompting.md)
