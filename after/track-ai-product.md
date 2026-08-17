# Track — AI Product (LLM Apps) (4 weeks)

Optional track. RAG, prompts, small agents — build **useful**, not hype. **Local or free-tier only.** You did **not** build RAG in the 2-day workshop; start small here.

Handbook: [how-editors-work.md](../how-editors-work.md) · [build-context.md](build-context.md) · [prompting.md](../prompting.md) · [marketplace.md](../marketplace.md)

---

## Outcomes

- A Q&A tool over **your** documents (keyword search is enough for week 1)
- Know when RAG vs a plain prompt is enough
- Honest about limitations (hallucination, cost, secrets)

---

## Module 1 — Grounded Q&A without a vector DB (Week 2)

**Learn:** Split markdown by headers; keyword search; paste top chunks into Claude/ChatGPT with "answer only from these chunks". Same shape as Cursor `@`: retrieve, then ask. Ladder (keyword → Chroma → optional MCP): [build-context.md](build-context.md).

**Build:** `rag_query.py` over a `docs/` folder of your notes. If it can't find a chunk, it must say "I don't know".

---

## Module 2 — Structured outputs (Week 2)

**Learn:** Pydantic models for JSON from an LLM; retry on validation fail.

**Build:** `POST /summarize` → `{ summary: str, bullets: list[str] }` on your FastAPI app **or** a CLI.

---

## Module 3 — Mini project (Week 3)

Pick one:

| Project | Users |
|---------|-------|
| **Course Q&A** | Your batch — index syllabi |
| **Code explainer** | Paste snippet → structured explanation |
| **Meeting notes** | Upload txt → action items |

Local demo is enough. Never commit API keys.

---

## Module 4 — Agent lite (Week 4)

**Learn:** Tool loop with a max iteration limit; human approval for anything destructive. Optional: expose `search_docs` as MCP so Cursor can retrieve — [build-context.md](build-context.md) Stage 3.

**Build:** CLI: question → search `docs/` → draft answer → save to `answers/`. ~100 lines is fine. Vectors only if keyword search already works and still misses paraphrases.

---

## Hackathon ideas

- Campus FAQ bot with citations
- Resume ↔ JD gap analyzer (privacy-safe, local)
- Lab-manual assistant that refuses when sources are missing

---

## OSS path

1. [ollama/ollama](https://github.com/ollama/ollama) — local models
2. [chroma-core/chroma](https://github.com/chroma-core/chroma) — if you outgrow keyword search
3. [langchain-ai/langchain](https://github.com/langchain-ai/langchain) — **read**, don't over-depend

Readings & writing: [follow-up.md](follow-up.md) · Repos: [oss.md](oss.md)

---

## Interview talking point

> "I built a notes Q&A tool that retrieves chunks first and answers only from those chunks. I can explain hallucination, why I started without a vector database, and how I keep keys out of Git."
