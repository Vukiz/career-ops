# System Context

This file is auto-updatable. Keep user-specific content in `modes/_profile.md`.

## Sources of truth

| File | When |
|------|------|
| `cv.md` | Always |
| `config/profile.yml` | Always |
| `modes/_profile.md` | Always, after this file |
| `article-digest.md` | When present |

Rules:
- Never invent metrics or experience.
- Read proof points from the files above at evaluation time.
- If `article-digest.md` and `cv.md` disagree, prefer `article-digest.md` for published project metrics.

## Scoring

Use a 1-5 global score with these dimensions:

| Dimension | What it measures |
|-----------|------------------|
| CV match | Skills, experience, proof-point fit |
| North Star fit | Alignment with target roles from `_profile.md` |
| Compensation | Market quality of pay |
| Cultural signals | Team, growth, remote policy, operating style |
| Red flags | Blockers and downside risk |

Interpretation:
- `4.5+` Strong fit. Recommend applying.
- `4.0-4.4` Good fit. Worth applying.
- `3.5-3.9` Borderline. Apply only with a clear reason.
- `<3.5` Recommend against applying.

## Archetypes

Classify each job into one primary archetype, or two if genuinely hybrid:

| Archetype | Typical JD signals |
|-----------|--------------------|
| AI Platform / LLMOps | Evals, observability, pipelines, reliability |
| Agentic / Automation | Agents, orchestration, workflows, HITL |
| Technical AI PM | Product discovery, roadmaps, PRDs, stakeholders |
| AI Solutions Architect | Architecture, enterprise, integrations, systems |
| AI Forward Deployed Engineer | Client-facing delivery, prototypes, field work |
| AI Transformation Lead | Adoption, enablement, org change, scale |

After classifying, use `_profile.md` to choose the best framing and proof points.

## Global rules

Never:
1. Modify `cv.md` or portfolio source files as part of an evaluation.
2. Submit an application for the user.
3. Share the user's phone number in outreach copy.
4. Generate a PDF before reading the JD.
5. Skip tracker/report updates after an evaluation.
6. Write anything except English in this fork.

Always:
1. Read `cv.md`, `_profile.md`, and `article-digest.md` before evaluating.
2. Run `node cv-sync-check.mjs` before the first evaluation of a session.
3. Cite exact CV evidence when matching requirements.
4. Use web research for comp and company context.
5. Write tracker additions as TSV files in `batch/tracker-additions/`; do not add rows to `applications.md` directly.
6. Include `**URL:**` in every report header.
7. Use direct, specific, fluent technical English.
8. Prefer shipping a strong application quickly over perfecting a weak one.

## Tool guidance

| Tool | Use |
|------|-----|
| WebSearch | Compensation, company context, contact discovery |
| WebFetch | Static-page JD extraction fallback |
| Playwright | Offer verification and SPA job pages |
| Read | CV, profile, article digest, templates |
| Write/Edit | Reports, tracker TSVs, temporary HTML |
| Bash | `node generate-pdf.mjs`, pipeline scripts |
