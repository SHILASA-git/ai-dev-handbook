# AI Dev Handbook

Student handbook for the **2-day AI-assisted development workshop** (Cursor, Copilot, Claude, ChatGPT, Gemini). Use it **in the room** and on later projects.

Labs and timing live in the workshop repo: [`ai-workshop`](../ai-workshop/). This repo is **how to use the tools**.

**AI multiplies you — it does not replace thinking.** Design first. Read diffs. Run the code. Never commit secrets.

---

## Open these three

| When | File |
|------|------|
| Always | **[START.md](START.md)** — which tool when + 5 rules |
| In the room | **[workshop-map.md](workshop-map.md)** — this block → this page |
| Copy-paste | **[prompts.md](prompts.md)** — prompts by job |
| Safety | **[what-not-to-do.md](what-not-to-do.md)** — secrets, Agent, OSS, assignments |

---

## During the workshop

| Need | Open |
|------|------|
| Prompting (Day 1 morning) | [prompting.md](prompting.md) |
| AI/ML history (refresh) | [ai-history.md](ai-history.md) |
| How the editor packs context | [how-editors-work.md](how-editors-work.md) |
| A specific tool | [tools/](tools/) — Cursor, Claude, ChatGPT, Copilot, Gemini |
| Marketplace / Skills / MCP | [marketplace.md](marketplace.md) |
| What **not** to do | [what-not-to-do.md](what-not-to-do.md) |
| Architecture | [jobs/architecture.md](jobs/architecture.md) |
| Coding / debug | [jobs/coding.md](jobs/coding.md) · [jobs/debugging.md](jobs/debugging.md) |

---

## After the workshop (any project)

1. Copy [templates/](templates/) into the new repo (ARCHITECTURE, LEARNING, Cursor rules + skill).
2. Pick the **job** you are doing — not a tool first:

| Job | File |
|-----|------|
| Design | [jobs/architecture.md](jobs/architecture.md) |
| Implement | [jobs/coding.md](jobs/coding.md) |
| Stuck | [jobs/debugging.md](jobs/debugging.md) |
| Compare / review | [jobs/analyzing.md](jobs/analyzing.md) |
| Learn a concept | [jobs/researching.md](jobs/researching.md) |

3. Pick **one** 4-week track: [after/README.md](after/README.md).

---

## Repo map

```
START.md            ← 2-minute card (project this)
workshop-map.md     ← Day 1 / Day 2 index
prompting.md        ← prompt engineering
ai-history.md       ← regression → nets → GPTs → agents
how-editors-work.md ← context window, Rules, Skills, MCP, RAG
marketplace.md      ← Rules, Skills, Marketplace, MCP — safely
what-not-to-do.md   ← secrets, Agent, OSS, assignments — strict don'ts
tools/              ← one page per tool
jobs/               ← coding, research, analyze, debug, architecture
prompts.md          ← copy-paste library
templates/          ← drop into any later repo
after/              ← 4-week tracks + OSS list
```

---

## Clone both (local)

```bash
# sibling folders
ls ../ai-workshop/README.md
ls ./START.md
```

Workshop labs: [ai-workshop/day1](../ai-workshop/day1/) · [ai-workshop/day2](../ai-workshop/day2/)
