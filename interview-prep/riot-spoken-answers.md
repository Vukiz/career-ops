# Riot Spoken Answers

This file turns the Riot behavioral map into spoken answers.

Goal:
- simple English
- natural and conversational
- strong, but not over-polished
- easy to remember and adapt

## Speaking Style

Use this style:
- short sentences
- clear structure
- no buzzwords unless needed
- say what happened, what you did, and what changed

Good pattern:
1. short context
2. what the problem was
3. what you personally did
4. result
5. short takeaway

Good phrase starters:
- `A good example is...`
- `One case that comes to mind is...`
- `What I did there was...`
- `The main thing I learned was...`
- `If I connect it to Riot, ...`

## Riot Manager Core Answers

### 1. Tell me about yourself

#### Short version

I started in live games, and most of my career grew from taking ownership of messy systems in production. At Playvision and Playtika, I worked on live games, legacy code, launches, incidents, and mentoring engineers. Later at Ankr I moved into broader leadership, first leading a game SDK team, then becoming Technical Director of a startup, and later leading infrastructure and process improvements at scale. The common thread is that I like environments where quality, delivery, and team health all matter at the same time. That is a big reason why a Riot manager role feels like a good fit for me.

#### Longer version

I started as a game engineer, and I think the main pattern in my career is that I usually get pulled into difficult environments where systems or teams need more ownership and structure. At Playvision I worked on a live game with real player pressure, where I helped modernize a legacy codebase, handled production issues, and grew into a lead role. At Playtika I worked in a bigger enterprise environment, where I helped port a game from C++ to Unity, owned a new minigame launch, and mentored engineers across different tech backgrounds.

Later at Ankr I moved into broader leadership. First I led development of a Unity and Unreal SDK and turned it from a prototype into a real open-source product. Then I became Technical Director of Mirage Interactive, where I hired and organized a cross-functional team, handled pivots, and managed a bigger organization. After that I moved into core infrastructure, where I still stayed hands-on technically but also improved team process, delivery quality, and large-scale system performance.

So I would describe myself as a manager with strong technical credibility, especially in messy, player-facing, or high-pressure environments.

### 2. Why Riot?

#### Short version

For me, Riot is interesting because it is one of the few companies where player experience and game quality are clearly taken seriously. I have spent most of my career in live products, so I care a lot about trust, polish, and long-term quality. I also like that Riot is not just about shipping features, but about building things players will really care about. That fits both my background and what I want next.

#### Longer version

The main reason is that Riot feels very aligned with how I already think about products. I spent years in live games, and in that world you see very quickly that quality is not abstract. If players lose trust, they feel it immediately. So I care a lot about player-first thinking, careful launches, incident response, and making systems reliable without losing speed.

I also like that Riot is clearly serious about games, not just software. That matters to me. I want to work somewhere where polish, gameplay experience, and cross-functional craft are taken seriously. And for this specific manager direction, I think I can bring both sides: I can lead engineers and process, but I also have enough technical depth to understand difficult tradeoffs and help teams make strong decisions.

### 3. Why do you want to be a manager?

#### Short version

Because my highest leverage is no longer only in my own coding. I still enjoy technical work, but over time I saw that I create more impact when I help teams work better, grow engineers, improve clarity, and connect technical decisions with product goals. That is already what I have been doing in practice, so I want a role where that is the main expectation.

#### Longer version

I still like building things myself, and I do not see management as moving away from engineering completely. But over time I noticed that my biggest impact usually came from helping a team perform better, not only from my own implementation. That can be mentoring someone into independence, improving process so delivery becomes predictable, handling hard incidents, or giving better technical direction so a team avoids waste.

At Playvision, Playtika, and Ankr, I naturally moved into those responsibilities anyway. I was mentoring, helping with planning, improving process, and aligning different functions before some of those responsibilities were even formal. So for me, becoming a manager is not a random shift. It is more that I want my role to match the kind of leverage I already create best.

## Story Answers

### 4. Tell me about a time you led through ambiguity

Best story:
- `Mirage pivots`

#### Short version

One good example is Mirage Interactive, where I was Technical Director. We were building a web3 gaming marketplace, but the product direction changed a lot and we had two major pivots. One of them was moving from a pure NFT marketplace to a more Steam-like marketplace with player profiles and game integrations. Because I expected startup volatility, I had pushed for a modular and low-coupling architecture early, and I also assigned backend and frontend leads so I had enough leverage to manage the bigger picture. That helped us survive the pivots and still reach beta, even though the company later stopped because of funding.

