# Mode: pipeline

Process the queued URLs in `data/pipeline.md`.

## Workflow

1. Read the `## Pending` section and find every `- [ ]` item.
2. For each pending item:
   - compute the next report number,
   - extract the JD,
   - run the full auto-pipeline,
   - generate the PDF when the role scores `>= 3.0`,
   - move the item to `## Processed` with report number, score, and PDF status.
3. If a URL is inaccessible, mark it as `- [!]` with a short note and continue.
4. If there are three or more pending URLs, parallelize where possible.
5. End with a summary table.

## Example format

```markdown
## Pending
- [ ] https://jobs.example.com/posting/123
- [ ] https://boards.greenhouse.io/company/jobs/456 | Company Inc | Senior PM
- [!] https://private.url/job | login required

## Processed
- [x] #143 | https://jobs.example.com/posting/789 | Acme Corp | AI PM | 4.2/5 | PDF ✅
```

## JD extraction order

1. Playwright
2. WebFetch
3. WebSearch

Special cases:
- LinkedIn often needs login. Ask the user to paste the text if needed.
- `local:` paths should be read from disk directly.
- PDF URLs should be read as PDFs.

Before processing, run `node cv-sync-check.mjs` and warn the user if the core files are out of sync.

## Numbering

Determine the next report number by scanning `reports/`, extracting the numeric prefix from existing files, and adding one.
