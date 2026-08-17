# Copy-paste prompts

Edit the bracketed parts. Run in **job order**, not all at once. How-to: [prompting.md](prompting.md) · [START.md](START.md)

---

## Understand

**Claude**

```
I'm a 4th-year CSE student building [project] for [who].

1. 5 clarifying questions before design
2. MVP for a 3-hour lab vs 1-week hackathon
3. 3 non-goals (do not build now)

Python, FastAPI unless I say otherwise.
```

**Cursor (read only)**

```
@codebase @README.md
Summarize this repo in 5 bullets. What's missing for a demo?
No code changes.
```

---

## Design

**Claude**

```
Design architecture for [project] MVP.
Users: [who] · scale: [e.g. ~100]
Stack: Python 3.11, FastAPI, [in-memory | sqlite | files]

Output:
1. Mermaid (UI → API → storage)
2. Component table: name | responsibility | file hint
3. API table: method, path, body, success, errors
4. Trade-offs for this MVP
5. At 10x scale: bullets only

No code.
```

**Cursor**

```
Create ARCHITECTURE.md from this spec. Mermaid + API table + MVP vs scale-up.
Do not write implementation code.
```

---

## Implement

**Cursor Agent**

```
@ARCHITECTURE.md @main.py
Implement ONLY [one endpoint or feature] from the API contract.
No new dependencies. Show files then diff.
```

```
@main.py @static/index.html @ARCHITECTURE.md
Add CORS and serve static/index.html at GET /.
UI calls existing /tasks via fetch. Do not change API behaviour.
```

**Copilot (comment + Tab)**

```python
# GET /tasks/{id} - return Task or HTTPException 404
# pytest: POST empty title returns 422
```

**Claude** (only if Cursor is down — you merge by hand)

```
Write FastAPI for PUT /tasks/{id} (title, done). 404 if missing.
Match this API table: [paste]
Single snippet only.
```

---

## Review, debug, refine, document

**Claude — review**

```
Senior engineer review vs ARCHITECTURE.md.
## Critical  ## Medium  ## Nice-to-have  ## Drift
[paste architecture + code — no secrets]
```

**Claude — debug**

```
Traceback: [paste]
Code: [paste]
1. Root cause  2. Minimal fix  3. How to prevent
```

**Cursor — apply fix**

```
@main.py
Apply this fix: [paste]
Add one test that would have caught it.
```

**Claude — refine**

```
This works for demo. Don't over-engineer.
1. One refactor for clarity
2. What stays out of MVP
3. README Architecture section, 150 words
```

**Claude — README**

```
README for a recruiter (60-second skim): Problem, Architecture link,
Setup, Run API, Run UI, one curl, 2 honest sentences on what AI did.
Stack: Python FastAPI.
```

**Research (ChatGPT or Gemini — then official docs)**

```
Explain [topic] for 4th-year CSE. 5 bullets + one example.
Official URL I should open next. I will verify.
```

---

## Day 1 — Task Tracker + UI

| # | Phase | Tool | Do this |
|---|-------|------|---------|
| 1 | Understand | Claude | Questions + user stories |
| 2 | Design | Claude | Task Tracker architecture (no code) |
| 3 | Design | Cursor | Create `ARCHITECTURE.md` |
| 4 | Implement | Cursor | POST/GET `/tasks` from contract |
| 5 | Implement | Copilot | Fill bodies + Pydantic via comments |
| 6 | Implement | Cursor | UI + CORS |
| 7 | Review | Claude | Code vs ARCHITECTURE |
| 8 | Refine | Cursor | Fix one Critical issue |

---

## Day 2 — automation, AppSec, mini-project

| # | Tool | Do this |
|---|------|---------|
| 1 | Mix | Productivity clinic: code / debug / docs / research |
| 2 | Claude | File organizer I/O diagram |
| 3 | Cursor | `organize_downloads.py` + `--dry-run` |
| 4 | Cursor | `scan_repo.py` |
| 5 | Claude | AppSec checklist vs Task Tracker |
| 6 | Browser | Bookmark one OSS repo |
| 7 | Claude | Mini-project architecture (10 min) |
| 8 | Cursor + Copilot | MVP only |
| 9 | Claude | Pre-demo review |
| 10 | Claude | README + `LEARNING.md` first entry |

**Automation**

```
Design a file organizer: input folder, group by extension, dry-run flag.
Mermaid + edge cases (hidden files, duplicates). No code.
```

```
@ARCHITECTURE.md
Implement organize_downloads.py. argparse --dry-run. pathlib + shutil only.
```

**AppSec**

```
Review this tree + .gitignore for secret leaks before push.
[paste tree]  No cloud — Git hygiene + FastAPI routes.
```

```
Implement scan_repo.py. Regex for API_KEY and password=. Skip .git and .venv.
```

**OSS PR text (Claude — you edit)**

```
Draft a PR description. Problem: [ ]. Change: [ ]. Tested: [ ].
Under 150 words. I will edit.
```

---

## Anti-patterns

| Bad | Better |
|-----|--------|
| “Build entire app” | One endpoint |
| Paste `.env` | Variable names only |
| “Make it production ready” | 5-item checklist |
| Accept 500-line diff | File-by-file + run |
| Skip ARCHITECTURE.md | Design first |
