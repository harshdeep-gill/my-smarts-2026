# FY26 SMART Objectives Tracker

Tracks work delivered against FY26 SMART objectives. Updated automatically by the `/smart-log` Claude Code command.

Last initialised: 2026-05-04

---

## Currently Working On

| Ticket | Title | Site | Started | Status | Notes |
|--------|-------|------|---------|--------|-------|
| [WP-239 / PR #156](https://github.com/Travelopia/wordpress-packages/pull/156) | Hide "Delete Site" menu under Tools | wordpress-packages (network-wide) | 2026-08-10 | In review | Removes WordPress's `ms-delete-site.php` entry from the Tools menu on every multisite sub-site — it was showing to any user with `manage_options`, and sites are only ever deleted from Network Admin. Shipped in `travelopia-core`, so it lands across every brand in the group rather than one site. Built TDD via `/travelopia-wp-php`: added `.tests/php/tests/test-core.php` (the package had no test coverage at all before this), 3 new tests, suite green at 149 tests / 355 assertions. PR flags for reviewers that this is hide-only — the URL stays reachable — with a `map_meta_cap` follow-up offered if the team wants deletion actually blocked. |
| [Skill PR #13](https://github.com/Travelopia/wordpress-team-ai-skills/pull/13) | Add frontend-context skill (SCSS, Blade, web components) | wordpress-team-ai-skills | 2026-04-08 | In progress (draft PR) | Skill that loads the entire front-end context into Claude — design system files, external libraries (web-components), and key conventions like the `<x-section>`, `<x-image>`, `<x-escape>` Blade components. Aimed at making front-end skill outputs consistent across the team. |
| [WP-144 / PR #117](https://github.com/Travelopia/web-components/pull/117) | Add scroll feature to tp-slider | web-components | 2025-06-24 | Blocked | Long-pending. Paired with brand devs to test across projects; regressions confirmed on Quark Expeditions (view cabin prices carousel on search page) and Enchanting Travels ([sample itinerary carousel](https://www.enchantingtravels.com/luxury-travel/kenya-egypt-safari-human-history/)). Two unblock proposals: (1) ship as `tp-slider` v2 so only new implementations opt in, or (2) introduce a `tp-slider` v0 and migrate the failing brands to it while the rest stay on the existing `tp-slider` and inherit the change automatically. Awaiting decision. |

---

## Standout PRs

PRs that go beyond routine delivery — large refactors, novel approaches, work that unblocked others, or work shipped significantly faster than expected. Routine WHAT 1 (AI-First) compliance is assumed for every PR; this section is only for the exceptions worth surfacing.

| PR | Title | Site | Why standout | Merged date |
|----|-------|------|--------------|-------------|
| [#1631](https://github.com/Travelopia/leboat/pull/1631), [#1658](https://github.com/Travelopia/leboat/pull/1658) | Search experience (+ follow-up fixes) | Le Boat | New search experience for Le Boat — significant feature work spanning LBWP-2312 and the follow-up fixes in LBWP-2473. Driven with AI skills end-to-end (`.specs` present on the main PR). | 2026-04-27 |

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
| March 2026 | Sunsail | Long-pending block architecture migration — entire block library (466 files) moved from legacy functional `index.php` to new class-based architecture. Approach: built two local AI skills (one for block refactor, one for architecture conversion), batched migration into 5-block reviews for safer testing, migrated and tested every block end-to-end, deployed with zero issues. | [YWEB-1193](https://tuispecialist.atlassian.net/browse/YWEB-1193) | [#544](https://github.com/Travelopia/sunsail/pull/544) | Unknown |

---

## AI Skills Package Contributions (WHAT 3)

| PR | Type | Date submitted | Date merged | Phase |
|----|------|----------------|-------------|-------|
| [#66](https://github.com/Travelopia/wordpress-team-ai-skills/pull/66) | Skill extension — new `travelopia-wp-a11y` + `travelopia-wp-a11y-audit` skills (25 pattern references, WCAG 2.2 AA). Incorporates sub-task PRs [#65](https://github.com/Travelopia/wordpress-team-ai-skills/pull/65) (carousel a11y) and [#63](https://github.com/Travelopia/wordpress-team-ai-skills/pull/63) (forms a11y), merged into main via this PR. Supersedes the earlier draft in PR #32. | 2026-06-02 | 2026-06-03 | Phase 1 |
| [#60](https://github.com/Travelopia/wordpress-team-ai-skills/pull/60) | New skill — `travelopia-wp-jest` (Jest unit-test patterns), wired into the `travelopia-wp` router and set as "Always load" in `travelopia-wp-web-component`, `travelopia-wp-block`, and `travelopia-wp-blade-component` | 2026-05-29 | 2026-06-02 | Phase 1 |

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
