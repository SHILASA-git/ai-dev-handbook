# Researching

Use ChatGPT or Gemini to **get a first explanation**, then **verify in official docs**. Research is not “the model said so.”

Tools: [ChatGPT](../tools/chatgpt.md) · [Gemini](../tools/gemini.md) · Day 2 drill: [productivity clinic](../../ai-workshop/day2/01-productivity-clinic.md)

---

## Tool order

1. One short prompt (5 bullets + sources to open).
2. Open the **official** page (FastAPI, MDN, Python docs, OWASP).
3. Tick or **reject** at least one claim.
4. If you will implement: switch to Cursor — don't paste a tutorial project blindly.

Claude is fine for “explain like 4th-year CSE” **after** you have the doc open, or for comparing two options you already named.

---

## Checklist

- [ ] Prompt asks for sources / official URLs
- [ ] You opened the doc in a real browser tab
- [ ] One claim marked true or false
- [ ] No secrets in the paste
- [ ] You wrote 3 bullets in `LEARNING.md` **in your words**

---

## Signature prompt

```
Explain [CORS / 422 validation / pathlib rglob] for a 4th-year CSE student.
5 bullets + one short example.
List the official doc URL I should open next.
I will verify each claim against that page.
```

---

## Common failures

| Don't | Do |
|-------|----|
| Trust a made-up library name | Search PyPI / official docs |
| Paste a whole blog into the repo | Cite the official page in LEARNING.md |
| Use research chat as the architect | [architecture.md](architecture.md) with Claude |
| Skip verify because the lab is timed | Verify **one** claim — that's the drill |

Readings after the workshop: [after/follow-up.md](../after/follow-up.md)
