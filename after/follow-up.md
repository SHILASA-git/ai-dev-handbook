# Follow-up — Readings & Writing (4 weeks)

After the 2-day workshop. **3–5 hours/week.** Pick **one** [track](README.md) for building; use this file for **reading and writing** every week.

Writing is not extra fluff — interviews and OSS both reward people who can **explain**.

---

## Week 0 (optional, before or right after Day 1)

| Read (20 min) | Why |
|---------------|-----|
| [What is an LLM?](https://huggingface.co/learn/llm-course/chapter1/1) — first page only | Vocabulary |
| Handbook [ai-history.md](../ai-history.md) | Regression → nets → GPTs → agents |
| FastAPI first steps: [Tutorial](https://fastapi.tiangolo.com/tutorial/) | Matches Day 1 |

---

## Readings (pick from your track)

Do **one** reading per week. Take 5 bullets in `LEARNING.md` — in your words, not pasted from the model.

### Everyone

| Resource | Length | Use |
|----------|--------|-----|
| [Anthropic prompt engineering](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) | Short | Better prompts |
| [OWASP Top 10](https://owasp.org/www-project-top-ten/) | Skim 3 items | AppSec vocabulary |
| [GitHub Skills](https://skills.github.com/) | 1 course | PRs, issues |
| [The Missing Semester — Git](https://missing.csail.mit.edu/2020/version-control/) | 1 lecture | Git confidence |

### Full-stack

| Resource | Why |
|----------|-----|
| [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) | Official, matches lab |
| [MDN: Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) | Your UI uses this |
| [HTTP status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) — 2xx/4xx only | API contract |

### Automation

| Resource | Why |
|----------|-----|
| [pathlib docs](https://docs.python.org/3/library/pathlib.html) | You used it on Day 2 |
| [Real Python — automating with Python](https://realpython.com/python-csv/) | CSV patterns |
| [schedule library README](https://github.com/dbader/schedule) | Next step after argparse |

### AppSec

| Resource | Why |
|----------|-----|
| [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/) | Contribution-friendly docs |
| [gitleaks README](https://github.com/gitleaks/gitleaks) | How real scanners work |
| [PortSwigger — what is XSS?](https://portswigger.net/web-security/cross-site-scripting) — intro only | Web risk, ethical lab later |

### System design (all tracks)

| Resource | Why |
|----------|-----|
| [System Design Primer](https://github.com/donnemartin/system-design-primer) — **first two sections only** | Names for load balancer, cache, DB |
| Your own `ARCHITECTURE.md` | Re-read weekly; keep it honest |

### AI product (optional track)

| Resource | Why |
|----------|-----|
| [RAG overview (short)](https://github.com/langchain-ai/langchain) — README only | Don't over-depend |
| [Ollama](https://github.com/ollama/ollama) | Local models, no cloud key |
| Handbook: [how-editors-work.md](../how-editors-work.md) + [build-context.md](build-context.md) | Pack → keyword RAG → Chroma → MCP |

**Skip for this workshop's follow-up:** AWS/GCP getting-started guides, Kubernetes, IAM deep dives — unless you get access later on your own.

---

## Writing assignments

Commit these to your GitHub repo (or a `notes/` folder). Claude can **draft**; you must **edit until it sounds like you**. Copy [templates/LEARNING.md](../templates/LEARNING.md).

### Weekly (everyone)

Create `LEARNING.md` and append each week:

```markdown
## Week N — YYYY-MM-DD

### Built
-

### AI got wrong (at least one)
-

### I verified by
-

### Read
- Title / URL — 3 bullets in my words

### Next week
-
```

### Choose **two** extra writing pieces this month

| Piece | Length | Audience |
|-------|--------|----------|
| **README polish** | Recruiter skim (60 seconds) | Hiring |
| **Architecture note** | 1 page: one trade-off you chose | You, later |
| **OSS PR description** (even if you don't send it) | Problem, change, test plan | Maintainers |
| **LinkedIn or blog** | ~200 words: "Design first, then AI" | Public |
| **Issue comment** on your bookmarked repo | 4–8 sentences: reproduction or docs gap | Maintainers |
| **SECURITY.md** | Secrets, auth TODO, error messages | Your future self |

**Prompt for the blog/LinkedIn piece:**

```
I am a 4th-year CSE student. I designed a Task Tracker API before generating code.
Write 200 words in first person, no hype, no buzzword pile.
Include: one AI mistake I caught, one tool I used (Cursor/Copilot/Claude).
I will edit this — keep sentences short.
```

---

## OSS contribution (writing + code)

Minimum this month:

- [ ] Read CONTRIBUTING.md of [your bookmarked repo](oss.md)
- [ ] One of: practice PR on [first-contributions](https://github.com/firstcontributions/first-contributions) **or** a **docs typo/fix** PR **or** a thoughtful issue comment

Do **not** open a feature PR generated entirely by an agent.

---

## How AI should help reading & writing

| Good | Bad |
|------|-----|
| "Summarize this FastAPI page in 5 bullets; I'll check the page" | "Write my LEARNING.md from nothing" |
| "Tighten this PR description; keep my facts" | Fake "I reproduced this" if you did not |
| "Quiz me on OWASP A01 from my notes" | Paste copyrighted chapters into chat |

---

## Checkpoint (end of week 4)

- [ ] `LEARNING.md` has 4 weekly entries
- [ ] One public writing piece **or** one OSS interaction
- [ ] Mini-project README is recruiter-readable
- [ ] You can explain your architecture without opening a chat
