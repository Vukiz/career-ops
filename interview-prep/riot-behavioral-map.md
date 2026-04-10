# Riot Behavioral Interview Map

This file is a Riot-focused behavioral prep guide built from the flagship stories.

Use this file for:
- recruiter / HR screen
- first-round behavioral interviews
- manager screens
- "tell me about a time when..." questions

Primary reference values come from Riot's official values pages:
- `Player First`
- `Serious About Games`
- `Dream and Deliver`
- `In for the long term`
- `One Riot`

Official sources:
- [Riot Values](https://www.riotgames.com/en/who-we-are/values)
- [Interviewing at Riot](https://www.riotgames.com/en/work-with-us/interviewing-at-riot)

## Riot Value Translation

### Player First

What they are likely screening for:
- empathy for players, not just internal stakeholders
- willingness to protect player trust during incidents and launches
- judgment about quality, fairness, safety, and player experience

Your best evidence:
- `Playvision incident`
- `Playvision modernization`
- `Playtika Gold Blast ownership`

### Serious About Games

What they are likely screening for:
- real care for gameplay feel and game quality
- respect for polish, craft, and player-facing detail
- understanding that "good enough" often is not good enough in games

Your best evidence:
- `Playtika Gold Blast ownership`
- `Playtika C++ -> Unity port` as backup
- `Playvision modernization`

### Dream and Deliver

What they are likely screening for:
- ambition combined with operational follow-through
- ability to turn messy ideas into shipped outcomes
- leadership that goes beyond planning into execution

Your best evidence:
- `Mirage pivots`
- `Ankr SDK platform`
- `Gold Blast ownership`

### In for the Long Term

What they are likely screening for:
- sustainable architecture and process
- investing in systems that survive future scale and change
- not trading tomorrow away for short-term wins

Your best evidence:
- `Playvision modernization`
- `Ankr process`
- `Ankr scale`

### One Riot

What they are likely screening for:
- cross-functional collaboration
- low-ego leadership
- ability to align engineering, design, product, QA, and leadership

Your best evidence:
- `Playvision incident`
- `Gold Blast ownership`
- `Mirage pivots`

## Core Story Keys

- `Playvision modernization`: live-game modernization, `30s -> 1-2s` load time, `1M` players, `30k` online
- `Playvision incident`: reward-loss incident, `~1000` affected players, `3-4h`, rollback plus process hardening
- `Playvision mentorship`: junior growth into independent engineer
- `Gold Blast ownership`: minigame HLD, reusable systems, analytics, no hotfixes, `~3 months`
- `Ankr SDK platform`: prototype -> open-source SDK, Unity + Unreal, Meta Apes usage
- `Mirage pivots`: Technical Director, `~20` people across directs and indirects, `2` pivots, beta release
- `Ankr process`: better estimation, less meeting load, async culture, biweekly release discipline
- `Ankr scale`: `10x` storage reduction, `50 GB -> 5 GB` RAM, `~500k` RPS
- `Ankr migration`: TypeScript workers -> Go, `2 months early`, `0 incidents`
- `Playtika debugging`: memory leak on `10k`-level map, crash fix plus FPS improvement

## HR Screen

These are usually higher-level and should sound concise, confident, and easy to follow.

### Tell me about yourself

Best structure:
1. Start with live games and legacy ownership.
2. Show progression into leadership and cross-functional responsibility.
3. End with scale and organizational leadership at Ankr.
4. Tie back to why Riot manager roles fit.

Suggested answer shape:
- "I started in live games, where I built my career taking ownership of difficult legacy systems under real player pressure. At Playvision and Playtika, that meant modernizing game codebases, shipping features, handling incidents, and mentoring engineers in production environments. Over time I moved into broader leadership, from leading a game SDK team and a startup at Ankr to later leading infrastructure work at scale, where I improved engineering process, reliability, and platform performance. The common thread is that I do my best work in messy environments where player impact, technical depth, and team leadership all matter at once, which is a big part of why Riot manager roles appeal to me."

Riot value emphasis:
- `Player First`
- `Serious About Games`
- `Dream and Deliver`

### Why Riot?

Recommended answer themes:
- you are already deeply motivated by games, not just software
- Riot's values are explicit about serving players
- you want to work where quality, craft, and player trust matter
- you can bring both hands-on technical credibility and people leadership

Do:
- mention that you actively play Riot games if true
- connect your live-service experience to Riot's player-first standard
- connect your manager aspiration to Riot's scale and craft bar

Avoid:
- generic "Riot is prestigious"
- over-focusing on web3 or infra unless tied back to player value and games

### Why this manager role?

Recommended answer themes:
- you have already crossed from pure implementation into mentorship, process, org design, and stakeholder alignment
- your best stories are about making teams more effective while staying technically credible
- you still enjoy engineering depth, but your highest leverage comes from helping teams deliver better outcomes

Best supporting stories:
- `Mirage pivots`
- `Playvision mentorship`
- `Ankr process`

## Behavioral Question Map

### Tell me about a time you led through ambiguity

Primary story:
- `Mirage pivots`

Riot value fit:
- `Dream and Deliver`
- `In for the long term`
- `One Riot`

Key points to emphasize:
- the strategy changed materially, not cosmetically
- you anticipated volatility and designed for it
- you delegated leads to create leverage
- the team still delivered beta despite two pivots

Watchout:
- do not let the story sound like "the project failed anyway"
- frame the success as organizational and architectural resilience under uncertainty

### Tell me about a time you put players first

Primary story:
- `Playvision incident`

Backup:
- `Playvision modernization`
- `Gold Blast ownership`

Riot value fit:
- `Player First`
- `One Riot`

Key points to emphasize:
- player trust was damaged in real time
- you acted quickly to contain harm
- you coordinated engineering, QA, and communication
- you improved the process so the same class of mistake would not recur

Watchout:
- do not over-index on blame
- keep the focus on response quality and player trust

### Tell me about a time you improved a struggling system

Primary story:
- `Playvision modernization`

Backup:
- `Ankr scale`
- `Ankr migration`

Riot value fit:
- `In for the long term`
- `Dream and Deliver`

Key points to emphasize:
- legacy monolith in a live game
- had to modernize while continuing delivery
- parallelized startup and delayed non-critical work
- achieved a meaningful player-facing improvement

Watchout:
- do not make it sound like a vague cleanup effort
- be explicit about the technical decision and business impact

### Tell me about a time you developed someone

Primary story:
- `Playvision mentorship`

Backup:
- `Playtika mentoring`

Riot value fit:
- `One Riot`
- `Dream and Deliver`

Key points to emphasize:
- the core challenge was confidence and ownership
- you tailored coaching to the person, not just the task
- the outcome was concrete and visible

Watchout:
- do not make the story paternalistic
- present the engineer as capable, and your role as enabling their growth

### Tell me about a time you had to make a hard people decision

Primary story:
- `Mirage exits`

Riot value fit:
- `One Riot`
- `In for the long term`

Key points to emphasize:
- different causes required different treatment
- one case had a real PIP and explicit expectations
- you understood the cost of delaying necessary action
- you handled it to protect the team and the business

Watchout:
- use this only when directly asked
- keep the tone serious and accountable, never casual

### Tell me about a time you launched something successfully

Primary story:
- `Gold Blast ownership`

Backup:
- `Ankr SDK platform`

Riot value fit:
- `Serious About Games`
- `Dream and Deliver`
- `Player First`

Key points to emphasize:
- HLD ownership, not just coding
- reusable systems, analytics, hot config, edge cases
- quiet launch with no hotfixes
- design/backend/client alignment

Watchout:
- do not bury the launch outcome
- say clearly that the game shipped in about three months and did not require hotfixes

### Tell me about a time you improved team execution

Primary story:
- `Ankr process`

Backup:
- `Playvision IC -> Lead` from reserve

Riot value fit:
- `Dream and Deliver`
- `One Riot`
- `In for the long term`

Key points to emphasize:
- there was a real before-state: poor estimation and sprint spillover
- your changes were concrete, not motivational
- you reduced meetings and increased focus time
- the team started finishing sprint commitments reliably

Watchout:
- do not call it "agile transformation"
- stay practical and outcome-focused

### Tell me about a time you built for long-term scalability

Primary story:
- `Ankr scale`

Backup:
- `Playvision architecture`
- `Ankr migration`

Riot value fit:
- `In for the long term`
- `Dream and Deliver`

Key points to emphasize:
- hard metrics matter here
- explain tradeoffs clearly
- show that you improved both cost and stability, not just speed

Watchout:
- avoid sounding too infra-generic for Riot game roles
- tie the answer back to reliable player-facing systems and sustainable engineering

### Tell me about a time you learned a new domain or stack quickly

Primary story:
- `Ankr migration`

Backup:
- `Playtika C++ -> Unity port`

Riot value fit:
- `Dream and Deliver`

Key points to emphasize:
- you switched into Go in a meaningful production context
- the system was critical
- you still delivered early and safely

### Tell me about a technical problem you solved that others found difficult

Primary story:
- `Playtika debugging`

Backup:
- `Playvision modernization`
- `Ankr scale`

Riot value fit:
- `Serious About Games`
- `Dream and Deliver`

Key points to emphasize:
- high-level players were affected
- you profiled and benchmarked rather than guessing
- you found the memory leak and improved performance more broadly
- you added tests afterward

## Riot-Specific Framing Guidance

### How to make your stories sound more Riot-aligned

- Say `players` more often than `users` when the story is about games.
- Talk about trust, fairness, experience quality, polish, and live-service responsibility.
- Emphasize that quality is not abstract; it shapes how players feel about the game.
- When describing launches, mention readiness, instrumentation, and quiet launches.
- When describing management, emphasize team health, craft standards, and collaboration.

### Phrases worth using

- `protect player trust`
- `quiet launch for the right reasons`
- `player-facing impact`
- `cross-functional alignment`
- `quality bar`
- `sustainable delivery`
- `low-coupling architecture`
- `technical credibility as a manager`

### Phrases to avoid

- `resources`
- `headcount management` unless discussing budgeting explicitly
- `just a game`
- `move fast and break things`
- `good enough`

## Answer Format

For behavioral rounds, default to:

1. `Situation`
2. `Task`
3. `Action`
4. `Result`
5. `What I learned`
6. `Why it matters at Riot`

That last sentence is important. Add a short Riot bridge like:
- "I think that maps well to Riot because player trust and quality clearly matter here."
- "That experience is why I care a lot about sustainable delivery, especially in player-facing systems."
- "That is the kind of cross-functional ownership I would bring to a Riot manager role."

## Recommended Story Order For Riot Manager Interviews

Use this default order unless the interviewer steers elsewhere:

1. `Mirage pivots`
2. `Playvision incident`
3. `Playvision mentorship`
4. `Ankr process`
5. `Gold Blast ownership`
6. `Playvision modernization`

Use these as supporting credibility stories when needed:
- `Ankr scale`
- `Ankr migration`
- `Playtika debugging`

## Open Gaps

These answers are already usable, but these details would improve them further:

- the exact outcome or player/business signal from Mirage beta, if any
- one concise example of feedback you gave in the PIP story
- one concise sentence on why the delayed non-critical startup retries at Playvision were safe from a player-experience standpoint
