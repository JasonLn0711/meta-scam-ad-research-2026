# Evidence Field Dictionary

| Field | Required | Type | Description | Notes |
|---|---|---|---|---|
| `case_id` | yes | string | Stable internal case identifier | No personal data in ID |
| `source_type` | yes | enum | stakeholder, manual_public, api_authorized, synthetic, weak_label | Must match governance decision |
| `authorization_status` | yes | enum | approved, pending, rejected, synthetic_only | No experiment without clarity |
| `platform_surface` | yes | enum | facebook, instagram, threads, landing_page, unknown | Use unknown if unclear |
| `content_form` | yes | enum | static_image, image_caption, carousel, text_only, short_video, long_video, story, comment_reply, landing_page, metadata_only | Stable content taxonomy |
| `capture_method` | yes | enum | stakeholder_provided, manual_capture, api, synthetic, other | Automated capture must be approved |
| `capture_timestamp_utc` | recommended | string | ISO-8601 timestamp | Required for real evidence when possible |
| `source_reference` | recommended | string | URL, report ID, or redacted reference | Redact if needed |
| `creative_text` | optional | string | Caption, post text, ad text | Raw or redacted |
| `ocr_text` | optional | string | OCR extracted from image/video | Include OCR tool/version in metadata |
| `asr_text` | optional | string | Speech transcript from video/audio | Phase 2+ |
| `landing_url` | optional | string | Destination URL | Only if lawfully available |
| `redirect_chain` | optional | array | Redirect URLs or domains | Security/legal gated |
| `media_reference` | optional | string | Local or external media reference | Do not commit sensitive media by default |
| `metadata_fields_available` | optional | array | Names of metadata fields available | Avoid assuming complete metadata |
| `reason_codes` | optional | array | Explainable risk reasons | See taxonomy |
| `evidence_completeness_score` | optional | integer | 0-5 evidence completeness | See evaluation framework |
| `reviewer_notes` | optional | string | Concise evidence note | Avoid personal-data expansion |
