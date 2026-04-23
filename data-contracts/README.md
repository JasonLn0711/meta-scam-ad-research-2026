# Data Contracts

Stable dataset schemas and evidence field definitions live here.

This folder is the bridge between domain experts, annotators, and engineers. It should make the data shape explicit before code is written.

## Files

```text
evidence-field-dictionary.md
evidence-record-schema.md
dataset-manifest-schema.md
annotation-record-schema.md
```

## Contract Rule

If an experiment relies on a field, that field should be defined here first.

If a stakeholder cannot provide a required field, mark it as optional or gated rather than silently assuming it exists.
