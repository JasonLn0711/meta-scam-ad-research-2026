# Dataset Manifest Schema

Every dataset slice used in an experiment should have a manifest.

## Manifest Fields

| Field | Required | Description |
|---|---|---|
| `dataset_id` | yes | Stable dataset slice ID |
| `created_date` | yes | Date created |
| `owner` | yes | Person/team responsible |
| `authorization_basis` | yes | Why this dataset may be used |
| `source_types` | yes | Stakeholder, manual, API, synthetic, weak-label |
| `item_count` | yes | Number of records |
| `content_forms` | yes | Included modalities/surfaces |
| `scam_families` | recommended | Included scam taxonomy categories |
| `benign_comparator_strategy` | recommended | How negatives were selected |
| `known_biases` | yes | Sampling and label limitations |
| `allowed_experiments` | yes | What this dataset may be used for |
| `disallowed_uses` | yes | What this dataset may not be used for |
| `retention_rule` | yes | Retention/deletion expectation |
| `redaction_status` | yes | Redacted, raw, synthetic, mixed |

## Manifest Template

```yaml
dataset_id:
created_date:
owner:
authorization_basis:
source_types:
item_count:
content_forms:
scam_families:
benign_comparator_strategy:
known_biases:
allowed_experiments:
disallowed_uses:
retention_rule:
redaction_status:
```
