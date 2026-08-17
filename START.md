# START — Which Tool When

Project this page. Keep it open both days.

**Design** with Claude · **Implement** with Cursor / Copilot · **Refine** with Claude · **Research** with ChatGPT or Gemini (then verify)

---

## Decision matrix

| Task | First choice | Why |
|------|--------------|-----|
| API contract, `ARCHITECTURE.md` | **Claude** | Design before code |
| Mermaid system diagram | **Claude** | Long reasoning |
| Write the next 5 lines in a known file | **Copilot** | Lowest friction |
| Add a feature across 3 files | **Cursor Agent** | Must match architecture |
| Debug a traceback | **Claude or Cursor Chat** | Paste error + file |
| README / long docs | **Claude** | Prose |
| Inline docstring | **Copilot** | Already in the file |
| Research a concept | **ChatGPT or Gemini** | Then open official docs |
| Same-prompt comparison (Day 1) | **ChatGPT + Claude + Gemini** | Score quality, not speed |
| Pre-demo review | **Claude** | “Does code match the diagram?” |

---

## Five rules

1. **Read every diff** before Accept.
2. **Run the code** after every AI edit (`uvicorn`, `pytest`, or the script).
3. **Never paste secrets** — passwords, API keys, college credentials, `.env`.
4. **One feature per prompt.** Not “build the entire app.”
5. **You own what ships.** Interviews: “I used AI to draft; I reviewed and can explain every line.”

---

## REFINE loop

```
UNDERSTAND  →  Claude: questions + user stories
DESIGN      →  Claude: Mermaid + API table → Cursor: ARCHITECTURE.md
IMPLEMENT   →  Cursor: @ARCHITECTURE multi-file | Copilot: comments + Tab
REVIEW      →  Claude: review vs design | Cursor/Copilot: tests
REFINE      →  Claude: prioritize fixes → Cursor: minimal diff
DOCUMENT    →  Claude: README | Copilot: docstrings
```

Full prompts: [prompts.md](prompts.md) · Architecture: [jobs/architecture.md](jobs/architecture.md)
