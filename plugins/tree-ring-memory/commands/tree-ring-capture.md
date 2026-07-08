---
description: Capture a concise validated lesson decision warning or preference in Tree Ring Memory
argument-hint: "<memory summary>"
allowed-tools: ["Bash"]
---

# Tree Ring Capture

Capture only durable, useful memory. Do not store transcripts, secrets,
credentials, raw chain-of-thought, or unverified claims as truth.

Use the user's argument as the memory summary:

```bash
tree-ring remember "$ARGUMENTS" \
  --event-type lesson \
  --scope project
```

Adjust `--event-type`, `--project`, and `--tag` values to match the actual
memory:

- `decision` for selected architecture, release, storage, or policy choices
- `lesson` for validated work patterns
- `warning` for failures and regressions to avoid
- `preference` for durable user preferences
- `seed` for future work that should be revisited

If the memory comes from a run, test, evaluation, incident, PR, or checkpoint,
prefer `tree-ring evidence` with an `--evidence-ref` and outcome.
