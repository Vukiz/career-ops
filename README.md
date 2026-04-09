# Career-Ops

AI-powered job search operations for Claude Code. Evaluate roles, generate tailored resumes, scan portals, and keep a clean application tracker.

![Claude Code](https://img.shields.io/badge/Claude_Code-000?style=flat&logo=anthropic&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)

<p align="center">
  <img src="docs/demo.gif" alt="Career-Ops Demo" width="800">
</p>

## What it does

Career-Ops turns Claude Code into a job-search command center:

- Evaluate roles with a structured A-F framework
- Generate ATS-friendly tailored PDFs
- Scan job portals and queue new opportunities
- Process roles in batch with isolated workers
- Keep reports, PDFs, and tracker entries in sync

This is a filter, not a spray-and-pray tool. The goal is to help you spend time on the few roles worth serious effort.

## Quick start

```bash
git clone https://github.com/santifer/career-ops.git
cd career-ops
npm install
npx playwright install chromium

cp config/profile.example.yml config/profile.yml
cp templates/portals.example.yml portals.yml
```

Then:
1. Create `cv.md` in the repo root.
2. Open Claude Code in this directory.
3. Ask Claude to personalize the system for your target roles.
4. Paste a job URL or run `/career-ops`.

See [docs/SETUP.md](docs/SETUP.md) for the full setup flow.

## Commands

```text
/career-ops                show commands
/career-ops {job URL}      run the full pipeline
/career-ops scan           scan job portals
/career-ops pdf            generate a tailored PDF
/career-ops batch          batch-process queued roles
/career-ops tracker        inspect application status
/career-ops apply          draft live form answers
/career-ops pipeline       process queued URLs
/career-ops outreach       generate LinkedIn outreach
/career-ops deep           build a research brief
/career-ops compare        compare multiple roles
/career-ops training       evaluate a course or certification
/career-ops project        evaluate a portfolio project
```

## Key features

| Feature | Description |
|---------|-------------|
| Auto-pipeline | URL in, report + PDF + tracker entry out |
| Interview planning | STAR+R story generation and story-bank accumulation |
| Portal scanning | Preconfigured companies and queries across major ATSs |
| Batch processing | Parallel `claude -p` workers with resumable state |
| Dashboard TUI | Browse, filter, and update your pipeline in the terminal |
| Integrity scripts | Merge, dedup, normalize, and verify tracker data |

## Project structure

```text
career-ops/
├── CLAUDE.md
├── cv.md
├── article-digest.md
├── config/
├── modes/
│   ├── _shared.md
│   ├── offer.md
│   ├── pdf.md
│   ├── scan.md
│   ├── batch.md
│   └── ...
├── templates/
├── batch/
├── dashboard/
├── data/
├── reports/
├── output/
├── docs/
└── examples/
```

## Dashboard

```bash
cd dashboard
go build -o career-dashboard .
./career-dashboard
```

The dashboard supports filtering, sorting, grouped and flat views, report previews, and inline status updates.

## Notes

- This fork is English-only.
- Tracker statuses are canonical English values: `Evaluated`, `Applied`, `Responded`, `Interview`, `Offer`, `Rejected`, `Discarded`, `SKIP`.
- User data lives in the user layer described in [DATA_CONTRACT.md](DATA_CONTRACT.md) and is not touched by system updates.

## License

MIT
