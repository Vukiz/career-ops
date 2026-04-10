# Flagship Stories

This file contains the strongest personal stories to lead with in behavioral interviews.

Use these first. The rest of `story-bank.md` is backup material.

## Selection Rules

- Prefer stories with clear stakes, measurable outcomes, and a concrete personal decision.
- Prefer stories that reveal judgment, not just effort.
- Prefer stories that can answer multiple questions without feeling stretched.
- Avoid leading with overlap when one stronger story already covers the same signal.

## Core Seven

### 1. Playvision - Live Modernization Under Real Player Pressure
**Story:** `[Modernization] Turning a live game codebase into a maintainable delivery engine`
**Why It Impresses:** It combines scale, technical debt, delivery, and a hard result: `30s -> 1-2s` load time improvement in a live game with about `1M` players and up to `30k` online, driven by a concrete redesign from monolithic sequential startup to parallelized loading with delayed non-critical retries.
**Signal:** Senior technical ownership, live-service judgment, modernization without rewrite fantasies.
**Use For:** biggest impact, technical debt, working under pressure, legacy rescue, game engineering.

### 2. Playvision - Incident Leadership with Player Trust at Stake
**Story:** `[Incident] Leading a live-service rollback after a reward-loss backend release`
**Why It Impresses:** It shows fast decision-making, cross-functional coordination, player empathy, and post-incident process improvement. It is much stronger than a generic "I fixed a bug" story.
**Signal:** Calm leadership, accountability, operational maturity.
**Use For:** failure, incident response, pressure, conflict, learning from mistakes.

### 3. Playvision - Mentorship with a Clear Human Outcome
**Story:** `[Mentorship] Coaching a talented but hesitant junior into an independent engineer`
**Why It Impresses:** It is specific, human, and outcome-backed. The junior did not just "improve" abstractly; he later soloed a full hypercasual game project.
**Signal:** Coaching ability, emotional intelligence, leverage through people.
**Use For:** mentorship, developing others, leadership impact, building confidence in teams.

### 4. Playtika - Feature Ownership from Design to Quiet Launch
**Story:** `[Ownership] Leading the design of a minigame with reusable platform systems`
**Why It Impresses:** It shows that you can own more than implementation: HLD, reusable systems, analytics, hot config, backend coordination, and a launch that did not require hotfixes.
**Signal:** Product sense, system design, launch readiness, cross-functional leadership.
**Use For:** end-to-end ownership, product partnership, designing for reuse, launching safely.

### 5. Ankr - Productizing a Prototype into a Real Developer Platform
**Story:** `[Platform] Turning a prototype web3 SDK into a production-grade open-source product`
**Why It Impresses:** It is a strong platform story with external credibility: public OSS usage plus Meta Apes relying on it as a core integration layer.
**Signal:** Productization, DX judgment, platform thinking, small-team leadership.
**Use For:** platform work, open source, raising quality bars, turning rough ideas into products.

### 6. Ankr - Leading Through Two Pivots Without Breaking the Org
**Story:** `[Leadership] Guiding a startup through two pivots to beta`
**Why It Impresses:** It shows senior leadership under ambiguity, delegation, organizational design, and architectural foresight that actually mattered when strategy changed, with management scope reaching about `20` people across directs and indirects.
**Signal:** Technical director maturity, startup leadership, pivot resilience.
**Use For:** ambiguity, pivots, building teams, delegation, senior leadership.

### 7. Ankr - Large-Scale Infra Optimization with Hard Numbers
**Story:** `[Scale] Cutting infra cost and improving stability on a 500k RPS path`
**Why It Impresses:** This is the strongest pure systems story in the set: `10x` storage improvement, `50 GB -> 5 GB` RAM reduction, and traffic peaking around `500k` RPS.
**Signal:** Scale, cost efficiency, backend depth, observability and performance judgment.
**Use For:** scale, performance, systems design, cost optimization, backend leadership.

## EM Add-Ons

### 8. Ankr - Making Delivery Predictable Without Adding Bureaucracy
**Story:** `[Process] Making an infrastructure team more predictable without slowing it down`
**Why It Impresses:** It shows you understand that process is only valuable if it improves delivery and focus time. The story has a real before/after, not vague "I improved agile."
**Use For:** process, execution, release management, org effectiveness.

### 9. Ankr - Handling Three Difficult Exits Responsibly
**Story:** `[Management] Handling three difficult exits with accountability`
**Why It Impresses:** It is serious, uncomfortable, and real. Use it only when the interviewer is explicitly probing managerial accountability or difficult decisions.
**Use For:** firing, difficult conversations, org health, leadership maturity.

## SWE Add-Ons

### 8. Ankr - Risky Infra Migration, Cleanly Executed
**Story:** `[Migration] Moving critical API infrastructure from TypeScript workers to Go with zero incidents`
**Why It Impresses:** It combines technical adaptability, schedule performance, and operational safety.
**Use For:** migrations, reliability, new stack adoption, backend execution.

### 9. Playtika - Root-Causing a Hard Production Crash
**Story:** `[Debugging] Fixing a production crash on a 10,000-level map`
**Why It Impresses:** It is a sharp, compact debugging story with visible user impact and a strong finish: fix, performance improvement, and tests.
**Use For:** debugging, profiling, production support, reliability engineering.

## Stories to De-Emphasize

These are good, but they overlap too much with stronger anchors:

- `Playvision - Growing from IC to Lead`
Reason: overlaps heavily with modernization, incident, and mentorship.

- `Playvision - Greenfield Architecture for a New Core Product`
Reason: solid technical story, but less vivid than your stronger game and infra stories.

- `Playtika - Porting an Acquired C++ Game into Unity`
Reason: good legacy story, but the minigame ownership and debugging story are sharper in interviews.

- `Playtika - Mentoring Across a Technology Transition`
Reason: good backup, but weaker than the Playvision junior-growth story.

- `Playtika - Operating in Enterprise Live-Ops`
Reason: useful context, but not distinctive enough to be a flagship.

## Interview Strategy

### If the loop is EM-leaning

Lead with:
1. Mirage pivots
2. Playvision incident
3. Playvision mentorship
4. Ankr process

### If the loop is SWE-leaning

Lead with:
1. Playvision modernization
2. Ankr scale
3. Ankr TypeScript -> Go migration
4. Playtika debugging

### If the loop is game-industry or Riot-manager-leaning

Lead with:
1. Mirage pivots
2. Playvision incident
3. Playvision mentorship
4. Ankr process
5. Playtika Gold Blast ownership

## Riot Note

For Riot manager interviews, the shortlist should skew manager-first:

1. `Mirage pivots`
2. `Playvision incident`
3. `Playvision mentorship`
4. `Ankr process`
5. `Playtika Gold Blast ownership`
6. `Playvision modernization`

Use the heavier infra stories as supporting proof of technical credibility, not as the opening narrative.
