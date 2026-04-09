# Mode: batch

Use batch mode when processing a list of already-collected job URLs at scale.

## Architecture

The conductor gathers URLs and JD text, then launches isolated `claude -p` workers. Each worker produces:
1. A report in `reports/`
2. A tailored PDF in `output/`
3. A tracker TSV addition in `batch/tracker-additions/`
4. JSON on stdout for state tracking

## Files

```text
batch/
  batch-input.tsv
  batch-state.tsv
  batch-runner.sh
  batch-prompt.md
  logs/
  tracker-additions/
```

## Conductor flow

1. Read `batch-state.tsv`.
2. For each pending URL, save the JD to `/tmp/batch-jd-{id}.txt`.
3. Compute the next report number.
4. Run a worker with `batch/batch-prompt.md`.
5. Update state, save logs, continue.
6. Merge tracker additions when the run ends.

## Standalone runner

```bash
batch/batch-runner.sh [OPTIONS]
```

Supported options:
- `--dry-run`
- `--retry-failed`
- `--start-from N`
- `--parallel N`
- `--max-retries N`

## Reliability rules

- `batch-state.tsv` is the source of truth for resumability.
- Workers are independent; one failure must not stop the full run.
- If PDF generation fails, keep the report and mark PDF as pending.
- Re-run with `--retry-failed` instead of duplicating completed work.
