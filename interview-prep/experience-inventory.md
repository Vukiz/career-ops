# Experience Inventory

Use this file as the raw capture layer for your career history. Dump facts here first, even if they are messy, incomplete, out of order, or repetitive.

This file is intentionally allowed to be long. The goal is completeness, not polish.

## How to use it

1. Add one experience at a time under `## Entries`.
2. Start with a short summary so future sessions can triage quickly.
3. Put the messy details under `Raw Notes`.
4. When an entry is strong enough, promote its best material into:
   - `interview-prep/experience-summary.md` for compact recall
   - `interview-prep/story-bank.md` for polished STAR+R interview stories

## Entry Template

```markdown
### YYYY or YYYY-YYYY — Company / Team / Context
**Short Summary:** 2-4 sentences covering scope, your role, and why it matters.
**Role Lens:** Engineering Manager | Software Engineer | Tech Lead | Founder | Other
**Themes:** leadership, execution, architecture, scaling, hiring, conflict, ambiguity
**Key Outcomes:** metric 1; metric 2; metric 3
**Reusable For:** tell me about yourself; biggest impact; failure; conflict; leadership; influencing without authority

**Raw Notes:**
- What was broken or needed?
- What did you own directly?
- What decisions did you make?
- Who did you influence?
- What tradeoffs did you navigate?
- What changed because of your work?
- What was hard, messy, or politically sensitive?
- What would you do differently now?

**Evidence / Artifacts:**
- Names of systems, projects, launches, incidents, migrations, org changes
- Metrics, team sizes, dates, partners, stakeholders
```

## Entries

<!-- Add raw experience entries below this line. -->

### 2019-2021 - Playvision / Durak Online + new international product
**Short Summary:** Joined Playvision as a Unity developer on Durak Online, a live production game with about 1 million players and up to 30,000 concurrent users, and later received a formal promotion to Lead Developer as both my title and scope expanded. Over time, I took ownership of a mature legacy monolithic codebase, improved product stability and code quality, standardized workflows, and partnered closely with design and stakeholders on feature delivery. As Lead, I also began mentoring, helping with hiring, planning tasks and roadmap work, and refining team processes. Later, I moved onto a new strategic product and designed the initial architecture and core functionality so the team could scale development on top of it, with some of that architecture later informing derivative products.
**Role Lens:** Software Engineer -> Tech Lead / Lead Developer
**Themes:** legacy modernization, live operations, technical leadership, mentoring, cross-functional collaboration, performance, architecture
**Key Outcomes:** launched roughly a dozen new features; shipped a full UI overhaul; reduced game load times from up to 30 seconds to roughly 1-2 seconds; moved the project from a monolithic legacy codebase toward a maintainable structure; created architecture for a new core product
**Reusable For:** tell me about yourself; most impactful project; improving a legacy system; mentoring others; influencing cross-functional partners; building foundations for a new product

**Raw Notes:**
- Started as an IC Unity developer maintaining and extending Durak Online in live production.
- Worked in a codebase that had accumulated years of technical debt across multiple contributors.
- Received a formal promotion to Lead Developer as ownership and scope increased.
- Took responsibility for engineering processes, critical bug resolution, and some server-side issue fixing in TypeScript.
- Before becoming Lead, I was mostly focused on task execution; after promotion I became involved in mentoring, hiring, planning tasks, roadmap participation, and process refinement.
- Mentored and guided new hires, especially juniors, in a way that let them contribute meaningfully without removing the learning process.
- One specific junior example: a smart but shy university graduate lacked confidence and hesitated to take ownership. I coached him on taking responsibility, standing up for his decisions, and reading the right materials to avoid repeat mistakes and write better code. He developed into a confident middle engineer who could take on serious work independently.
- That junior later progressed from small single-file tasks into owning an entire hypercasual game project solo, taking it from scratch through a production release in about two weeks.
- Collaborated heavily with stakeholders and design; used both technical constraints and personal player empathy to improve feature decisions.
- Established CI/CD pipelines and tests.
- Improved the developer and QA loop by making manual QA easier and faster.
- Standardized development workflows to improve engineering efficiency and delivery consistency.
- Delivered many features and a complete UI overhaul while keeping a live game running.
- Reduced load times from up to 30 seconds down to roughly 1-2 seconds.
- The key technical change behind the load-time improvement was replacing a monolithic sequential startup flow with parallelized loading steps, while delaying and retrying non-critical work instead of blocking startup.
- Reworked the codebase from a legacy monolith into a more maintainable system that newer developers could work in safely.
- One major production incident happened shortly after I became Lead Developer: a backend rollout caused many players not to receive rewards for game wins.
- The incident stayed live for roughly 3-4 hours and affected around 1,000 players, all of whom were later reimbursed.
- I took the lead during the incident, directed backend to roll back immediately, asked QA to collect affected user IDs, and coordinated player communication so we could reassure users that reimbursements would happen.
- After the incident, I changed the process: no direct backend rollouts to production without QA approval on a test stand, contract updates had to be published to shared chat plus documentation, and I pushed for additional backend tests.
- This later informed my push toward protobuf contracts with versioning to make integrations safer.
- Later moved onto a new strategic product intended to become a core international product for the company.
- Designed the architecture and implemented core functionality for that new project to make further expansion easier.
- Used a self-built MVVM architecture with auto code generation to decouple views from logic and support autotesting.
- Enabled a separate test-focused contributor to reuse views with custom view models for test scenarios.
- Introduced protobuf as a serialized contract with the backend to reduce server update issues and allow safe gradual migration.
- Parts of the architecture were reusable enough to support derivative products.

