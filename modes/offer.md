# Mode: offer

When the user pastes a job description or job URL, always produce the six core blocks below.

## Step 0: Archetype detection

Classify the role into one of the six archetypes from `modes/_shared.md`. If it is genuinely hybrid, name the two closest archetypes.

Use that classification to decide:
- which proof points to emphasize,
- how to rewrite the summary,
- which interview stories to lead with.

## Block A: Role summary

Provide a table with:
- detected archetype,
- domain,
- function,
- seniority,
- remote policy,
- team size if stated,
- a one-sentence TL;DR.

## Block B: CV match

Read `cv.md` and map each important JD requirement to exact evidence from the CV.

Also include:
- strongest matches,
- missing pieces,
- whether each gap is a blocker or a nice-to-have,
- a concrete mitigation plan for every meaningful gap.

## Block C: Level and strategy

Cover:
1. The level implied by the JD vs the candidate's natural level.
2. How to present seniority honestly.
3. What to do if the company downlevels the role.

## Block D: Compensation and demand

Use web research for:
- current salary ranges,
- company compensation reputation,
- demand signals for the role.

If hard data is missing, say that directly.

## Block E: Personalization plan

Provide a table:

| # | Section | Current state | Proposed change | Why |
|---|---------|---------------|-----------------|-----|

Then summarize:
- top 5 resume changes,
- top 5 LinkedIn changes.

## Block F: Interview plan

Map 6-10 JD requirements to STAR+R stories:

| # | JD requirement | Story | S | T | A | R | Reflection |
|---|----------------|-------|---|---|---|---|------------|

Also include:
- the single best case study to present,
- likely red-flag questions,
- how to answer them directly.

If `interview-prep/story-bank.md` exists, append new reusable stories that are not already there.

## After the evaluation

Always:
1. Save the report to `reports/{###}-{company-slug}-{YYYY-MM-DD}.md`.
2. Include `**Date:**`, `**Archetype:**`, `**Score:**`, `**URL:**`, and `**PDF:**` in the header.
3. Write a tracker TSV addition in `batch/tracker-additions/` using canonical English statuses.

## Report format

```markdown
# Evaluation: {Company} - {Role}

**Date:** {YYYY-MM-DD}
**Archetype:** {detected}
**Score:** {X/5}
**URL:** {job URL}
**PDF:** {path or pending}

---

## A) Role Summary
## B) CV Match
## C) Level and Strategy
## D) Compensation and Demand
## E) Personalization Plan
## F) Interview Plan
## G) Draft Application Answers

---

## Extracted Keywords
```

Use `## G)` only when the score justifies drafting application answers.
