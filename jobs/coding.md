# Coding

Implement **one feature** that already exists on the API table. If there is no `ARCHITECTURE.md`, stop and [design first](architecture.md).

Tools: [Cursor](../tools/cursor.md) · [Copilot](../tools/copilot.md) · [prompts.md](../prompts.md) · Don'ts: [what-not-to-do.md](../what-not-to-do.md)

---

## Tool order

1. Open `@ARCHITECTURE.md` in Cursor.
2. Cursor Agent: one endpoint / one script flag / one UI hook.
3. Copilot Tab: fill obvious lines **inside** that file.
4. Run it. Then Claude review if you have time.

---

## Checklist

- [ ] Prompt names the files (`@main.py`) and the **only** behaviour to add
- [ ] “No new dependencies” / “stdlib + fastapi” if that is the stack
- [ ] Diff reviewed file by file — not one 500-line Accept
- [ ] `uvicorn` / `pytest` / script `--dry-run` actually ran
- [ ] Routes still match the API table (no surprise fields)

---

## Signature prompt (Cursor)

```
@ARCHITECTURE.md @main.py

Implement ONLY POST /tasks and GET /tasks from the API contract.
Use TaskStore + Pydantic. 422 on invalid body. In-memory. No new deps.
Show files you will change, then the diff.
```

Copilot, while typing:

```python
# GET /tasks/{id} - return Task or HTTPException 404
```

---

## Common failures

| What happened | Fix |
|---------------|-----|
| Agent invented Flask / extra packages | “stdlib + fastapi only” |
| Changed files you didn't ask for | `@filename` + “do not change API behaviour” |
| UI blank | Don't open `file://` — serve HTML from FastAPI |
| “It compiles” but contract drift | Claude review vs ARCHITECTURE |

After it works: [analyzing.md](analyzing.md) or [debugging.md](debugging.md).
