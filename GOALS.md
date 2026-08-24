# FY26 Goals — Checklist & Progress

Full statement of the FY26 objectives, with a progress summary counted from the evidence logged in [README.md](README.md).

**As of:** 2026-08-24 · **Current phase:** Phase 2 (July – September 2026), month 2 of 3

---

## Objectives Progress

Counts are derived only from entries present in `README.md`. Anything with no logged evidence is counted as not done — the tracker is the source of truth.

| # | Objective | Phase | Target | Done | Left | Status |
|---|-----------|-------|--------|------|------|--------|
| WHAT 1.2 | Automated test coverage on every PR | P1 + P2 | 100% of PRs | — | — | ✅ On track — no QA rejections logged |
| WHAT 1.6 | Zero QA rejections for missing tests | P2 | 0 rejections | — | — | ✅ On track — none logged |
| WHAT 2.1 | Health check quick-fixes, 2 per fortnight | P1 | 12 (6 fortnights) | 3 | 9 | ❌ Behind — only the 13–26 Apr fortnight covered |
| WHAT 2.2 | Slack summary posted when quick-fix PR raised | P1 | 3 of 3 fixes | 0 | 3 | ❌ Missed — all three logged as "No" |
| WHAT 2.3 | No repeat quick-fix across consecutive health checks | P1 | 0 repeats | — | — | ✅ No repeats logged |
| WHAT 2.4 | Tech debt items resolved, 5 per month | P2 | 15 (Jul–Sep) | 0 | 15 | ❌ Behind — only pre-phase item logged (Mar 2026) |
| WHAT 2.5 | Cross-brand initiative completed | P2 | 1 | 0 | 1 | 🟡 In flight — [PR #156](https://github.com/Travelopia/wordpress-packages/pull/156) is network-wide, still in review |
| WHAT 3.1 | Merged contributions to AI Skills package | P1 | 1 | 2 | 0 | ✅ Exceeded — [#60](https://github.com/Travelopia/wordpress-team-ai-skills/pull/60), [#66](https://github.com/Travelopia/wordpress-team-ai-skills/pull/66) |
| WHAT 3.2 | Learning shared with team, 1 per month | P1 | 3 (Apr–Jun) | 1 | 2 | ❌ Behind — May only |
| WHAT 3.3 | Further merged AI Skills contributions | P2 | 2 | 1 | 1 | 🟡 In progress — [helix-skills #13](https://github.com/Travelopia/helix-skills/pull/13) |
| WHAT 3.4 | Merged PRs to team open source packages | P2 | 2 | 0 | 2 | 🟡 In flight — [PR #156](https://github.com/Travelopia/wordpress-packages/pull/156) in review |
| WHAT 3.5 | Deep dive presented to the team | P2 | 1 | 0 | 1 | ❌ Not started |
| WHAT 3.6 | Merged skill/extension benefiting own project or group | P2 | 1 by 30 Sep | 1 | 0 | ✅ Done — a11y gate skills used across brand builds |
| HOW 1.1 | Async video demos in #wordpress, 1 per month | FY26 | 6 by Sep (10+ stretch) | 1 | 5 | ❌ Behind — May only |
| HOW 1.2 | Direct responses to PM/stakeholder questions | FY26 | No deferrals | 1 | — | ✅ On track — 1 logged, same-day |
| HOW 1.3 | Zero escalations that should have been handled | FY26 | 0 | — | — | ✅ On track — none logged |
| HOW 1.4 | PR descriptions explaining business impact | FY26 | Every PR | — | — | ✅ On track — in-flight entries carry impact notes |
| HOW 2.1 | Proactive fixes without a ticket | FY26 | Ongoing | 0 | — | ❌ None logged |
| HOW 2.2 | Zero untested code reaching QA | FY26 | 0 | — | — | ✅ On track |
| HOW 2.3 | Explore 2+ AI approaches before "not possible" | FY26 | Every case | — | — | ✅ Evidenced — `tp-slider` unblock proposals, Sunsail itineraries |

**Countable totals:** 10 done · 39 remaining across the 11 objectives with hard numeric targets. The remaining 9 are qualitative or ongoing.

### Immediate priorities

1. **WHAT 2.4** — 15 tech debt items due Jul–Sep, none logged. Highest-volume gap.
2. **HOW 1.1 / WHAT 3.2** — 5 demos short of the September target; one per month recovers it only if Aug and Sep both ship, so a catch-up is needed.
3. **WHAT 3.5** — deep dive not started; one month of runway left.

---

## WHAT 1 — AI-First Delivery

### Phase 1 (April – June 2026)
- [ ] Deliver 100% of development work using the WordPress AI Skills package — every PR from April onwards uses the relevant skill (`/travelopia-wp-block`, `/travelopia-wp-blade-component`, `/travelopia-wp-php`, etc.)
- [ ] Every PR carries a `.specs` directory — this is how skill usage is measured
- [ ] Every PR ships with automated test coverage generated through the skills — engineer owns quality, not QA
- [ ] Achieve 1.5x faster average PR turnaround (ticket start to merged PR) vs the April baseline

### Phase 2 (July – September 2026)
- [ ] Maintain 100% AI skill usage
- [ ] Push speed to 2x faster vs the April baseline
- [ ] Use AI for discovery and estimation — initial feasibility assessments within 4 hours for standard requests
- [ ] Zero QA rejections from missing test coverage for the full phase

**Why testing matters:** every E2E test makes future work faster. WordPress and plugin updates become near-automatic when coverage exists — `/travelopia-wp-update` runs the update, the tests verify nothing broke, and the PR ships with confidence. Phase 1 coverage is the infrastructure that makes everything after it easier.

**Measure:** AI skill usage per PR (`.specs` + 1:1 verification), PR turnaround time (GitHub data), feasibility response time (PM feedback).

---

## WHAT 2 — Site and Group Ownership

WordPress core updates, plugin updates, and routine dependency bumps are BAU — handled with `/travelopia-wp-update` as part of regular delivery. They do **not** count as tech debt.

### Phase 1 (April – June 2026)
- [ ] Know the assigned sites and group inside out — health check scores, open tech debt, recurring issues
- [ ] Resolve at least 2 quick-fix health check findings per fortnight, within 5 working days of the health check run
- [ ] Post a summary in the site Slack channel when each quick-fix PR is raised
- [ ] Route anything that could affect live functionality through a ticket and the PM — quick-fixes are zero-risk items only
- [ ] No quick-fix issue appears in two consecutive health checks (a repeat is a miss)

Quick-fix = no business decision needed: config fixes, performance tweaks, broken schemas, missing tests, deprecated code removal.

### Phase 2 (July – September 2026)
- [ ] Resolve at least 5 tech debt items per month across the group — proactively identified, not ticketed; tagged "Tech Debt" in Jira
- [ ] Complete at least 1 cross-brand initiative in the group (shared component, common fix, pattern standardisation)
- [ ] 30% reduction in the group's open tech debt backlog by end of September

**The PM relationship:** PMs are informed, not gatekeepers. Default is fix it and notify the PM in the site Slack channel. If it could affect live functionality or business priorities, flag the PM first. When in doubt, ask — but the bias is toward action.

**Measure:** health check resolution rate (Cyrax), consecutive misses (Cyrax), tech debt items resolved (Jira "Tech Debt" label), cross-brand PRs, group backlog trend.

---

## WHAT 3 — AI Learning and Contribution

### Phase 1 (April – June 2026)
- [x] Submit at least 1 merged contribution to the WordPress AI Skills package — [#60](https://github.com/Travelopia/wordpress-team-ai-skills/pull/60), [#66](https://github.com/Travelopia/wordpress-team-ai-skills/pull/66)
- [ ] Share 1 learning per month with the team — async video (3–5 min) or written post in #wordpress (1 of 3: May 2026)

### Phase 2 (July – September 2026)
- [ ] Submit at least 2 merged contributions to the AI Skills package (1 of 2: [helix-skills #13](https://github.com/Travelopia/helix-skills/pull/13))
- [ ] Contribute at least 2 merged PRs to the team's open source packages
- [ ] Present 1 deep dive to the team on a WordPress or AI ecosystem development that impacts our work
- [x] By end of September, have at least 1 merged skill or skill extension that directly benefits the project or group

**Measure:** merged PRs on the AI skills repo (GitHub), published learnings in #wordpress, open source contributions (GitHub), deep dive presentations delivered.

---

## HOW 1 — Communication and Visibility (Collaborative and Inclusive)

Throughout FY26, make work, thinking, and learnings visible to the team and stakeholders.

- [ ] Post 1 async video demo per month in #wordpress showing AI-delivered work — format: "I built [thing] using [skill], here's the before/after, here's what surprised me" (1 of 6 target by September)
- [ ] Actively contribute in every group and team call — share context, ask questions, raise concerns
- [ ] Write PR descriptions that explain business impact, not just the technical change
- [ ] Respond directly to PM and stakeholder questions — do not defer; if unsure, say "I'll find out by [time]" and follow through
- [ ] Share knowledge proactively — post solutions and better approaches for the team without being asked

**Measure:** monthly demo posts (target 10+ by September), zero escalations to Junaid that should have been handled directly, PM/peer feedback on communication quality (June and September reviews).

---

## HOW 2 — Ownership Mindset (Bias for Action)

Throughout FY26, operate as an owner of outcomes, not a processor of tickets.

- [ ] Never default to "not possible" — explore at least 2 AI-assisted approaches first; if genuinely not feasible, document why with evidence
- [ ] Treat testing as own responsibility, not QA's — every piece of work tested before it leaves your hands, using the tests the skills generate
- [ ] Act the same day on problems seen in the group — fix if quick, raise in Slack if it needs discussion; don't wait for a ticket, sprint, or manager
- [ ] Flag risks and blockers immediately in the site/group channel, not at the next standup or 1:1

**Measure:** proactive contributions (PRs, Slack posts, fixes without tickets), zero untested code reaching QA, PM/peer feedback on initiative and reliability.

---

## Exceeds Expectations

Not required for "meets expectations" — tracked in [README.md](README.md#exceeds-expectations-checklist).

- [ ] Ship significantly faster than the 2x target
- [ ] Proactively find and fix problems nobody else noticed
- [ ] Async demos so good that other teams reference them
- [x] Multiple meaningful AI skill improvements (3+)
- [ ] PMs specifically call out communication as exceptional
- [ ] Mentor other engineers on AI skills without being asked
- [ ] Contribute to the WordPress ecosystem (core, plugins, Trac) and raise Travelopia's profile
- [ ] Become the person others go to when they're stuck
