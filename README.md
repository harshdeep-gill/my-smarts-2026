# FY26 SMART Objectives Tracker

Tracks work delivered against FY26 SMART objectives. Updated automatically by the `/smart-log` Claude Code command.

Last initialised: 2026-05-04

---

## Standout PRs

PRs that go beyond routine delivery — large refactors, novel approaches, work that unblocked others, or work shipped significantly faster than expected. Routine WHAT 1 (AI-First) compliance is assumed for every PR; this section is only for the exceptions worth surfacing.

| PR | Title | Site | Why standout | Merged date |
|----|-------|------|--------------|-------------|
| [#1631](https://github.com/Travelopia/leboat/pull/1631), [#1658](https://github.com/Travelopia/leboat/pull/1658) | Search experience (+ follow-up fixes) | Le Boat | New search experience for Le Boat — significant feature work spanning LBWP-2312 and the follow-up fixes in LBWP-2473. Driven with AI skills end-to-end (`.specs` present on the main PR). | 2026-04-27 |
| [#867](https://github.com/Travelopia/moorings/pull/867), [#894](https://github.com/Travelopia/moorings/pull/894) | Google Analytics ID submission across HubSpot forms | Moorings; adopted by other brands including Exodus | Developed reusable approaches to reliably submit Google Analytics IDs to HubSpot across form types, including CTA-based forms (YWEB-816) and forms built with the new HubSpot editor (YWEB-863). Adopted by other brands, including Exodus, extending the impact beyond Moorings. Reported to remain robust in production as of October 2026. | #867: 2025-09-12; #894: 2025-10-24 |
| — | Server-based A/B testing enablement | Moorings; supported TCS | Enabled server-based A/B testing on Moorings and helped other brands, including TCS, enable the same capability, extending the impact through support across brands. | — |

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
| [helix-skills #13](https://github.com/Travelopia/helix-skills/pull/13) | Skill extension + two new *integrated* skills — `helix-a11y` (foundation enforcement gate, co-loaded with every Helix build) and `helix-a11y-interactions` (post-build, detection-gated interaction questionnaire for the design-dependent "it depends" forks). Before this, Helix only verified a11y *after* code existed; there was no planning-time enforcement. Wired into the `helix` router pairing table and atomic-load rule, plus a path-scoped `PreToolUse` hook (`check-a11y-load.sh`) as a write-time backstop so a11y can't be silently skipped — explorations/wireframes stay permissive structurally rather than by special-casing. Also extended `helix-component` / `helix-compose-layout` / `helix-exploration-promote`, expanded `docs/rules.md` into a 22-row enforceable Tier 1+2 foundation checklist with WCAG SC citations, and added the `docs/accessibility.md` steering doc (project bindings, 15-item trap list, per-pattern Helix deviations). Deliberately carries only the *delta* Claude can't infer — the KB is not shipped wholesale. 12 files, +406/−34; hook test suite 20/20. **Repo note:** this landed in `helix-skills`, not `wordpress-team-ai-skills`. **Skill testing:** tested the skill and recorded a before-and-after comparison — [Before skill (Loom)](https://www.loom.com/share/c04af0b0ddaf484680ae8a5319ba71cc) · [After skill (Loom)](https://www.loom.com/share/60e1908267c74282a9ef6650600c3047) · [Slack discussion](https://travelopia-it.slack.com/archives/C05FXSGF6AU/p1784744698184759?thread_ts=1784676557.502289&cid=C05FXSGF6AU). | 2026-06-25 | 2026-07-23 | Phase 2 |
| [#66](https://github.com/Travelopia/wordpress-team-ai-skills/pull/66) | Skill extension — new `travelopia-wp-a11y` + `travelopia-wp-a11y-audit` skills (25 pattern references, WCAG 2.2 AA). Incorporates sub-task PRs [#65](https://github.com/Travelopia/wordpress-team-ai-skills/pull/65) (carousel a11y) and [#63](https://github.com/Travelopia/wordpress-team-ai-skills/pull/63) (forms a11y), merged into main via this PR. Supersedes the earlier draft in PR #32. | 2026-06-02 | 2026-06-03 | Phase 1 |
| [#60](https://github.com/Travelopia/wordpress-team-ai-skills/pull/60) | New skill — `travelopia-wp-jest` (Jest unit-test patterns), wired into the `travelopia-wp` router and set as "Always load" in `travelopia-wp-web-component`, `travelopia-wp-block`, and `travelopia-wp-blade-component` | 2026-05-29 | 2026-06-02 | Phase 1 |

---

## Open Source Package Contributions (WHAT 3 — Phase 2)

| Repo | PR | Description | Date merged |
|------|----|-------------|-------------|
| wordpress-packages | [#139](https://github.com/Travelopia/wordpress-packages/pull/139) | **WP-237 — user role based permalinks menu visibility:** fixed Permalinks menu visibility based on user role in the shared WordPress package used across all our projects, extending the fix across brands through the common package. | 2026-02-04 |

---

## Async Demos / Learnings (WHAT 3 / HOW 1)

| Month | Title / topic | Format | Posted in #wordpress | Link |
|-------|---------------|--------|----------------------|------|
| May 2026 | **axe-core + WCAG 2.1 AA accessibility CLI workflow for Blade components** — combines axe-core scanning (the same engine as Axe DevTools) with an accessibility skill to detect and fix issues automatically. Launches a headless browser against the local WordPress site, scopes the scan to the target component, performs a 13-rule source-code accessibility review, applies pattern-specific rules for carousels, modals, accordions, tabs, forms, and navigation, and fixes issues directly in Blade/JS/SCSS files. | Async video (Loom, 2 parts) + workflow document + Slack post | Yes | [Part 1](https://www.loom.com/share/2f1f2dcda71643c9a9187e75592b3871) · [Part 2](https://www.loom.com/share/79b9c567ae4440faa12d8322144ca5b8) · [Detailed workflow document](https://docs.google.com/document/d/1gpLlGZUqOIiGbe0x1DtlFgAkkgwZqznSKPF_NBqKr8U/edit?usp=sharing) · [Slack discussion](https://travelopia-it.slack.com/archives/C05FXSGF6AU/p1775798292256629) |
| May 2026 | **chrome-devtools-mcp** — gives Claude Code direct access to Chrome DevTools from the terminal to inspect pages, debug, and profile | Async video (Loom) + Slack post | Yes | [Watch demo](https://www.loom.com/share/a9e28e2d15f54c70a78e82d2bce244e9) · [Slack discussion](https://travelopia-it.slack.com/archives/C05FXSGF6AU/p1779770989487769) |
| June 2026 | Basic tutorial for MacBook VoiceOver | Async video (Loom) + Slack post | Yes | [Watch tutorial](https://www.loom.com/share/7b784368423e4211ae8464aad2836145) · [Slack discussion](https://travelopia-it.slack.com/archives/C05FXSGF6AU/p1780288270022289?thread_ts=1779057517.046569&cid=C05FXSGF6AU) |

---

## Proactive Fixes (HOW 2)

| Date | Site | Problem | Fix | PR / Slack link |
|------|------|---------|-----|-----------------|
| 2026-08-07 | Moorings Yacht Ownership; Sunsail Yacht Ownership | WordPress update notification received for version 7.0.3 | Proactively applied the WordPress 7.0.3 update on both sites as soon as the notification was received. | [Moorings Yacht Ownership #459](https://github.com/Travelopia/mooringsyachtownership/pull/459) · [Sunsail Yacht Ownership #194](https://github.com/Travelopia/sunsailyachtownership/pull/194) |
| 2026-08-13 | Moorings Yacht Ownership; Sunsail Yacht Ownership | WordPress update notification received for version 7.0.4 | Proactively applied the WordPress 7.0.4 update on both sites as soon as the notification was received. | [Moorings Yacht Ownership #463](https://github.com/Travelopia/mooringsyachtownership/pull/463) · [Sunsail Yacht Ownership #196](https://github.com/Travelopia/sunsailyachtownership/pull/196) |

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
- [x] Multiple meaningful AI skill improvements (3+) — `wordpress-team-ai-skills` [#60](https://github.com/Travelopia/wordpress-team-ai-skills/pull/60) (jest skill), [#66](https://github.com/Travelopia/wordpress-team-ai-skills/pull/66) (a11y + a11y-audit skills), `helix-skills` [#13](https://github.com/Travelopia/helix-skills/pull/13) (a11y foundation gate + interaction questionnaire) — all merged
- [ ] PMs specifically call out communication as exceptional
- [ ] Mentor other engineers on AI skills without being asked
- [ ] Contribute to WordPress ecosystem (core, plugins, Trac) and raise Travelopia's profile
- [ ] Become the person others go to when they're stuck
