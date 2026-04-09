# Mode: pdf

Generate an ATS-friendly English resume tailored to a specific job.

## Pipeline

1. Read `cv.md`.
2. Get the JD text or URL.
3. Extract 15-20 meaningful keywords from the JD.
4. Choose page format:
   - `letter` for US/Canada
   - `a4` otherwise
5. Detect the job archetype and adjust framing.
6. Rewrite the Professional Summary using only real experience and relevant JD vocabulary.
7. Choose the top 3-4 most relevant projects.
8. Reorder experience bullets by relevance.
9. Build a competency grid with 6-8 keyword phrases.
10. Generate HTML from `templates/cv-template.html`.
11. Write HTML to `/tmp/cv-candidate-{company}.html`.
12. Run `node generate-pdf.mjs` to create the PDF in `output/`.
13. Report the output path, page count, and keyword coverage.

## ATS rules

- Single-column layout only
- Standard English section names
- No critical information in headers, footers, or images
- Selectable text, UTF-8, no rasterization
- No nested tables
- Put the most important keywords in the summary, leading bullets, and skills

## Design

- Fonts: Space Grotesk for headings, DM Sans for body
- Header: name, gradient rule, contact row
- Section titles: uppercase accent style
- Clean white background
- 0.6in margins

## Keyword injection

Only translate real experience into the JD's vocabulary. Never add skills the candidate does not have.

Legitimate reframing examples:
- "LLM workflows with retrieval" -> "RAG pipeline design and LLM orchestration workflows"
- "observability, evals, error handling" -> "MLOps and observability: evals, error handling, cost monitoring"

## Template placeholders

Populate the template with English-only content:
- `{{PAGE_WIDTH}}`
- `{{NAME}}`
- `{{EMAIL}}`
- `{{LINKEDIN_URL}}`
- `{{LINKEDIN_DISPLAY}}`
- `{{PORTFOLIO_URL}}`
- `{{PORTFOLIO_DISPLAY}}`
- `{{LOCATION}}`
- `{{SECTION_SUMMARY}}` -> `Professional Summary`
- `{{SUMMARY_TEXT}}`
- `{{SECTION_COMPETENCIES}}` -> `Core Competencies`
- `{{COMPETENCIES}}`
- `{{SECTION_EXPERIENCE}}` -> `Work Experience`
- `{{EXPERIENCE}}`
- `{{SECTION_PROJECTS}}` -> `Projects`
- `{{PROJECTS}}`
- `{{SECTION_EDUCATION}}` -> `Education`
- `{{EDUCATION}}`
- `{{SECTION_CERTIFICATIONS}}` -> `Certifications`
- `{{CERTIFICATIONS}}`
- `{{SECTION_SKILLS}}` -> `Skills`
- `{{SKILLS}}`

After generation, update the tracker row to mark PDF as `✅` if the role is already tracked.
