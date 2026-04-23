# Experiments

Use this folder for experiment logs. Each experiment should answer a narrowing decision, not merely record a model run.

## Subfolders

```text
modality-studies/   Comparisons across text, OCR, image, image+text, landing page, metadata, and video slices
baselines/          Manual rules, keyword patterns, OCR baselines, classical ML, transformer text, image baselines
evaluation-notes/   Human review notes, error analysis, evidence completeness, triage usefulness
```

## Naming Convention

```text
YYYY-MM-DD-short-experiment-name.md
```

Use `templates/experiment-log.md`, `000-template.md`, or `docs/14-experiment-tracking-template.md`.

Required fields:

- hypothesis
- dataset slice
- authorization status
- evidence fields
- pipeline
- cost
- metrics
- observations
- decision

Do not store raw sensitive data here.
