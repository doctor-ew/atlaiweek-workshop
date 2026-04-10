# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Directory Is

Workshop assets for the Atlanta AI Week (April 20–22, 2026) talk: *"From Prompt to Production: Building a FIFA Fan App with Claude Code."*

- `PROMPT-BUILD.md` — paste at the start of any build session
- `PROMPT-SHOW.md` — paste at the start of the live on-stage session
- The actual Next.js app lives in `../ATL-FIFA-Navigator/atl-fifa-navigator-v2/`

## Session Setup

Both session prompts require running with the `_Workshops_` directory added:

```bash
claude --add-dir /Users/doctorew/shuttlebay/doctorews-laboratory/_Workshops_
```

## App: ATL FIFA Navigator v2

**Core story:** Help FIFA fans answer *"How do I get to the game from where I am right now?"* using real MARTA APIs, static match schedule JSON, and Claude-powered routing.

**Stack:** Next.js 15 (App Router) · bun · Tailwind · shadcn/ui · next-intl (EN/ES) · Vercel

**Initialize the app:**

```bash
cd ../ATL-FIFA-Navigator
mkdir atl-fifa-navigator-v2 && cd atl-fifa-navigator-v2
bun create next-app@latest . --typescript --tailwind --app --src-dir --import-alias "@/*"
```

**Wire in gstack:**

```bash
mkdir -p .claude/skills
cp -Rf ../../gstack .claude/skills/gstack
cd .claude/skills/gstack && ./setup
```

## gstack Workflow (The Talk's Meta-Story)

gstack lives at `../gstack/`. Run these commands in order before building:

| Command | When | Purpose |
|---------|------|---------|
| `/office-hours` | Before any code | CEO role — validates concept, surfaces gaps |
| `/plan-eng-review` | After PRD, before scaffold | Architect locks the tech approach |
| `/effort high` | Before architecture decisions | More deliberate reasoning |
| `/simplify` | After generating a component | Self-review — cuts what doesn't need to be there |
| `/design-review` | After first UI render | Catches AI-generated visual slop |
| `/review` | Before anything is "done" | Code review pass |
| `/qa` | On staging URL | Opens a real browser and tests the app |
| `/ship` | Final step | PR created + Vercel deployed |

## Full Project Plan

The authoritative plan, tech decisions, match schedule (8 Atlanta games), and 3-week timeline are in:

```
../ATL-FIFA-Navigator/docs/PLAN.md
```

Read this before making any architectural or scope decisions.

## Live Demo Feature (Built On Stage)

**Real-time MARTA status card** — shows current train/bus delays for lines serving Mercedes-Benz Stadium. The live build sequence is: prompt → component → `/simplify` → `/design-review` → `/ship`.

## Skill routing

When the user's request matches an available skill, ALWAYS invoke it using the Skill
tool as your FIRST action. Do NOT answer directly, do NOT use other tools first.
The skill has specialized workflows that produce better results than ad-hoc answers.

Key routing rules:
- Product ideas, "is this worth building", brainstorming → invoke office-hours
- Bugs, errors, "why is this broken", 500 errors → invoke investigate
- Ship, deploy, push, create PR → invoke ship
- QA, test the site, find bugs → invoke qa
- Code review, check my diff → invoke review
- Update docs after shipping → invoke document-release
- Weekly retro → invoke retro
- Design system, brand → invoke design-consultation
- Visual audit, design polish → invoke design-review
- Architecture review → invoke plan-eng-review

## Key Context

- MARTA bus + rail REST APIs are already integrated in a prior repo — port them, don't rewrite
- Match schedule is static JSON for now (8 confirmed Atlanta games, June–July 2026)
- All at Mercedes-Benz Stadium
- i18n required (EN/ES) via next-intl
- Parking API has no reliable source — skip, document as future