#### Longer version

A strong example is Mirage Interactive. I was the Technical Director there, and it was a startup environment inside a bigger company, so there was already a lot of uncertainty. We were building a web3 gaming marketplace, but over time the product direction changed in a major way. One concrete pivot was moving from a pure NFT marketplace inside a gaming ecosystem to something much closer to a Steam-like marketplace, where we needed player profiles and game integrations.

That kind of change can destroy a team if the architecture and org are too rigid. Because I expected instability, I had already been pushing for low coupling in the architecture. I also delegated backend and frontend leads, because I needed enough room to handle product direction, roadmap, budgeting, and stakeholder alignment. At peak I was effectively managing around 20 people across directs and indirects.

The result was that, even with two big pivots, the team kept functioning and we still reached beta. The project later stopped because of funding, but I still see that as one of my best examples of leading through ambiguity without letting the team break apart.

### 5. Tell me about a time you put players first

Best story:
- `Playvision incident`

#### Short version

One strong example was at Playvision, shortly after I became Lead Developer. A backend rollout caused players not to receive rewards after winning games. Around 1,000 players were affected over about 3 to 4 hours. I took ownership of the response, told backend to roll back immediately, asked QA to collect affected player IDs, and made sure communication went out that affected players would be reimbursed. After that, I changed the release process so backend changes could not go directly to production without proper QA and contract visibility. For me that was very player-first, because the focus was not only fixing the bug, but protecting trust.

#### Longer version

At Playvision we had an incident where a backend update caused players not to receive rewards after winning games. This happened shortly after I became Lead Developer. The issue affected around 1,000 players and lasted for roughly 3 to 4 hours, so complaints started coming in fast.

What mattered to me there was not only the technical fix. It was also player trust. I took lead on the response and made a few fast calls. I asked backend to roll back right away. I asked QA to identify affected players, and I made sure our communication clearly said that we understood the issue and would reimburse the players who were impacted.

Then after the incident I focused on making sure we would not repeat the same class of mistake. I blocked direct backend rollouts to production without QA approval on a test environment, required contract changes to be visible in shared communication and documentation, and pushed for stronger backend testing.

The thing I like about this story is that it shows player-first thinking in a real live-service situation, not only in theory.

### 6. Tell me about a time you developed someone

Best story:
- `Playvision mentorship`

#### Short version

At Playvision I mentored a junior engineer who was clearly smart, but he lacked confidence and avoided responsibility. I focused on helping him build ownership and confidence, not only teaching technical details. I gave him manageable responsibility, pushed him to defend his thinking, and shared learning material that would help him avoid common mistakes. Over time he became much more confident and later soloed a full hypercasual game project from scratch to production release in about two weeks.

#### Longer version

One of my favorite mentorship examples was a junior engineer at Playvision. He was smart and well-educated, but he was shy and not confident enough, so he often hesitated to take ownership even when he could handle the work.

I felt that the real problem was not raw technical ability. It was confidence and responsibility. So I did not only review his code. I tried to create a framework where he could own tasks safely. I gave him work that was challenging but manageable, encouraged him to explain and defend his choices, and pointed him to learning materials that would help him build better habits and judgment.

Over time he changed a lot. He became much more confident, and the best proof was that later he could solo a full hypercasual game project from scratch to production release in around two weeks.

For me, that is one of the clearest examples that good leadership is not only about solving problems yourself. It is also about helping other people become capable of solving bigger problems.

### 7. Tell me about a time you improved team execution

Best story:
- `Ankr process`

#### Short version

At Ankr Core Infrastructure, I inherited a team where estimates were inconsistent and sprint work often spilled into the next sprint. We were releasing backend changes every two weeks, so that lack of predictability was becoming painful. I introduced a clearer estimation model, blocked undecomposed tasks from entering a sprint, required tests to be included in estimates, required HLDs for more complex work, and reduced meetings in favor of async written communication. Within about two months, the team became much more reliable at finishing planned sprint work.

#### Longer version

At Ankr Core Infrastructure, one of the team problems was that delivery predictability was weak. We had a biweekly backend release cadence, but estimates were often inconsistent, people brought work into the sprint that was not broken down enough, and we kept carrying tasks into the next sprint.

