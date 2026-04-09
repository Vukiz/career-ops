# Mode: scan

Scan configured job portals, filter for relevant titles, and add new roles to `data/pipeline.md`.

## Configuration

Read `portals.yml`:
- `search_queries`
- `tracked_companies`
- `title_filter`

## Discovery order

1. Direct Playwright scan of each `careers_url`
2. Greenhouse API when configured
3. WebSearch queries for broad discovery

Run all three layers, merge results, then deduplicate.

## Workflow

1. Read `portals.yml`.
2. Read `data/scan-history.tsv`.
3. Read `data/applications.md` and `data/pipeline.md` for deduping.
4. Run the Playwright layer first:
   - open each enabled `careers_url`,
   - read every visible listing,
   - walk relevant department filters when the page separates teams,
   - paginate when more results exist,
   - if a `careers_url` is broken, fall back to search and note that the URL should be updated.
5. Run the Greenhouse API layer for companies that define `api:`.
6. Run the broad WebSearch layer for enabled `search_queries`.
7. Merge results from all layers.
8. Filter titles:
   - at least one positive keyword,
   - no negative keywords,
   - seniority boost terms raise priority.
9. Deduplicate against scan history, tracker, and pipeline.
10. For each new role:
   - append `- [ ] {url} | {company} | {title}` to `## Pending` in `pipeline.md`,
   - append an `added` row to `scan-history.tsv`.
11. Record filtered-out items as `skipped_title` and duplicates as `skipped_dup`.

## Search-result parsing

When parsing broad search results, extract company and title from common formats such as:
- `Role @ Company`
- `Role | Company`
- `Role - Company`
- `Role at Company`

Use the title before the separator as the role and the text after it as the company.

## URL handling

If a URL is private or only readable after login:
1. Save the JD to `jds/{company}-{role-slug}.md`.
2. Add `local:jds/{company}-{role-slug}.md | {company} | {title}` to the pipeline.

## `careers_url` maintenance

Each tracked company should have a direct `careers_url`.

If one is missing:
1. Try the expected ATS pattern.
2. Fall back to a quick search for the company's careers page.
3. Confirm the page works.
4. Save the discovered URL back into `portals.yml` for future scans.

If an existing `careers_url` now redirects or fails:
1. Note it in the scan summary.
2. Use search as a fallback for this run.
3. Mark the config for update.

## Output summary

Provide:
- number of queries run,
- total roles found,
- relevant roles after filtering,
- duplicates skipped,
- new roles added to the pipeline.
