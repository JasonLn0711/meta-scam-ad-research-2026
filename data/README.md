# Data Directory

This directory defines the data layout. Do not commit raw sensitive evidence.

## Subdirectories

```text
raw/          Original approved data, local only unless explicitly cleared
interim/      Normalized or partially processed data, local only by default
processed/    Derived analysis-ready tables, local only by default
annotations/  Label files and reviewer exports, local only unless redacted
synthetic/    Synthetic or toy examples for pipeline testing
external/     Public reference datasets or source snapshots, local only by default
```

## Default Rule

Only governance docs, schemas, synthetic toy examples, and redacted samples should be committed. Real case evidence requires explicit approval recorded in `governance/data-governance.md`.

## Minimum Evidence Record

See `docs/03-data-strategy.md` for required fields.