I wanted to fix that without adding heavy process. So I introduced a few concrete rules. We created a reference table for story point estimation. I blocked undecomposed tasks from entering a sprint. I made sure test work had to be included in the estimate. For more complex work, I required an HLD so people could preread and review it before implementation. I also reduced meeting load and pushed communication more toward written async updates.

The result was that in about two months the team became much more predictable. We started finishing the work we planned instead of constantly moving it to the next sprint. That was important to me because good process should create more focus, not more bureaucracy.

### 8. Tell me about a time you launched something successfully

Best story:
- `Gold Blast ownership`

#### Short version

At Playtika, after I became Key Developer, I owned the HLD for a new minigame called Gold Blast, also known as Catch the Mole. What made it interesting was that it was not only feature work. We also needed reusable systems, analytics, hot-config support, and strong edge-case coverage. I worked closely with product and backend so the launch would be operationally solid, not just feature-complete. We shipped it in about three months and did not need hotfixes after launch.

#### Longer version

At Playtika I was promoted to Key Developer after I gained enough context in the game codebase, and one of my biggest feature-ownership stories there was Gold Blast, or Catch the Mole.

From the outside it looked like just a minigame, but in practice it included much more than implementing the mechanic itself. We needed underlying systems that other teams could reuse later, like badge-related functionality. We also needed analytics coverage, hot-config support, and careful handling of edge cases. I also worked with backend developers on client-server communication so we were not sending unnecessary data and were keeping the right responsibilities on the client side.

The thing I am most proud of is that the launch was quiet for the right reasons. We shipped it in about three months from planning to production release, and we did not need hotfixes after launch. For me, that is a good example of ownership because the job was not only to ship the feature. It was to make the feature launch-ready.

### 9. Tell me about a time you improved a difficult system

Best story:
- `Playvision modernization`

#### Short version

At Playvision I worked on Durak Online, which had a legacy monolithic codebase and real player pressure because it was already a live game. I had to improve the system while we were still shipping features, not in some isolated rewrite project. One of the biggest technical changes I made was moving startup from a monolithic sequential load to parallelized steps, with non-critical work delayed and retried later instead of blocking the whole startup flow. That helped reduce load times from up to 30 seconds to around 1-2 seconds and made the codebase much easier to work with.

#### Longer version

At Playvision I inherited a legacy live-game codebase that had years of technical debt. The hard part was that we could not stop and rebuild everything from scratch, because the game was live, players were active, and the team still needed to ship features.

So my approach was incremental modernization. I improved testing, CI/CD, workflow quality, and maintainability over time. But one of the most important technical changes was in the startup flow. It used to be very monolithic and sequential, so if one part was slow, the whole startup was slow. I redesigned it so more steps could run in parallel, and non-critical work could be delayed and retried later instead of blocking startup.

That was a big reason why we reduced load time from up to 30 seconds to around 1-2 seconds. At the same time, we were still delivering features and keeping the game stable. That is why I think this story works well: it is not modernization in a vacuum, it is modernization inside a real live product.

### 10. Tell me about a time you had to influence without authority

Best story:
- `Gold Blast ownership`

Backup:
- `Playvision incident`
- `Mirage pivots`

#### Short version

At Playtika, when I owned the HLD for Gold Blast, I had to work closely with product and backend even though they did not report to me. I pushed for analytics, hot-config support, and stronger edge-case handling because I wanted the launch to be solid, not only feature-complete. I also guided backend communication design so we were not passing unnecessary data and were keeping the system cleaner. The feature launched in about three months without post-release hotfixes, so the alignment worked.

#### Longer version

At Playtika, a good example of influence without authority was Gold Blast. I owned the HLD, but product, backend, and other functions did not report to me. So I had to influence through credibility and clarity, not through title.

The main thing I pushed for was not only the feature mechanic itself, but everything needed for a successful launch. That meant analytics coverage, hot-config support, stronger edge-case handling, and cleaner client-server communication. In some cases I had to explain why certain data should not be passed or why some processing should stay on the client, because otherwise we were creating unnecessary complexity.

The result was that we got a stronger launch and did not need hotfixes after release. For me, that is a good influence story because I was not pushing for control. I was pushing for quality and sustainability.

## Negative / Trap Questions

You do not need a dramatic disaster here.

