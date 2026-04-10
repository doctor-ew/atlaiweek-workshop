# Prompt: MY BUILD SESSION
> Paste this at the start of a fresh Claude Code session in this directory.
> Run with: claude --add-dir /Users/doctorew/shuttlebay/doctorews-laboratory/_Workshops_

---

Read these files to get full context before doing anything:
- `~/.claude/projects/-Users-doctorew/memory/MEMORY.md` — my preferences and history
- `../ATL-FIFA-Navigator/docs/PLAN.md` — the full project plan, match schedule, tech decisions

## Context

I am building the **ATL FIFA Navigator v2** — a Next.js fan navigation app for FIFA World Cup 2026 Atlanta matches. I'm presenting this at Atlanta AI Week (April 20-22, 2026) as a live build demo. I have ~3 weeks.

The app helps fans answer: *"How do I get to the game from where I am right now?"* using real MARTA bus + rail APIs (already working in a prior repo), the confirmed match schedule, and Claude-powered routing assistance.

## Your job

We are scaffolding and building the actual app here in `AtlantaAIWeek/`.

Before writing a line of code:
1. Run `/office-hours` using gstack at `../gstack/` to validate the concept and surface any gaps
2. Then run `/plan-eng-review` to lock the architecture

Tech stack: Next.js 15 (App Router), bun, Tailwind, shadcn/ui, next-intl (EN/ES), Vercel deploy. MARTA APIs are REST — I'll provide keys when needed.

Use `/effort high` before any architecture decisions. Use `/simplify` after generating any component. Use gstack's `/review` before we consider anything "done."

Start with `/office-hours`.
