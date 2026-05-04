# FY26 SMART Objectives Tracker

Tracks work delivered against FY26 SMART objectives. Updated automatically by the `/smart-log` Claude Code command.

Last initialised: 2026-05-04

---

## Currently Working On

| Ticket | Title | Site | Started | Status | Notes |
|--------|-------|------|---------|--------|-------|
| [Skill PR #32](https://github.com/Travelopia/wordpress-team-ai-skills/pull/32) | Add a11y skill | wordpress-team-ai-skills | 2026-04-23 | In progress (draft PR) | Completing accessibility course (~50% done) and updating the skill in parallel. Reference notes: [Google Doc](https://docs.google.com/document/d/1xI8efpsa15WLlZwq3vQ_EHSTbosaNjdcLDq3JngdVgc/edit?usp=sharing) |

---

## PR Log (WHAT 1 — AI-First Delivery)

| PR | Title | Ticket | AI skill used | Start date | Merged date | Days taken | `.specs` present |
|----|-------|--------|---------------|------------|-------------|------------|------------------|
| [#1631](https://github.com/Travelopia/leboat/pull/1631) | Search experience | LBWP-2312 | Yes | 2026-04-16 | 2026-04-23 | 7 | Yes |
| [#1636](https://github.com/Travelopia/leboat/pull/1636) | Boat and bases API | LBWP-2453 | Yes | 2026-04-17 | 2026-04-21 | 4 | Yes |
| [#1658](https://github.com/Travelopia/leboat/pull/1658) | Search experience fixes | LBWP-2473 | No | 2026-04-27 | 2026-04-27 | 0 | No |
| [#547](https://github.com/Travelopia/sunsail/pull/547) | Script to migrate old slug | [YWEB-1147](https://tuispecialist.atlassian.net/browse/YWEB-1147) | No | 2026-04-02 | 2026-04-08 | 6 | No |
| [#557](https://github.com/Travelopia/sunsail/pull/557) | Add itinerary details component for individual pages | [YWEB-1255](https://tuispecialist.atlassian.net/browse/YWEB-1255) | No | 2026-04-09 | 2026-04-14 | 5 | No |
| [#558](https://github.com/Travelopia/sunsail/pull/558) | Add quote CTA on itinerary pages | [YWEB-1256](https://tuispecialist.atlassian.net/browse/YWEB-1256) | No | 2026-04-09 | 2026-04-14 | 5 | No |
| [#544](https://github.com/Travelopia/sunsail/pull/544) | New block architecture | [YWEB-1193](https://tuispecialist.atlassian.net/browse/YWEB-1193) | Yes (local skills) | 2026-03-31 | 2026-03-31 | 0 | No |

---

## Health Check Quick-Fixes (WHAT 2 — Phase 1)

| Fortnight | Site | Issue | Jira ticket | PR | Slack post | Date resolved | Within 5 days |
|-----------|------|-------|-------------|----|------------|---------------|---------------|
| 13–26 Apr 2026 | Moorings Yacht Ownership | Backend error fix | [YWEB-1266](https://tuispecialist.atlassian.net/browse/YWEB-1266) | [#433](https://github.com/Travelopia/mooringsyachtownership/pull/433) | No | 2026-04-14 | — |
| 13–26 Apr 2026 | Moorings Yacht Ownership | Frontend error fix | [YWEB-1262](https://tuispecialist.atlassian.net/browse/YWEB-1262) | [#432](https://github.com/Travelopia/mooringsyachtownership/pull/432) | No | 2026-04-14 | — |
| 13–26 Apr 2026 | Sunsail Yacht Ownership | Frontend error fix | [YWEB-1267](https://tuispecialist.atlassian.net/browse/YWEB-1267) | [#164](https://github.com/Travelopia/sunsailyachtownership/pull/164) | No | 2026-04-23 | — |

---

## Tech Debt Items (WHAT 2 — Phase 2)

| Month | Site | Issue | Jira ticket | PR | Tagged "Tech Debt" |
|-------|------|-------|-------------|----|--------------------|
| March 2026 | Sunsail | Long-pending block architecture migration — entire block library (466 files) moved from legacy functional `index.php` to new class-based architecture | [YWEB-1193](https://tuispecialist.atlassian.net/browse/YWEB-1193) | [#544](https://github.com/Travelopia/sunsail/pull/544) | Unknown |

---

## AI Skills Package Contributions (WHAT 3)

| PR | Type | Date submitted | Date merged | Phase |
|----|------|----------------|-------------|-------|

---

## Open Source Package Contributions (WHAT 3 — Phase 2)

| Repo | PR | Description | Date merged |
|------|----|-------------|-------------|

---

## Async Demos / Learnings (WHAT 3 / HOW 1)

| Month | Title / topic | Format | Posted in #wordpress | Link |
|-------|---------------|--------|----------------------|------|
| May 2026 | Axe-core + WCAG 2.1 AA accessibility CLI workflow for Blade components | Async video (Loom, 2 parts) + Slack post | Yes (#wp-engineers) | [Part 1](https://www.loom.com/share/2f1f2dcda71643c9a9187e75592b3871) · [Part 2](https://www.loom.com/share/79b9c567ae4440faa12d8322144ca5b8) |

---

## Proactive Fixes (HOW 2)

| Date | Site | Problem | Fix | PR / Slack link |
|------|------|---------|-----|-----------------|
| 2026-03-31 | Sunsail | Long-pending tech debt — every block on legacy functional architecture, blocking future work and harder to maintain | Built two local AI skills (block refactor + architecture conversion), batched migration into 5-block reviews for safer testing, migrated all blocks, tested end-to-end, deployed with zero issues | [#544](https://github.com/Travelopia/sunsail/pull/544) |

---

## PM / Stakeholder Responsiveness (HOW 1)

| Date | PM / stakeholder | Question | Response time | Outcome |
|------|------------------|----------|---------------|---------|
| 2026-04-02 | Sunsail PM | How to give itineraries their own pages with a refreshed component design while keeping editor effort to zero | Same-day | Brainstormed multiple approaches and shipped a seamless solution: slug-migration CLI ([#547](https://github.com/Travelopia/sunsail/pull/547)), new itinerary-details component for single pages ([#557](https://github.com/Travelopia/sunsail/pull/557)), Build My Quote CTA on single itinerary ([#558](https://github.com/Travelopia/sunsail/pull/558)), and existing itineraries component redesigned as accordion ([#561](https://github.com/Travelopia/sunsail/pull/561)) — no editor rework required |

---

## Escalations (HOW 1)

| Date | Issue | Why escalated | Resolution |
|------|-------|---------------|------------|

---

## Exceeds Expectations Checklist

- [ ] Ship significantly faster than the 2x target
- [ ] Proactively find and fix problems nobody else noticed
- [ ] Async demos so good that other teams reference them
- [ ] Multiple meaningful AI skill improvements (3+)
- [ ] PMs specifically call out communication as exceptional
- [ ] Mentor other engineers on AI skills without being asked
- [ ] Contribute to WordPress ecosystem (core, plugins, Trac) and raise Travelopia's profile
- [ ] Become the person others go to when they're stuck
