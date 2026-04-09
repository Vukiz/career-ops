# Mode: auto-pipeline

When the user pastes a JD or job URL without an explicit sub-command, run the full flow:

1. Extract the JD.
2. Evaluate it with `modes/offer.md`.
3. Save the report in `reports/`.
4. Generate the tailored PDF with `modes/pdf.md`.
5. If the score is `>= 4.5`, draft application answers and append them as `## G) Draft Application Answers`.
6. Write a tracker TSV addition with report and PDF references.

## JD extraction order

If the input is a URL:
1. Playwright first for SPA job boards.
2. WebFetch for static pages.
3. WebSearch as a last resort.

If none work, ask the user to paste the JD or share a screenshot.

If the user pasted the JD text directly, use it as-is.

## Draft application answers

Use a confident, selective tone. The stance is: the candidate is choosing this company for specific reasons, not begging for a chance.

Guidelines:
- 2-4 sentences per answer.
- Reference something concrete from the JD or company.
- Ground every claim in real candidate evidence.
- Avoid filler and generic enthusiasm.

Fallback questions if you cannot inspect the form:
- Why are you interested in this role?
- Why this company?
- Tell us about a relevant project or achievement.
- What makes you a good fit?
- How did you hear about this role?

If any step fails, continue the remaining steps and clearly mark the missing piece as pending.
