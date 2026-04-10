# TODOS — ATL FIFA Navigator v2

## Active

### [ ] Zod schema validation for static match JSON
**What:** Add a Zod schema for the match entries in `public/matches.json`. Validate at build time (e.g., in a `bun run validate` script or as part of `bun run build`). Fail the build if any entry is missing `team_a`, `team_b`, `kickoff_time`, or `match_id`.
**Why:** Prevents silent demo failure where undefined values reach the Claude prompt ("undefined vs undefined kicks off in undefined minutes").
**Where to start:** Add `lib/schemas.ts` with `MatchSchema = z.object({...})`. Run validation in `scripts/validate-matches.ts`. Add to `build` script in `package.json`.
**Depends on:** Static match JSON created (data layer step)

### [ ] Verify Atlanta FIFA 2026 match schedule
**What:** Cross-reference `public/matches.json` against the official schedule at https://atlantafwc26.com/faq/ and https://fifa.com. Confirm all 8 Atlanta match dates, kickoff times, and team group assignments.
**Why:** If dates/times are wrong, the match selector shows bad info on stage. FIFA assignments may shift.
**Where to start:** Check atlantafwc26.com — the official Atlanta host committee site.
**Deadline:** Before April 15.

## Deferred (post-demo)
- Playwright E2E tests (2 core flows: normal + delay injection)
- EN/ES translation (next-intl stubs → fill content)
- Offline-first / service worker
- Group coordination feature
- Approach C: War Room split-screen reasoning panel
