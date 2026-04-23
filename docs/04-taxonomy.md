# Taxonomy

This taxonomy is a draft. It should be validated with CIB/165/domain experts and refined through annotation disagreement.

## Scam Pattern Taxonomy

| Code | Pattern | Description | Common evidence |
|---|---|---|---|
| `INVESTMENT_LURE` | Investment scam | Promises high return, exclusive group, trading signal, crypto/stock profit | unrealistic ROI, LINE/WhatsApp group, celebrity endorsement |
| `FAKE_ECOMMERCE` | Fake shopping / counterfeit / non-delivery | Deep discounts, brand misuse, survey-to-prize, payment collection | suspicious domain, fake checkout, too-good-to-be-true offer |
| `HEALTH_PRODUCT` | Fraudulent health product | Unapproved treatment, exaggerated cure, fake doctor endorsement | medical claims, public-figure image, before/after manipulation |
| `PHISHING` | Credential or identity theft | Login, account recovery, prize, verification | credential form, urgency, lookalike domain |
| `SUBSCRIPTION_TRAP` | Subscription fraud | Small payment leads to recurring charge | hidden subscription, fake survey, credit card request |
| `ROMANCE_SOCIAL_ENGINEERING` | Romance or confidence pathway | Moves victim to private channel or investment group | intimacy lure, off-platform migration |
| `ACCOUNT_RECOVERY_SCAM` | Fake unban/recovery service | Claims to restore accounts or recover funds | payment demand, fake expert, urgency |
| `JOB_TASK_SCAM` | Job or task scam | Fake remote job, commission, deposit | deposit request, high pay, messaging migration |
| `LOTTERY_PRIZE` | Prize or giveaway scam | Claims user won prize or reward | fee request, personal info form |
| `UNKNOWN_DECEPTIVE` | Other deceptive scheme | Suspicious but not classified | reviewer notes required |

## Content Taxonomy

| Code | Form | Notes |
|---|---|---|
| `STATIC_IMAGE` | Static image creative | Includes screenshot-like ads and AI-generated imagery |
| `IMAGE_CAPTION` | Image plus caption/post text | Phase 1 priority |
| `CAROUSEL` | Multi-image carousel | Treat as image-set in Phase 1 |
| `TEXT_ONLY` | Text-only lure | Often useful and cheap |
| `SHORT_VIDEO` | Reels/short video | Phase 2 keyframe + ASR + OCR |
| `LONG_VIDEO` | Longer video | Deferred |
| `STORY` | Story | Deferred due to access/ephemerality |
| `COMMENT_REPLY` | Comments/replies | Phase 2 limited |
| `PROFILE_METADATA` | Profile/page/account fields | Limited to lawful fields |
| `LANDING_PAGE` | External page evidence | High value, legally gated |

## Manipulation Taxonomy

| Code | Signal | Important caution |
|---|---|---|
| `CELEB_BAIT` | Public figure used to attract clicks | Legitimate endorsements exist |
| `BRAND_IMPERSONATION` | Brand/logo/name misuse | Need compare against legitimate brand use |
| `AI_GENERATED_IMAGE` | Possible generated image | Not proof of scam |
| `DEEPFAKE_RISK` | Altered voice/face or synthetic public figure | Treat as risk indicator, not definitive judgment |
| `CLOAKING_RISK` | Different content for review vs user | Requires careful capture and legal review |
| `URGENCY_PRESSURE` | limited time, few slots, countdown | Common in benign ads too |
| `FAKE_SOCIAL_PROOF` | fake comments, testimonials, likes | Needs pattern evidence |
| `OFF_PLATFORM_MIGRATION` | LINE/WhatsApp/Telegram/DM redirect | High investigative value |

## Severity / Risk Taxonomy

| Level | Meaning | Example action |
|---|---|---|
| `high_risk` | Strong multi-evidence scam pattern or likely victim harm | Human review first; preserve evidence packet |
| `medium_risk` | Several suspicious signals but incomplete evidence | Review if capacity allows; seek landing/metadata evidence |
| `low_risk` | Weak signals or mostly benign with one warning sign | Sample for QA/drift, not urgent |
| `insufficient_evidence` | Cannot judge from available fields | Do not overclaim |

## Explainable Reasons Taxonomy

Reason codes should be attached to model and human judgments:

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

## Scam-Likely Signals

Examples of signals that may support scam-like classification:

- "guaranteed profit", "risk-free", "limited seats", or "teacher group" in investment context.
- Celebrity or doctor image paired with product or investment claims.
- Huge discount plus unfamiliar domain plus card collection.
- Landing page asks for credentials, payment, or personal data unrelated to the ad claim.
- CTA moves the user to LINE, WhatsApp, Telegram, or private group before details are provided.
- Multiple creatives reuse the same domain, text, or image with different page identities.

No single signal is conclusive. The system should preserve evidence and uncertainty.