**Evidence / Artifacts:**
- Durak Online
- Player scale: about 1 million players, up to 30,000 online
- Team shape: 2-3 QA, 2 designers, 1 backend engineer, 3-4 Unity developers on my team, plus another 4 Unity developers on a neighboring team that I also helped mentor
- Unity client codebase
- Server issue debugging in TypeScript
- CI/CD setup
- Test coverage improvements
- UI overhaul
- Formal promotion to Lead Developer
- Participation in hiring and roadmap/process work
- Production rollback / missing rewards incident
- Self-built MVVM with auto code generation
- Protobuf contracts with backend
- New strategic international product architecture
- Need confirmation later: names of highest-impact features, approximate player scale, the specific derivative products this architecture informed

### 2021-2022 - Playtika / Solitaire Grand Harvest
**Short Summary:** Joined Playtika as a Senior Developer after the company acquired Solitaire Grand Harvest, which still ran on a legacy Murl Engine codebase in C++. The initial goal was to port the game fully into Unity so it remained indistinguishable for players while becoming much more maintainable for the team. After getting deep enough into the codebase, I was promoted to Key Developer and started owning high-level design for new features, while also mentoring engineers, supporting live operations, and helping the team work more effectively in an enterprise environment. One of the strongest outcomes was launching a new minigame successfully in about three months without post-launch hotfixes, and another was resolving a production crash affecting high-level players by finding and fixing a memory leak.
**Role Lens:** Senior Software Engineer -> Key Developer
**Themes:** legacy migration, feature architecture, live operations, cross-functional planning, mentoring, onboarding, enterprise delivery
**Key Outcomes:** ported major parts of a C++ game into Unity; promoted from Senior Developer to Key Developer; led HLD for a new minigame and reusable systems that shipped successfully in about 3 months without hotfixes; fixed a production crash affecting high-level players by identifying a memory leak; improved onboarding with project documentation
**Reusable For:** porting legacy systems; feature ownership; working across product and engineering; mentoring engineers across technology shifts; supporting live operations in enterprise environments

**Raw Notes:**
- Joined Playtika after acquisition of Solitaire Grand Harvest.
- The original game had been built on Murl Engine in C++.
- Main initial goal was a full Unity port that players would not perceive as different from the original, while making the game much easier to maintain.
- Spent a lot of time reading legacy C++ code and porting it into Unity/C#.
- The hardest part of the port was often not algorithmic difficulty but preserving context and fidelity in a codebase optimized for fast delivery rather than maintainability.
- UI-heavy features such as the game shop were especially difficult because interactions and transitions had to stay pixel-perfect and behave exactly like the original.
- Tech artists helped a lot by building tools for developers and integrators, which made fidelity and iteration more manageable.
- After becoming familiar enough with the codebase, I was promoted to Key Developer.
- As Key Developer, I owned HLD for a new feature: a Whack-a-Mole style minigame.
- The minigame required meaningful groundwork beyond feature logic, including reusable systems such as a badge system that other teams could also build on.
- Had many conversations with product to ensure analytics coverage, hot-config reload support, and edge cases were handled for a safe launch.
- The minigame launched successfully in about 3 months from planning to production release, including design assets, SFX, VFX, backend, and client work.
- The launch did not require hotfixes afterward.
- The feature was called Gold Blast / Catch the Mole and received a lot of positive player comments.
- I also actively guided backend developers on client-server communication best practices: reducing unnecessary data transfer, optimizing server calls, and moving non-critical processing to the client.
- Took part in on-call rotations.
- During on-call weeks, spent significant time fixing tech debt and shipping hotfixes for live production issues.
- One specific production issue involved crashes for very high-level players on a scrollable world map with around 10,000 levels.
- I investigated, profiled, and benchmarked the issue, found a memory leak, fixed it, improved overall map scrolling performance, and added tests to cover it.
- Beyond coding, actively participated in team processes and helped manage junior and mid-level developer load.
- Helped the project manager distribute workload more effectively.
- Mentored junior developers.
- Helped senior C++ engineers adapt to C#, Unity workflows, profiling, performance traps, and engine-specific nuances.
- Created Confluence documentation with project-specific details to improve developer onboarding.
- That documentation became the go-to onboarding reference and reduced repetitive explanatory conversations.

