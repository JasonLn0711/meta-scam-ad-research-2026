# Data Strategy

## Data Posture

Default posture: authorization-first.

Do not perform automated data collection from Meta products without explicit written authorization, approved API access, or a stakeholder/legal decision recorded in `governance/data-governance.md`. Meta's automated data collection terms and platform policies must be treated as first-order constraints.

## Candidate Data Sources

| Source type | Examples | Strength | Risk / limitation | Phase use |
|---|---|---|---|---|
| Stakeholder-provided cases | CIB/165 examples, confirmed reports, takedown evidence | High realism | privacy, chain of custody, access approval | Phase 0-1 priority |
| Manual public capture | Human-reviewed examples from public ad/library/page surfaces | Direct evidence | slow, platform terms, reproducibility | Phase 0-1 with governance |
| Official API / approved access | Meta Ad Library/API where applicable | More repeatable | scope may be limited; approval required | Phase 1 if approved |
| Public reports | FTC, consumer alerts, media investigations, public scam examples | Useful taxonomy seed | not model-training ground truth | Phase 0 |
| Synthetic examples | Generated lures, benign lookalikes, prompt variants | Safe for pipeline testing | not representative of real adversaries | Phase 0-1 only |
| Weak labels | reports, keyword hits, domain reputation, prior takedowns | scalable signal | noisy and biased | Phase 1-2 with audit |
| Landing pages | URLs, screenshots, DOM text, redirect chain | High investigative value | cloaking, malware, legal risk | Gated by approval |

## Ethical, Legal, And Privacy Constraints

- Minimize personal data.
- Prefer evidence necessary for scam assessment, not broad user profiling.
- Avoid storing unrelated faces, names, comments, or account identifiers unless needed and approved.
- Preserve source URL, capture timestamp, and collection method for reproducibility.
- Separate sensitive raw evidence from derived features.
- Use redaction in stakeholder-facing examples.
- Never use sensitive data for model demos outside the approved project context.

## Sampling Strategy

Phase 0 sample:

- 20-50 stakeholder examples if available.
- 20-50 public/manual examples across scam families.
- 20-50 benign comparator examples from legitimate ads or posts in similar domains.

Phase 1 pilot:

- Target 300-800 items if data access is available.
- Balance high-risk families: investment, fake e-commerce, healthcare, phishing, subscription traps, celebrity/brand impersonation.
- Include hard negatives: legitimate finance ads, legitimate healthcare ads, legitimate celebrity campaigns, political satire, news posts.

Phase 2 narrowed prototype:

- Expand only the best-ROI subset.
- Add short-video or comment slices only if Phase 1 shows stakeholder value and legal access.

## Deduplication Strategy

Deduplicate at multiple levels:

- Exact URL/domain match.
- Screenshot perceptual hash.
- OCR text similarity.
- Caption/text similarity.
- Landing-page canonical URL and redirect target.
- Creative reuse across different pages or accounts.

Deduplication should preserve clusters, not delete history blindly. Reuse itself can be an investigative signal.

## Labeling Policy Ideas

Primary label:

- `scam_like`
- `benign`
- `uncertain`
- `insufficient_evidence`

Triage label:

- `high_risk`
- `medium_risk`
- `low_risk`

Reason labels:

- impersonation
- unrealistic financial claim
- suspicious medical claim
- fake e-commerce discount
- credential/payment collection
- off-platform migration
- cloaking/redirect concern
- suspicious domain
- AI/deepfake risk indicator
- engagement manipulation

## Evidence Fields To Preserve

Minimum evidence record:

| Field | Purpose |
|---|---|
| `case_id` | Stable internal reference |
| `source_type` | stakeholder, manual public, API, synthetic, weak label |
| `platform_surface` | Facebook, Instagram, Threads, landing page, unknown |
| `content_form` | image, text, carousel, short video, comment, landing page |
| `capture_method` | manual, API, stakeholder-provided, synthetic |
| `capture_timestamp_utc` | reproducibility |
| `source_url_or_reference` | traceability, redacted where needed |
| `creative_text` | caption/post text |
| `ocr_text` | text extracted from image/video |
| `asr_text` | speech transcript if video/audio |
| `landing_url` | destination evidence |
| `redirect_chain` | cloaking and fraud evidence |
| `metadata_fields_available` | not all fields will exist |
| `label` | scam_like/benign/uncertain/insufficient_evidence |
| `triage_level` | high/medium/low |
| `reason_codes` | explainable evidence |
| `reviewer_id` | pseudonymous reviewer |
| `review_notes` | concise evidence notes |

## Data Decision Rule

If a data source is high value but legally fragile, it should be documented as a requirement or stakeholder question, not silently used.
