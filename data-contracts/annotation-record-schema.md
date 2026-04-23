# Annotation Record Schema

Annotation records should be separate from evidence records so labels can be revised without altering source evidence.

## Required Fields

| Field | Type | Description |
|---|---|---|
| `annotation_id` | string | Stable annotation ID |
| `case_id` | string | Links to evidence record |
| `reviewer_id` | string | Pseudonymous reviewer ID |
| `review_timestamp_utc` | string | ISO-8601 timestamp |
| `primary_label` | enum | `scam_like`, `benign`, `uncertain`, `insufficient_evidence` |
| `triage_label` | enum | `high_risk`, `medium_risk`, `low_risk` |
| `reason_codes` | array[string] | Explainable reasons |
| `reviewer_confidence` | enum | `high`, `medium`, `low` |

## Optional Fields

| Field | Type | Description |
|---|---|---|
| `evidence_completeness_score` | integer | 0-5 |
| `missing_evidence` | array[string] | What would improve judgment |
| `review_notes` | string | Concise notes |
| `adjudication_status` | enum | `not_needed`, `pending`, `resolved` |
| `adjudicated_label` | enum | Final label if disagreement resolved |

## Labeling Rule

Use `uncertain` when evidence is suspicious but inconclusive. Use `insufficient_evidence` when the available evidence cannot support a judgment. Do not force ambiguous cases into binary labels.