**Evidence / Artifacts:**
- Solitaire Grand Harvest
- Team shape: around 8 developers per team, plus 1 project/team leader, 2-3 QA, 1 occasional backend developer, and 1-2 integrators
- Legacy Murl Engine C++ codebase
- Unity porting work
- Promotion from Senior Developer to Key Developer
- Whack-a-Mole style minigame
- Gold Blast / Catch the Mole
- Reusable badge system groundwork
- Analytics instrumentation discussions
- Hot-config reload support
- Backend/client communication guidance
- On-call / hotfix support
- Production crash on very high levels
- Mentoring C++ engineers into Unity/C#
- Confluence onboarding documentation
- Need confirmation later: exact impact of the port, any measurable onboarding or delivery improvements beyond reduced repeated explanations

### 2022-2025 - Ankr / SDK -> Mirage Interactive -> Core Infrastructure
**Short Summary:** I joined Ankr to lead game engineering work around a web3 SDK for Unity and Unreal, where I turned a prototype wrapper into a proper open-source SDK with documentation, demos, and deeper integration with Ankr services. I was then asked to become Technical Director for Mirage Interactive, a child startup building a web3 game marketplace, where I led hiring, product and technical direction, architecture through two pivots, and broader org management including delegation, budgeting, roadmap work, and eventually difficult performance exits. After Mirage ran out of funding, I transitioned into Ankr Core Infrastructure, moved into Go, migrated legacy TypeScript Cloudflare-worker functionality into a Go platform ahead of schedule with zero production incidents, and later led a team improving scale, reliability, process quality, telemetry efficiency, and proxy performance at very high traffic volumes.
**Role Lens:** Engineering Manager + Technical Director + Software Engineering Team Lead
**Themes:** open-source engineering, startup leadership, architecture under ambiguity, people management, infra migration, scale, process transformation, reliability
**Key Outcomes:** transformed a prototype SDK into a production-grade open-source offering; led Mirage through 2 pivots to beta release; redistributed strong Mirage engineers into internal Ankr teams after shutdown; migrated legacy infra into Go 2 months ahead of plan with 0 incidents; reduced telemetry storage 10x; reduced proxy RAM from 50 GB to 5 GB per instance; supported traffic up to roughly 500k RPS; improved estimation accuracy and release discipline
**Reusable For:** building foundations from prototypes; leading through pivots; managing managers/leads and growing teams; handling layoffs/performance decisions; large-scale infrastructure migration; performance optimization; improving engineering process and release reliability

