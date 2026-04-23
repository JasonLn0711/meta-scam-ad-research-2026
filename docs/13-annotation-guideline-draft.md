# Annotation Guideline Draft

## Purpose

This guideline helps reviewers label Meta-related scam-like content consistently. It is a draft and should be tested through pilot annotation.

## Primary Labels

| Label | Definition | Use when |
|---|---|---|
| `scam_like` | Available evidence strongly suggests deceptive or fraudulent intent | Multiple scam signals or strong destination/payment/impersonation evidence |
| `benign` | Content appears legitimate based on available evidence | Normal ad/post with clear business, reasonable claims, no suspicious redirect |
| `uncertain` | Suspicious but evidence is not enough | Some red flags but plausible benign explanation |
| `insufficient_evidence` | Cannot judge because required evidence is missing | Image/text lacks context, URL unavailable, media unreadable |

## Triage Labels

| Label | Meaning |
|---|---|
| `high_risk` | Review immediately; likely scam or high potential harm |
| `medium_risk` | Needs more evidence or secondary review |
| `low_risk` | Weak signals; review only for QA or drift |

## Reason Codes

Select all that apply:

- `unrealistic_return_claim`
- `medical_cure_claim`
- `celebrity_or_doctor_impersonation`
- `brand_impersonation`
- `suspicious_domain`
- `hidden_or_redirected_destination`
- `payment_or_credential_collection`
- `off_platform_chat_migration`
- `fake_testimonial_pattern`
- `AI_or_deepfake_risk_indicator`
- `metadata_anomaly`
- `known_case_similarity`
- `insufficient_context`

## Scam-Like Criteria

Mark `scam_like` when evidence supports one or more of:

- Investment or crypto profit claims that promise unrealistic returns or low/no risk.
- Celebrity, public figure, doctor, or brand used in a way that appears unauthorized or misleading.
- Landing page asks for credentials, payment, credit card, or personal data unrelated to a legitimate transaction.
- Strong mismatch between ad content and destination page.
- Off-platform migration to LINE, WhatsApp, Telegram, or private group as the main conversion step.
- Fake e-commerce discount or prize that leads to suspicious payment or subscription flow.
- Health product claims that imply cure, guaranteed effect, or regulatory impossibility.

## Uncertain Criteria

Use `uncertain` when:

- Claims are aggressive but not clearly fraudulent.
- A celebrity or brand appears, but endorsement cannot be verified.
- OCR is low quality.
- URL is missing or destination cannot be inspected.
- Content may be satire, commentary, news, or parody.
- The same signal appears in legitimate ads in the same domain.

## Benign Criteria

Use `benign` when:

- Business identity is clear.
- Claims are reasonable and verifiable.
- Destination page matches the ad.
- Payment or personal-data request is expected and transparent.
- No strong impersonation, deception, or off-platform manipulation is visible.

## Insufficient Evidence

Use `insufficient_evidence` when:

- Only a cropped image exists.
- Text is unreadable.
- Link is missing.
- Screenshot lacks timestamp/source.
- Video cannot be reviewed.
- Metadata needed for judgment is unavailable.

## Special Handling

### Satire And Parody

Do not label as scam-like only because a public figure image appears. Check whether the content is commentary, parody, political satire, or news.

### Legitimate Ads

Legitimate ads may use urgency, discounts, influencers, testimonials, or finance language. Require deception evidence before marking high risk.

### Finance

Finance/investment content should be reviewed carefully. Red flags include guaranteed returns, private trading groups, pressure to deposit, crypto wallet instructions, or fake celebrity endorsement.

### Medical And Health

Health content is high-risk when it claims cure, uses fake doctors, misuses hospital/authority identity, or redirects to suspicious purchase pages. Do not assume all supplement ads are scams.

### Political Content

Political content may be sensitive and may overlap with public-interest ads. Use uncertainty when scam evidence is weak.

### Celebrity/Public Figure Content

Public figure presence is not enough. Look for false endorsement, altered quote, AI/deepfake risk indicator, destination mismatch, or payment/credential capture.

## Reviewer Note Format

Use short evidence notes:

```text
Label:
Triage:
Reason codes:
Evidence observed:
Missing evidence:
Reviewer confidence:
```

## Annotation Quality Checks

- Review hard negatives.
- Track disagreement.
- Revise reason codes if reviewers keep inventing new explanations.
- Separate "suspicious content" from "insufficient evidence."
