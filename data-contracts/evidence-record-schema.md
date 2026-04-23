# Evidence Record Schema

This is the minimum logical schema for one research evidence record. It is intentionally format-neutral and can later be represented as JSONL, CSV, or database rows.

## Required Fields

| Field | Type | Allowed values / format |
|---|---|---|
| `case_id` | string | stable unique ID |
| `source_type` | enum | `stakeholder`, `manual_public`, `api_authorized`, `synthetic`, `weak_label` |
| `authorization_status` | enum | `approved`, `pending`, `rejected`, `synthetic_only` |
| `platform_surface` | enum | `facebook`, `instagram`, `threads`, `landing_page`, `unknown` |
| `content_form` | enum | `static_image`, `image_caption`, `carousel`, `text_only`, `short_video`, `long_video`, `story`, `comment_reply`, `landing_page`, `metadata_only` |
| `capture_method` | enum | `stakeholder_provided`, `manual_capture`, `api`, `synthetic`, `other` |

## Recommended Fields

| Field | Type | Notes |
|---|---|---|
| `capture_timestamp_utc` | string | ISO-8601 |
| `source_reference` | string | URL, report ID, or redacted source reference |
| `creative_text` | string | caption/post/ad text |
| `ocr_text` | string | extracted image/video text |
| `landing_url` | string | gated by data approval |
| `redirect_chain` | array[string] | gated by data approval and safe capture |
| `metadata_fields_available` | array[string] | field names only if values cannot be stored |

## Derived Fields

| Field | Type | Producer |
|---|---|---|
| `risk_score` | number | rule/model/hybrid pipeline |
| `risk_level` | enum | `high`, `medium`, `low` |
| `reason_codes` | array[string] | rule/model/reviewer |
| `evidence_completeness_score` | integer | pipeline/reviewer |

## JSONL Sketch

```json
{
  "case_id": "case-0001",
  "source_type": "synthetic",
  "authorization_status": "synthetic_only",
  "platform_surface": "unknown",
  "content_form": "image_caption",
  "capture_method": "synthetic",
  "creative_text": "Example text for pipeline testing only.",
  "ocr_text": "",
  "reason_codes": []
}
```

Do not treat this sketch as real evidence.
