# Experience Summary

This file is the low-context recall layer for interview prep.

Read order:
1. `interview-prep/flagship-stories.md`
2. `interview-prep/story-bank.md` for the full STAR+R versions
3. `interview-prep/experience-inventory.md` only when deeper raw context is needed

## Core Narrative

I started in live games and grew by taking ownership of difficult legacy systems under production pressure. Over time, that turned into broader technical leadership: improving maintainability, mentoring engineers, handling incidents, designing reusable systems, and eventually leading teams, startups, and infrastructure platforms. The throughline across my career is that I do well in messy environments where systems, teams, and process all need to become more reliable without slowing delivery. I can operate as either a hands-on engineering leader or a senior engineer with strong product and operational judgment.

## Core Flagship Stories

### Playvision - Live Game Modernization at Scale
**Snapshot:** I helped turn Durak Online, a live game with about 1 million players and up to 30,000 concurrent users, from a fragile monolithic codebase into a much more maintainable delivery system while still shipping features, supporting a full UI overhaul, and keeping production stable. The biggest technical lever was redesigning startup from a monolithic sequential load into parallelized steps, while delaying and retrying non-critical work instead of blocking the whole flow. That brought load times down from up to 30 seconds to around 1-2 seconds.
**Why Keep It:** Best all-around story for technical depth, scale, live-ops pressure, and business impact.
**Primary Lens:** hybrid
**Best Question Fits:** biggest impact; technical debt; improving a broken system; live operations
**Story Ref:** `[Modernization] Turning a live game codebase into a maintainable delivery engine`

### Playvision - Leading a Reward-Loss Production Incident
**Snapshot:** Shortly after becoming Lead Developer, I handled a live incident where a backend rollout caused around 1,000 players not to receive rewards for wins over a 3-4 hour period. I drove rollback, coordinated QA and player communication, and then changed the release process to prevent the same failure mode from recurring.
**Why Keep It:** Strongest player-empathy and under-pressure leadership story.
**Primary Lens:** EM
**Best Question Fits:** incident response; accountability; handling pressure; learning from failure
**Story Ref:** `[Incident] Leading a live-service rollback after a reward-loss backend release`

### Playvision - Coaching a Junior into an Independent Engineer
**Snapshot:** I mentored a very capable but low-confidence junior engineer and focused on building ownership, judgment, and confidence rather than just teaching syntax. He went from small isolated tasks to soloing a full hypercasual game project from scratch to production release in about two weeks.
**Why Keep It:** Best pure people-development story.
**Primary Lens:** EM
**Best Question Fits:** mentorship; developing others; raising team capability; leadership impact
**Story Ref:** `[Mentorship] Coaching a talented but hesitant junior into an independent engineer`

### Playtika - Owning a Minigame Launch End to End
**Snapshot:** As Key Developer on Solitaire Grand Harvest, I owned the HLD for Gold Blast / Catch the Mole, a new minigame that also required reusable systems, analytics coverage, hot-config support, and careful client-server communication design. We shipped it in about three months without needing hotfixes after launch.
**Why Keep It:** Best game-feature ownership story with product, backend, and launch-readiness depth.
**Primary Lens:** hybrid
**Best Question Fits:** end-to-end ownership; launch readiness; cross-functional execution; designing for reuse
**Story Ref:** `[Ownership] Leading the design of a minigame with reusable platform systems`

### Ankr - Turning a Prototype SDK into a Real Platform
**Snapshot:** I inherited a prototype web3 SDK for Unity and Unreal that was mostly a thin wrapper over a third-party library and turned it into a real open-source product with stronger quality, documentation, demos, and deeper Ankr integration. It saw public adoption and was used by Meta Apes as a core web interaction library in a game that generated millions in revenue.
**Why Keep It:** Strong platform, productization, and external-impact story.
**Primary Lens:** hybrid
**Best Question Fits:** platform engineering; developer experience; productizing prototypes; open source
**Story Ref:** `[Platform] Turning a prototype web3 SDK into a production-grade open-source product`

