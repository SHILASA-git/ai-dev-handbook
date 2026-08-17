# ChatGPT

Use for **research and the Day 1 comparison lab**. It has **no repo context** unless you paste. Do not treat it as your architect or your IDE.

Lab: [day1/01-ai-landscape.md](../../ai-workshop/day1/01-ai-landscape.md) · Research job: [jobs/researching.md](../jobs/researching.md)

---

## When it wins

| Use | Why |
|-----|-----|
| Same-prompt comparison (Day 1) | See hallucinations vs Claude / Gemini |
| “Explain X for 4th-year CSE” | Fast first pass |
| List official doc URLs to open next | Starting point — you still open them |
| Study Q&A | Then verify |

Custom GPTs / extra plugins: skip for this workshop. One chat is enough.

---

## Signature prompt (research, then verify)

```
Explain CORS for a FastAPI + static HTML app on localhost.
5 bullets. One short example.
List the official doc URL I should open next.
I will tick or reject each claim against that page.
```

Then open the FastAPI CORS docs. **Tick or reject one claim.** If you skip that step, you didn't research — you copied.

---

## What ChatGPT does not see

- Your files, Git status, or terminal — unless you paste
- Fresh private APIs — it may invent package names

Never paste `.env`, tokens, or classmate data.

---

## Switch away

| Need | Use |
|------|-----|
| Design `ARCHITECTURE.md` | **Claude** |
| Edit three files to match a contract | **Cursor Agent** |
| Next 5 lines while typing | **Copilot** |
| Second opinion on the same research prompt | **Gemini**, then docs |

Anti-pattern: asking ChatGPT to “write my whole FastAPI app” and pasting it blindly into Cursor.
