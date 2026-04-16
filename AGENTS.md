# Career-Ops for Codex

## Purpose

This repository is a Codex-operated career pipeline. Use the mode files, scripts, templates, and data layout here as the working contract for job-search operations.

Ignore Claude-specific entrypoints, slash commands, hooks, and batch-worker flows unless the user explicitly asks to preserve or adapt them. Batch mode can remain untouched.

## Data Contract

Read `DATA_CONTRACT.md` before making changes.

Two layers matter:
- User layer: `cv.md`, `config/profile.yml`, `modes/_profile.md`, `article-digest.md`, `portals.yml`, `data/*`, `reports/*`, `output/*`, `interview-prep/*`, `jds/*`
- System layer: `modes/*` except `_profile.md`, `AGENTS.md`, scripts, templates, dashboard, docs

Rules:
- Put user-specific customization in `cv.md`, `config/profile.yml`, `modes/_profile.md`, `article-digest.md`, or the `interview-prep/` files.
- Do not write user-specific content into shared system prompts such as `modes/_shared.md`.
- Do not overwrite user-layer files with template/example content unless the user asks.

## Session Start

At the start of repository work:

1. Read `DATA_CONTRACT.md`.
2. Check core setup:
   - `cv.md`
   - `config/profile.yml`
   - `modes/_profile.md`
   - `portals.yml`
3. Run `node cv-sync-check.mjs` before pipeline execution when those files are expected to exist.
4. If required setup is missing, stop pipeline execution and fix onboarding first.

If `_profile.md` is missing and the user wants onboarding completed, create it from `modes/_profile.template.md`.

## Codex Operating Rules

- Never invent experience, metrics, credentials, or links.
- Keep outputs in English unless the user asks otherwise.
- Always include `**URL:**` in report headers.
- Always use canonical tracker statuses:
  - `Evaluated`
  - `Applied`
  - `Responded`
  - `Interview`
  - `Offer`
  - `Rejected`
  - `Discarded`
  - `SKIP`
- Never submit a live application without explicit user review.
- Never write directly into `data/applications.md` during evaluation flows; write TSV additions into `batch/tracker-additions/` and merge with `node merge-tracker.mjs`.
- For compensation work, use this order:
  1. read `data/compensation.md`,
  2. use the closest stored company or role-family anchor as the base point,
  3. only if no usable anchor exists, do live salary research,
  4. append the new benchmark or company note back into `data/compensation.md`.

## Tooling

- Prefer local repo scripts when they already exist.
- Use Playwright for job-page verification and extraction before weaker fallbacks.
- For current web facts such as compensation or whether a job is still live, verify with browsing.
- Use `generate-pdf.mjs` for HTML-to-PDF generation.

Preferred JD extraction order:
1. Playwright
2. Direct page fetch or local file read
3. Search only as a discovery fallback, not final verification

## Mode Map

Use these files as the task-level operating prompts:

| Intent | File |
|--------|------|
| Evaluate one role | `modes/offer.md` |
| Compare roles | `modes/compare.md` |
| Generate outreach | `modes/outreach.md` |
| Research a company | `modes/deep.md` |
| Generate a PDF | `modes/pdf.md` |
| Evaluate training | `modes/training.md` |
| Evaluate a project | `modes/project.md` |
| Check tracker status | `modes/tracker.md` |
| Draft application answers | `modes/apply.md` |
| Scan portals | `modes/scan.md` |
| Process queued URLs | `modes/pipeline.md` |

Batch mode exists in the repo but is not part of the default Codex workflow.

## Reports and Tracker

Report path:
- `reports/{###}-{company-slug}-{YYYY-MM-DD}.md`

Tracker TSV line format:

```text
{num}\t{date}\t{company}\t{role}\t{status}\t{score}/5\t{pdf_emoji}\t[{num}](reports/{num}-{slug}-{date}.md)\t{note}
```

After evaluation runs that create tracker additions, use:

```bash
node merge-tracker.mjs
node verify-pipeline.mjs
```

Useful integrity commands:

```bash
node normalize-statuses.mjs
node dedup-tracker.mjs
node cv-sync-check.mjs
```

## Practical Notes

- `cv.md` is the source of truth for resume tailoring.
- `data/compensation.md` is the compensation memory layer. Read it before doing fresh salary research, and use web research only to fill gaps or refresh stale market data.
- `interview-prep/experience-inventory.md` is the raw fact layer.
- `interview-prep/experience-summary.md` and `interview-prep/story-bank.md` are the recall layers for interview and application work.
- `config/profile.yml` remains the main identity/target-role config and still needs to exist for the full pipeline.
