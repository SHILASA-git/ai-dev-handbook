# Track — AppSec (4 weeks)

Local **application security** — secrets, OWASP, hardening the code you write. Ethical learning only. **No requirement for cloud accounts.**

Handbook: [marketplace.md](../marketplace.md) · [jobs/analyzing.md](../jobs/analyzing.md)

---

## Outcomes

- Scan your own repos before you push
- Name OWASP risks in *your* FastAPI app
- One portfolio artifact: scanner + `SECURITY.md`

---

## Module 1 — Secrets hygiene (Week 2)

**Learn:** `.gitignore`, `.env.example`, rotation if you ever leaked a toy key (only toy keys).

**Build:** Harden Day 2 `scan_repo.py` — fail if `.env` is not gitignored; skip binaries.

---

## Module 2 — OWASP on your API (Week 2)

**Learn:** Injection, broken auth, sensitive data exposure — using [OWASP Top 10](https://owasp.org/www-project-top-ten/).

**Build:** Claude review of your routes + a `SECURITY.md` with TODOs (auth, rate limit, generic errors).

**AI prompt:**

```
AppSec checklist for a student FastAPI app on localhost.
Focus: secrets, auth gaps, error messages, prompt-injection if we add an LLM later.
Prioritize high/med/low. No cloud vendor list.
```

---

## Module 3 — Mini project (Week 3)

Pick one:

| Project | Description |
|---------|-------------|
| **Pre-commit scanner** | Wrapper script you run before `git push` |
| **Juice Shop notes** | Run [OWASP Juice Shop](https://github.com/juice-shop/juice-shop) **locally**; write 1 page of findings (no attacking others) |
| **Docs contribution** | Small PR to [OWASP CheatSheetSeries](https://github.com/OWASP/CheatSheetSeries) |

---

## Module 4 — Hackathon ideas (AppSec)

- Secret scanner for classmate repos (with permission)
- Educational "bad vs good" demo repo (dummy secrets only)
- FastAPI middleware that strips stack traces in non-debug mode

---

## OSS path

1. [OWASP/CheatSheetSeries](https://github.com/OWASP/CheatSheetSeries) — docs first
2. [gitleaks/gitleaks](https://github.com/gitleaks/gitleaks)
3. [juice-shop/juice-shop](https://github.com/juice-shop/juice-shop) — learn, don't "contribute exploits"

Readings & writing: [follow-up.md](follow-up.md) · Repos: [oss.md](oss.md)

---

## Interview talking point

> "I wrote a Python secret scanner, keep secrets out of Git, and can walk through OWASP risks on my own FastAPI app. I treat AI like an intern — I don't paste credentials or blindly run commands."