**Raw Notes:**
- Hired as Game Department Lead at Ankr.
- Rough split: about 1 year on the SDK team, about 1 year at Mirage, and 2+ years on Core Infrastructure.
- Initial responsibility was development of a web3 SDK for Unity and Unreal Engine.
- The SDK existed in prototype form and was mainly a wrapper around a third-party library when I joined.
- My first step was to turn it into a proper open-source library with enterprise-level quality while keeping it simple for developers to use.
- Team was small: 3 Unity developers and 1 Unreal developer.
- I oversaw both Unity and Unreal parts.
- We created proper documentation, onboarding, and demos.
- Implemented integration with Ankr services so users could access advanced API capabilities through the SDK.
- The SDK saw some public adoption, including roughly 40 GitHub stars.
- A major real-world use case was Meta Apes, which used the SDK as a core library for web interactions and generated millions in revenue.
- Later I was offered to lead a child startup of Ankr called Mirage Interactive as Technical Director.
- Mirage was building a web3 gaming marketplace, roughly like Steam for web3 games, with tokenomics, NFTs, and other web3-specific requirements.
- I helped establish product vision and pushed CEO/CPO thinking toward more appropriate technical usage.
- We hired 4 backend developers (.NET), 2 frontend developers, 2 QA, and 1 DevOps engineer.
- At peak, I was effectively managing around 20 people across directs and indirects.
- We worked on Mirage for about a year and got to a beta release, but the company eventually lacked funding and the project stopped.
- The product survived 2 pivots, which required major code rework close to from-scratch changes.
- One concrete pivot was moving from a pure NFT marketplace inside a gaming ecosystem toward a Steam-like marketplace that required player profiles and direct game integrations.
- Because the architecture was modular and I consistently pushed for low coupling through my own reviews and through backend/frontend leads, it was relatively straightforward to plug features in and out during pivots.
- Because I expected startup volatility, I had established a flexible architecture early, which helped us survive those pivots.
- I assigned 1 backend lead and 1 frontend lead because I needed leverage to manage everything else, including budgeting, roadmap work, and stakeholder reporting.
- I held regular 1:1s with directs and indirects and established growth plans.
- While doing this, I still retained the SDK department under my leadership.
- It was in this role that I had to fire 3 people for a combination of insufficient performance and budget constraints.
- Two exits were primarily budget-driven because expensive senior hires were not demonstrating the expected level of autonomy and seniority.
- One exit was performance-driven: a senior developer had persistent soft-skill and communication problems that led to poor delivery quality and avoidable mistakes.
- We ran a one-month PIP for that engineer, but he did not meet the agreed goals.
- After Mirage collapsed, I was transferred to the Core Infrastructure team at Ankr as a software engineer.
- I switched to Go without major difficulty.
- I vouched for strong Mirage team members so several valuable people could be redistributed into internal Ankr teams instead of losing the hiring investment.
- I worked on the Core Infrastructure team for 2+ years and became a Team Lead.
- Team size there was about 3-5 developers working on Ankr API / RPC infrastructure.
- Initially the system was enterprise-only telemetry, reverse proxy, and control plane, but over time we took over public and private traffic too.
- My task was to transfer legacy functionality from TypeScript Cloudflare workers into a Go ecosystem.
- I finished that migration 2 months earlier than estimated.
- We had 0 production incidents during that migration because of extensive autotest coverage.
- There were no dedicated QA engineers in the infrastructure team.
- We had 1-2 frontend engineers, but eventually moved from a React frontend to Go templates so backend developers could keep shipping without frontend dependency.
- I completed a SOC 2 compliance update, including audit logs and RBAC access.
- I worked extensively on telemetry services and ClickHouse optimization.
- Reduced storage space by 10x by optimizing data format and implementing streaming preaggregation and batching.
- Improved monitoring with alerts and Grafana dashboards.
- Worked on proxy improvements, increasing stability and reducing RAM usage from 50 GB to 5 GB per instance.
- Implemented hybrid caching with Redis plus in-memory caching.
- Proxy handled hundreds of thousands of RPS and occasionally hit about 500k RPS.
- As a manager, I established a measurable project roadmap and stronger development process.
- Within about 2 months after process changes, the team started hitting estimates more reliably.
- We created a reference task table for each story point estimate.
- Before the change, estimates were often assigned inconsistently and the team routinely overshot sprint commitments.
- I forbade undecomposed tasks from entering a sprint, pushed teams to finish small tasks first, required test work to be included in estimates, and required HLDs for complex features so designs could be preread and reviewed.
- I reduced the number of meetings during the sprint to improve focus time.
- Reduced hop-on calls and pushed for written asynchronous communication.
- As public traffic support grew, release discipline became more important.
- I established release highlights, feedback loops, and rollout/rollback policies.
- Backend releases were happening on a biweekly cadence.
- After the process changes, the team was able to complete sprint commitments rather than constantly transferring work into the next sprint.

**Evidence / Artifacts:**
- Ankr Unity SDK / Unreal SDK
- Open-source SDK modernization
- Small SDK team: 3 Unity developers, 1 Unreal developer
- Mirage Interactive
- Mirage staffing: 4 backend, 2 frontend, 2 QA, 1 DevOps
- 2 product pivots
- Pivot example: NFT marketplace -> Steam-like marketplace with player profiles and game integrations
- Beta release before shutdown
- Backend lead and frontend lead delegation
- 1:1s and growth plans
- Performance management / firing 3 people
- 2 budget-driven exits + 1 performance-driven exit after a 1-month PIP
- Internal talent redistribution after Mirage shutdown
- Ankr API / RPC platform
- TypeScript Cloudflare workers to Go migration
- 0 production incidents during migration
- Migration delivered 2 months ahead of estimate
- SOC 2 audit logs and RBAC
- ClickHouse storage optimization 10x
- Proxy RAM reduction 50 GB -> 5 GB per instance
- Hybrid caching with Redis + in-memory cache
- Traffic scale: hundreds of thousands of RPS, peaks around 500k RPS
- Process changes: estimation model, reduced meetings, async communication, release policy
- SDK adoption: roughly 40 GitHub stars; Meta Apes used it as a core web interaction library
- Biweekly backend release cadence
- Need confirmation later: size of indirect org at Mirage; whether Mirage beta had any notable user/adoption signal beyond reaching beta