A good answer is:
- real
- owned by you
- limited in damage
- shows maturity
- ends with a behavior change

## Best "Negative" Stories

### A. Tell me about a project where you failed

Safest story:
- `Mirage pivots / beta / funding stop`

Why this works:
- it is real
- you can own part of it without claiming full blame
- it shows maturity and strategy, not self-destruction

#### Short version

One example is Mirage Interactive. We did reach beta, but the project did not become a full success because it stopped after funding issues and a lot of strategic change. I do not treat that as somebody else’s problem only, because as Technical Director I was part of the leadership team. What I think I did well was keeping the architecture and team resilient enough to survive two pivots and still ship beta. What I would do better next time is push even harder for earlier product focus and sharper scope control, because in startup environments you can lose a lot of energy by trying to support too many possible directions.

#### Longer version

If I think about a project that did not fully succeed, Mirage is the clearest example. I was Technical Director there, and we built a web3 gaming marketplace. We survived two major pivots and still reached beta, so I do not see it as a total failure in execution. But the business outcome was still not what we wanted, because the startup eventually stopped due to funding and strategy instability.

I do not like answering those questions by pretending it was completely outside my responsibility. As part of leadership, I own part of that outcome too. I think one thing I did well was preparing the architecture and org for volatility, which is why we survived the pivots at all. But if I look back, I would push harder for sharper scope and earlier product focus. In startup environments, flexibility is good, but too much strategic spread can still cost you a lot of momentum.

So the main lesson for me was that resilience is not enough by itself. You also need stronger focus earlier.

### B. Tell me about a time you made a mistake

Safest story:
- `Playvision incident`

Why this works:
- you can own the system/process gap even if you did not write the backend change yourself
- it shows leadership accountability

#### Short version

One example is a reward-loss incident at Playvision. I was already in a lead role, and even though I did not create the backend bug myself, I still saw it as partly my responsibility because the release process was not strong enough. Around 1,000 players were affected. I helped contain the issue fast, but the real mistake was that we still allowed a release model where that kind of backend change could reach production without enough safeguards. After that I changed the process so it would not happen the same way again.

### C. Tell me about a time you had a conflict

Safest story:
- `Gold Blast ownership`
- or `Mirage pivots`

Suggested framing:
- difference in priorities, not personal drama
- quality vs speed
- product ambition vs technical sustainability

#### Short version

A common type of conflict for me is not personal conflict, but priority conflict. For example on Gold Blast, I had to push for analytics, hot-config support, and edge-case handling even when some people naturally wanted to focus only on visible feature work. I tried to handle that by making the tradeoff clear: if we want a calm launch, we need the operational side too. In the end we aligned and shipped without post-release hotfixes, so that was a good example of resolving tension through clarity rather than ego.

### D. Tell me about a time you failed as a manager

Safest story:
- `Mirage exits`

Recommended angle:
- not "I failed by firing people"
- better: "I waited too long to accept the gap"

#### Short version

One hard lesson for me as a manager was around exits at Mirage. In a few cases, especially with expensive senior hires, I was a bit too patient at first because I wanted to give people a fair chance. The result was that the team carried some avoidable cost and delivery drag longer than ideal. I eventually made the calls, including one case after a one-month PIP, but the lesson for me was that compassion should not become avoidance. As a manager, protecting the team also means acting when the gap is clear.

### E. Tell me about a time you missed something important

Safest story:
- `Ankr process`

#### Short version

At Ankr Core Infrastructure, one thing I realized was that the team had accepted weak estimation habits for too long. It was not one big failure, but it was still an important miss because sprint work kept rolling over and that reduces trust in delivery. Once I saw how systematic it was, I changed the rules around decomposition, testing estimates, and HLD prereads. The lesson was that repeated small misses in process can become a real delivery problem if you normalize them.

## Simple Bridges Back to Riot

At the end of an answer, add one sentence like:

- `I think that maps well to Riot because player trust really matters in live games.`
- `That is why I care a lot about quality and calm launches.`
- `That experience is a big part of why I like manager roles where I can help both people and delivery.`
- `I think Riot is the kind of place where that mix of technical depth and team leadership is useful.`

## Questions I Still Need From You

To make the negative answers stronger, I still need just one thing:

- In Mirage, if you look back honestly, what is one decision you would make earlier or differently?

That one answer will make the `failure` story much stronger and more believable.
