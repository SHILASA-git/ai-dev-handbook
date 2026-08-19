# Marketplace, Skills, Rules, MCP — use safely

Cursor can load **extra instructions and tools**. That is useful after the workshop. Treat them like untrusted code until you have read them.

This page is **not** a lab. Skim on Day 2 AppSec; copy the templates into later projects.

---

## Four things (don't mix them up)

| Thing | What it is | Where |
|-------|------------|--------|
| **Rules** | Always-on project conventions | `.cursor/rules/*.mdc` |
| **Skills** | Playbooks for a *kind* of task (`SKILL.md`) | `.cursor/skills/name/` or Cursor Marketplace |
| **Marketplace / plugins** | Extra IDE or agent capabilities | Cursor Settings → Marketplace |
| **MCP** | Lets the agent talk to GitHub, browsers, DBs, … | Cursor Settings → MCP |

**Start with Rules.** Add one Skill. Leave Marketplace and MCP off until you need them.

---

## Rules (do this on every project)

Copy [templates/cursor/rules/python-student.mdc](templates/cursor/rules/python-student.mdc) to `.cursor/rules/` in **your** repo.

Rules should be short: stack, “no new deps without asking”, “no secrets”, “match ARCHITECTURE.md”. Long novels get ignored.

---

## Skills

A skill is a markdown playbook the agent can load. Copy [templates/cursor/skills/review-architecture/](templates/cursor/skills/review-architecture/) into `.cursor/skills/` to review code against `ARCHITECTURE.md`.

**Before you enable a skill from Marketplace or GitHub:**

1. Open `SKILL.md` and read it.
2. Check whether it asks the agent to run shell commands or hit the network.
3. Prefer project skills you committed over random personal skills you forgot about.
4. Disable anything you are not using this week.

Treat a skill like a PR from a stranger.

---

## Marketplace / plugins

- Prefer **official or verified** listings.
- Install **one** plugin, try it, then decide.
- If it wants file, terminal, or network access — assume it can see your repo.
- Remove plugins you are not using. Fewer moving parts.

You do not need Marketplace to finish the 2-day workshop.

---

## MCP (keep off by default)

MCP servers give the agent extra tools (e.g. GitHub). The model **calls a tool**; the **result text** is packed into the same context window — not extra memory. How that pack works: [how-editors-work.md](how-editors-work.md). Build a tiny `search_docs` later: [after/build-context.md](after/build-context.md).

Useful later. Risky if you don't know the server.

| Do | Don't |
|----|-------|
| Add one server you understand | Paste API tokens into a random MCP config |
| Disable unused servers | Let a server run shell “to be helpful” |
| Approve Agent commands yourself | Auto-run on an unknown MCP |

---

## Agent safety (same as AppSec lab)

1. Never paste `.env`, passwords, or college credentials into chat, a skill, or MCP.
2. **You** approve terminal commands. Reject `rm`, git force, or anything you don't understand.
3. Don't auto-run unknown skills.
4. Don't open mass AI-generated OSS PRs.

Secrets and Git: workshop [AppSec lab](../ai-workshop/day2/03-appsec-lab.md). Full don'ts: [what-not-to-do.md](what-not-to-do.md). After: [after/track-security.md](after/track-security.md).
