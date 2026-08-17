# Track — Full-Stack (4 weeks)

Extend the Day 1 Task Tracker (FastAPI + HTML/JS). **Stay local** unless you later choose to deploy on your own.

Handbook: [jobs/architecture.md](../jobs/architecture.md) · [jobs/coding.md](../jobs/coding.md) · [templates/](../templates/)

---

## Outcomes

After 4 weeks you can:

- Explain UI → API → store as a design, not a lucky demo
- Add a feature across backend and frontend without breaking the contract
- Point to a GitHub repo with README, architecture, and a working UI

---

## Module 1 — Persistence without a cloud (Week 2)

**Design first:** In-memory vs file vs SQLite — pick one in `ARCHITECTURE.md`.

**Learn:**

- JSON file store **or** SQLite (`sqlite3` stdlib)
- Keep routes thin; storage in a class

**Build:** Tasks survive restart.

**AI prompt:**

```
@ARCHITECTURE.md @store.py
Replace in-memory list with SQLite using stdlib sqlite3.
Keep the same API contract. No new dependencies.
```

---

## Module 2 — UI that matches the contract (Week 2)

**Learn:**

- Loading and error states
- Don't trust the network
- CORS only as wide as local demo needs

**Build:** Toggle done, filter, empty state. Optional: very small CSS polish (no framework required).

---

## Module 3 — Mini project (Week 3)

Pick one:

| Project | Description |
|---------|-------------|
| **Notes app** | Same architecture, different resource |
| **Auth stub** | API key header on mutating routes (document limits) |
| **Tests** | 5 pytest cases with TestClient |

---

## Module 4 — Interview / hackathon (Week 4)

- Draw scale-up: PostgreSQL, auth, load balancer — **as a diagram**, not as homework to provision
- README: problem, architecture link, setup, what AI did

---

## OSS path

1. [fastapi/fastapi](https://github.com/fastapi/fastapi) — docs / `good first issue`
2. [encode/httpx](https://github.com/encode/httpx)
3. [tiangolo/sqlmodel](https://github.com/fastapi/sqlmodel) — later, if you add a DB

Readings & writing: [follow-up.md](follow-up.md) · Repos: [oss.md](oss.md)

---

## Interview talking point

> "I designed the API contract first, built FastAPI + a simple UI, then replaced in-memory storage with SQLite without changing the routes. I can explain CORS, 404/422, and what I'd add for real auth."
