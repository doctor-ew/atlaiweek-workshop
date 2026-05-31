# PRD: Leave By Badge

**Paste this at the start of the live demo session.**

---

## What we're building

A "Leave by HH:MM PM" badge on each zone row in the `ZonePicker` component.

Fans see at a glance whether they have time to finish dinner or need to leave
right now — without doing any math. The feature is simple. Watch the pipeline.

---

## Context

- App: `atl-fifa-navigator-v2` — Next.js 16 App Router, bun, Tailwind, shadcn/ui
- Sidebar already has: `MatchSelector`, `ZonePicker`, `MartaStatusCard`, `RecommendationArea`
- Match data: `src/lib/matches.ts` — exposes `getMatches()`, `getMatch(id)`, `minutesUntilKickoff(match)`
- Selected match flows into `ZonePicker` via props from `Sidebar.tsx`
- Design tokens: `text-amber-400` accent, `bg-gray-800/80` panels, `text-gray-300` body

---

## The feature

**File to change:** `src/components/ZonePicker.tsx`

Add a leave-by badge beneath each zone name. No new component file needed.

**Time math:**
```
leave_by = kickoff_time_ET − ZONE_TRAVEL_MINUTES[zone] − 15 min buffer
```

**Static travel time map (hardcoded — no API calls):**

| Zone | Minutes | Constant |
|------|---------|----------|
| Downtown (Five Points / Centennial Park) | 10 | `ZONE_TRAVEL_MINUTES.downtown` |
| Midtown (Arts Center / Peachtree) | 15 | `ZONE_TRAVEL_MINUTES.midtown` |
| Airport (College Park / MARTA) | 35 | `ZONE_TRAVEL_MINUTES.airport` |
| Decatur (Blue Line) | 30 | `ZONE_TRAVEL_MINUTES.decatur` |
| Dunwoody (Red Line) | 45 | `ZONE_TRAVEL_MINUTES.dunwoody` |

**Badge states:**

- **Neutral** (`text-gray-400`) — more than 30 min until leave-by time
- **Urgent** (`text-amber-400`) — ≤ 30 min remaining
- **Now** (`text-red-400`) — past leave-by time → reads "Leave now — you may be late"
- **Hidden** — no match selected

---

## What this is NOT

- No live routing or traffic-adjusted estimates
- No countdown timer (static label, not ticking)
- No new API calls
- No new component file

---

## Acceptance criteria

1. Every zone row shows a "Leave by HH:MM AM/PM ET" label when a match is selected
2. Leave-by time = `kickoff − travel_minutes[zone] − 15 min`, displayed in 12-hour ET
3. Badge is neutral when > 30 min away, amber when ≤ 30 min, red + "Leave now" when past
4. No badge rendered when no match is selected
5. `minutesUntilKickoff()` from `src/lib/matches.ts` anchors the time math
6. No `any` types
7. No layout shift in the `w-80` sidebar
