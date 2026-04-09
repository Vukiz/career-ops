# Mode: apply

Use this when the user is actively filling out an application form.

## Workflow

1. Detect the company, role, and page context from the active browser tab, screenshot, or pasted questions.
2. Find the matching report in `reports/`.
3. Load the full report and any existing `Section G` draft answers.
4. Compare the live role to the evaluated role; if they differ, flag it before drafting answers.
5. Read every visible question and classify it by type.
6. Draft copy-paste-ready answers grounded in the report and CV.

## Inputs

Best case:
- Visible browser with Playwright.

Fallbacks:
- A screenshot of the form.
- Pasted questions.
- Company plus role name so you can locate the report.

## Drafting rules

- Reuse strong material from `Section G` when it already exists.
- Pull proof points from the report's CV-match and interview sections.
- Keep the same "I'm choosing you" tone as auto-pipeline.
- Be concrete, short, and tailored to the visible JD.
- Never invent work authorization, salary flexibility, or credentials.

## Output format

```markdown
## Application Answers — {Company} — {Role}

Based on: Report #{NNN} | Score: X.X/5 | Archetype: {type}

### 1. {Exact question}
> {Answer}

### 2. {Exact question}
> {Answer}

Notes:
- {Any mismatch or caveat}
- {Anything the user should double-check}
```

## After submission

If the user confirms they submitted:
1. Update the tracker status from `Evaluated` to `Applied`.
2. Save the final answers back into the report if useful.
3. Suggest `/career-ops outreach` as the next move.