### Ankr - Guiding Mirage Through Two Pivots to Beta
**Snapshot:** As Technical Director of Mirage Interactive, I hired and organized a cross-functional team, shaped product and technical direction with leadership, and guided the company through two pivots, including one from a pure NFT marketplace toward a Steam-like marketplace with profiles and game integrations. At peak, I was effectively managing around 20 people across directs and indirects, and the modular low-coupling architecture I pushed for made the rework survivable. We still reached beta before funding ran out.
**Why Keep It:** Best ambiguity, startup, and organizational leadership story.
**Primary Lens:** EM
**Best Question Fits:** leading through ambiguity; startup execution; pivots; delegation; technical leadership
**Story Ref:** `[Leadership] Guiding a startup through two pivots to beta`

### Ankr - Cutting Infra Cost and Improving Stability at 500k RPS
**Snapshot:** In Ankr Core Infrastructure, I reduced ClickHouse storage by about 10x and cut proxy RAM usage from roughly 50 GB to 5 GB per instance while improving stability on a path that handled hundreds of thousands of RPS and peaks around 500k. I also implemented hybrid caching and improved observability.
**Why Keep It:** Strongest pure scale and performance story.
**Primary Lens:** SWE
**Best Question Fits:** scale; performance optimization; cost efficiency; reliability at scale
**Story Ref:** `[Scale] Cutting infra cost and improving stability on a 500k RPS path`

## EM Add-Ons

### Ankr - Making an Infra Team Predictable Without Slowing It Down
**Snapshot:** I introduced better estimation rules, HLD prereads, release policies, fewer meetings, and more async communication in Ankr Core Infrastructure. Within about two months, the team became much better at finishing planned sprint work on a biweekly backend release cadence.
**Why Keep It:** Best process-improvement story for manager loops.
**Primary Lens:** EM
**Best Question Fits:** process improvement; release management; execution discipline; async culture
**Story Ref:** `[Process] Making an infrastructure team more predictable without slowing it down`

### Ankr - Handling Three Difficult Exits with Accountability
**Snapshot:** At Mirage, I had to make three difficult exits under a mix of budget and performance pressure, including one case that went through a one-month PIP. It was painful, but it forced me to treat accountability and org health as part of leadership rather than something to delay.
**Why Keep It:** Important manager-only story, but use selectively.
**Primary Lens:** EM
**Best Question Fits:** difficult conversations; firing; accountability; protecting team health
**Story Ref:** `[Management] Handling three difficult exits with accountability`

## SWE Add-Ons

### Ankr - Migrating Critical Infrastructure from TypeScript to Go
**Snapshot:** I moved legacy TypeScript Cloudflare-worker functionality into a Go-based Ankr platform as the system expanded into public and private traffic. We delivered the migration about two months ahead of plan with zero production incidents because of extensive automated test coverage.
**Why Keep It:** Best migration and risk-management story for backend interviews.
**Primary Lens:** SWE
**Best Question Fits:** migrations; learning new stacks fast; reliability during change; backend execution
**Story Ref:** `[Migration] Moving critical API infrastructure from TypeScript workers to Go with zero incidents`

### Playtika - Fixing a Crash on a 10,000-Level Map
**Snapshot:** I debugged a production crash affecting very high-level players on a large scrollable map, traced it to a memory leak, fixed it, improved scrolling FPS more broadly, and added tests to prevent regression.
**Why Keep It:** Best compact debugging story.
**Primary Lens:** SWE
**Best Question Fits:** debugging hard problems; production support; performance; root-cause analysis
**Story Ref:** `[Debugging] Fixing a production crash on a 10,000-level map`

## Reserve Stories

These are useful, but not top-tier anchors unless a question specifically calls for them:

- `Playvision - Growing from IC to Lead`
- `Playvision - Greenfield Architecture for a New Core Product`
- `Playtika - Porting an Acquired C++ Game into Unity`
- `Playtika - Mentoring Across a Technology Transition`
- `Playtika - Operating in Enterprise Live-Ops`

## Pruning Notes

- The strongest stories are the ones with clear stakes, measurable outcomes, and a visible leadership or technical choice.
- Several older entries were overlapping versions of the same theme, especially around "grew into leadership" and "worked in legacy systems." Those are now compressed into stronger anchor stories instead of being treated as separate pillars.
- For most interviews, you do not need more than 7 core stories plus 2 role-specific add-ons.
