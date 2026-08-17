# Track — Python Automation (4 weeks)

Extend the Day 2 automation lab or start fresh. **Python scripts first** — not CI/CD pipelines.

Handbook: [jobs/coding.md](../jobs/coding.md) · [prompts.md](../prompts.md)

---

## Outcomes

After 4 weeks you can:

- Automate file, data, and report tasks with Python
- Use `pathlib`, `csv`, `schedule`, and basic API polling
- Point to 1–2 automation repos on a resume

---

## Module 1 — File & folder automation (Week 2)

**Design first:** Sketch input → script → output in ARCHITECTURE.md.

**Learn:** `pathlib`, `shutil`, `glob`; idempotent scripts; `argparse --dry-run`

**Build:** `scripts/organize_downloads.py` + `scripts/backup_notes.py` (copy changed `.md` files)

**AI prompt:**

```
Add --dry-run flag to my organize script. Print planned moves without executing.
Refuse to run if the source path is my home Downloads folder unless --i-mean-it.
```

---

## Module 2 — Data & report automation (Week 2)

**Learn:** `csv`, `json`, `httpx` to poll an API; optional `schedule`

**Build:** Read `scores.csv` → `weekly_report.txt`

**Stretch:** `watchdog` — run organizer when a new file arrives

---

## Module 3 — Mini project (Week 3)

Pick one:

| Project | Description |
|---------|-------------|
| **Lab submission organizer** | Sort files by roll-number pattern |
| **Log summarizer** | Parse app log, count ERROR lines |
| **Form filler** | Playwright script for **your own** test form only |
| **Attendance CSV pipeline** | Merge sheets → one summary report |

---

## Module 4 — Hackathon ideas (Automation)

- Auto-rename and validate submission folders
- Scheduled backup of project docs to a second folder
- CSV → summary pipeline

---

## Optional later (not Week 1–2)

- GitHub Actions — only after you are comfortable with Python scripts
- n8n / Airflow — visual or workflow orchestration

---

## OSS path

1. [dbader/schedule](https://github.com/dbader/schedule) — docs PRs
2. [PrefectHQ/prefect](https://github.com/PrefectHQ/prefect) — `good first issue`
3. [microsoft/playwright-python](https://github.com/microsoft/playwright-python)

Readings & writing: [follow-up.md](follow-up.md) · Repos: [oss.md](oss.md)

---

## Interview talking point

> "I wrote Python scripts to organize lab files and generate CSV reports — pathlib, argparse, and a dry-run mode. I can explain what the script will do before it moves anything."
