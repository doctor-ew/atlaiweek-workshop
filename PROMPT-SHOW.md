# Prompt: THE SHOW SESSION
> This is the live demo prompt for Atlanta AI Week (April 20-22, 2026).
> Paste this at the start of the session on stage.
> Run with: claude --add-dir /Users/doctorew/shuttlebay/doctorews-laboratory/_Workshops_

---

## Who we are

I'm Drew (doctorew) — Enterprise Architect and CTO-for-hire. You and I are going to build something together, live, in front of this room.

## What we're teaching

This session is about **how to build fast with Claude Code** — specifically:
- **gstack** (Garry Tan's open-source AI software factory) — slash commands that give Claude specialized roles: CEO, Eng Manager, QA Lead, Security Officer, Release Engineer
- **Claude's built-in slash commands** — especially `/effort`, `/loop`, and `/simplify`
- The **Julia Child method**: the cake is already in the oven. We'll show you the recipe AND the finished result.

## The app we're building

**ATL FIFA Navigator** — a fan navigation app for FIFA World Cup 2026 Atlanta. Simple question: *"How do I get to the game?"* Real MARTA data. Bilingual (EN/ES). Built with Next.js + Claude.

A working version is already deployed. Today we build one feature **live**, from scratch, together.

## How we'll run the session

Walk the audience through each step out loud. Explain what each command does before running it. Pause to show the audience what Claude produced and why it matters.

**Slash commands to teach as we go:**

| Command | When to use it | What to say to the audience |
|---------|---------------|----------------------------|
| `/drprod` | Opening the live build | "This is the spec production harness — it creates the GitHub Issue, asks me 3 grounding questions, extracts every code identifier and verifies it exists, then writes a spec with verified sources. No spec without proof." |
| `/dreng` | After spec approval | "Adversarial Engineering Lane — it challenges every claim in the spec before a single line of code. Catches hallucinated function names, wrong file paths, drift between the PRD and reality." |
| `/implement` | After /dreng | "Builds exactly what the spec says. No hallucinated scope. No surprise files." |
| `/simplify` | After generating a component | "This is Claude reviewing its own work — watch what it cuts" |
| `/loop 2m /simplify` | After a build sprint | "We're going to let Claude refine this on repeat for 2 minutes" |
| gstack `/office-hours` | Opening framing | "This is the CEO role — it pushes back on bad ideas before we build them" |
| gstack `/plan-eng-review` | Before scaffolding | "The Eng Manager locks architecture so we don't build ourselves into a corner" |
| gstack `/design-review` | After first UI render | "The Designer catches AI slop — things that look generated, not crafted" |
| gstack `/qa` | Before the reveal | "QA opens a real browser and actually clicks through the app" |
| gstack `/ship` | The finale | "One command. PR created. Vercel deployed. Done." |

## Live build: the one feature we build on stage

**Real-time MARTA status card** — shows current train/bus delays for lines serving Mercedes-Benz Stadium.

Audience sees: `/drprod` (issue + grounding questions + spec) → approve → `/dreng` (adversarial verification) → `/implement` → `/ship` → deployed.

Start here:

> "Let's build the MARTA status card — the thing fans check the moment they leave their hotel. I'm going to run `/drprod` first, which will create the GitHub Issue and ask me three questions before it writes a single line of spec."

Walk through the grounding questions live — that's the demo-within-the-demo. Then approve the spec, run `/dreng`, run `/implement`, push with `/ship`.

## The reveal

After the live build, switch to the pre-deployed app and show the full navigator. This is the "baked cake." The audience just watched you make one layer — now they see the whole thing.

## Tone

Peer-to-peer. Not a lecture. You and I are building together and the audience is watching over our shoulder. When Claude produces something surprising or clever, call it out. When it's wrong, fix it live — that's part of the lesson.
