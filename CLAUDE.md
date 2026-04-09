# Career-Ops Agent Instructions

## Purpose

Career-Ops is an AI-assisted job search system built on Claude Code. The system evaluates roles, generates tailored PDFs, scans portals, tracks applications, and helps with interview prep.

This fork is English-only. Do not produce or preserve Spanish or German modes, prompts, tracker states, or docs.

## Data contract

Read `DATA_CONTRACT.md`.

Two layers matter:
- User layer: `cv.md`, `config/profile.yml`, `modes/_profile.md`, `article-digest.md`, `portals.yml`, `data/*`, `reports/*`, `output/*`, `interview-prep/*`
- System layer: `modes/*` except `_profile.md`, `CLAUDE.md`, scripts, templates, dashboard, batch files, docs

Rule:
- Put user-specific customization in `modes/_profile.md` or `config/profile.yml`.
- Do not write user-specific content into `modes/_shared.md`.

## Session start

Silently run:

```bash
node update-system.mjs check
```

If an update is available, ask the user before applying it.

Then silently verify setup:
1. `cv.md`
2. `config/profile.yml`
3. `modes/_profile.md`
4. `portals.yml`

If `_profile.md` is missing, copy it from `modes/_profile.template.md`.

If required files are missing, stop and onboard the user before running other modes.

## Onboarding

If `cv.md` is missing:
- ask for the CV, LinkedIn URL, or a summary of experience,
- create a clean markdown CV.

If `config/profile.yml` is missing:
- copy from `config/profile.example.yml`,
- collect name, contact details, location, timezone, target roles, and comp range,
- fill the file in.

If `portals.yml` is missing:
- copy from `templates/portals.example.yml`,
- adapt search keywords to the target roles.

If `data/applications.md` is missing, create:

```markdown
# Applications Tracker

| # | Date | Company | Role | Score | Status | PDF | Report | Notes |
|---|------|---------|------|-------|--------|-----|--------|-------|
```

After setup, ask for more context:
- standout strengths,
- work that energizes or drains,
- deal-breakers,
- best professional achievement,
- published projects or proof points.

Store that in `config/profile.yml`, `modes/_profile.md`, or `article-digest.md`.

## Mode map

| User intent | Mode file |
|-------------|-----------|
| Evaluate one role | `modes/offer.md` |
| Compare roles | `modes/compare.md` |
| Generate outreach | `modes/outreach.md` |
| Research a company | `modes/deep.md` |
| Generate a PDF | `modes/pdf.md` |
| Evaluate training | `modes/training.md` |
| Evaluate a project | `modes/project.md` |
| Check the tracker | `modes/tracker.md` |
| Fill an application form | `modes/apply.md` |
| Scan for new roles | `modes/scan.md` |
| Process queued URLs | `modes/pipeline.md` |
| Batch-process roles | `modes/batch.md` |

## Global rules

- Never invent experience, metrics, or credentials.
- Never submit an application without explicit user review.
- Never hardcode proof-point metrics; read them from the user files.
- Never create a new tracker entry directly in `applications.md`; write TSV additions in `batch/tracker-additions/`.
- Always include `**URL:**` in report headers.
- Always use canonical English tracker statuses.
- Always keep outputs in English.

## Tracker and reports

Tracker TSV additions use:

```text
{num}\t{date}\t{company}\t{role}\t{status}\t{score}/5\t{pdf_emoji}\t[{num}](reports/{num}-{slug}-{date}.md)\t{note}
```

Canonical statuses:
- `Evaluated`
- `Applied`
- `Responded`
- `Interview`
- `Offer`
- `Rejected`
- `Discarded`
- `SKIP`

After batch evaluations, run:

```bash
node merge-tracker.mjs
```

Useful integrity commands:

```bash
node verify-pipeline.mjs
node normalize-statuses.mjs
node dedup-tracker.mjs
node cv-sync-check.mjs
```

## Offer verification

Do not trust search snippets to verify whether a role is still live.

Preferred order:
1. Playwright
2. WebFetch
3. WebSearch as a fallback for discovery, not final verification

In batch worker mode where Playwright is unavailable, mark verification as unconfirmed.
