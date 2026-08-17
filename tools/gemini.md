# Gemini

Second **chat** model for the Day 1 comparison lab and for research. Same rules as ChatGPT: **no repo**, verify in official docs.

Lab: [day1/01-ai-landscape.md](../../ai-workshop/day1/01-ai-landscape.md) · Research: [jobs/researching.md](../jobs/researching.md)

---

## When it wins

| Use | Why |
|-----|-----|
| Same prompt as ChatGPT and Claude | Compare mistakes and tone (Day 1) |
| Concept explanation | Backup if ChatGPT is down or vague |
| “List sources I should verify” | Starting URLs — you open them |

It is **not** the primary coder in this workshop. Don't fight Cursor vs Gemini for implementing FastAPI.

---

## Signature prompt (same as ChatGPT — compare outputs)

```
Explain CORS in FastAPI for a 4th-year CSE student.
Give 5 bullets + one example.
List sources I should verify.
```

Score **quality**, not speed: did it invent a library? Did you run or verify anything?

---

## Day 1 scoring (pairs)

After ChatGPT → Claude → Gemini on the **same** buggy function:

- Which caught the bug?
- Which hallucinated an API?
- Who actually **ran** the fix?

Then try the same fix in Cursor with `@file` — editor context vs paste-into-chat.

---

## Switch away

| Need | Use |
|------|-----|
| Architecture + API table | **Claude** |
| Multi-file implement | **Cursor** |
| Inline completion | **Copilot** |
| Research (alternate) | **ChatGPT**, then the same official doc |

Never paste secrets. Workshop ≠ graded assignments — ask faculty before using Gemini on coursework.
