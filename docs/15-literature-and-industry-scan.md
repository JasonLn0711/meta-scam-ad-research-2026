# Literature And Industry Scan

This is an initial synthesis, not a complete bibliography. It should be expanded as the proposal matures.

## Key Public Signals

FTC reporting has identified social media as a major contact method for scams, with reported losses tied to social media scams and prominent categories including online shopping, investment scams, and romance scams. This supports prioritizing fake e-commerce, investment lures, and social-engineering redirection in the taxonomy.

Meta's public scam-enforcement updates discuss scam advertisers, celebrity bait, brand impersonation, cloaking, subscription fraud, AI-assisted detection, and cross-industry/law-enforcement partnerships. These public statements support the idea that scam-ad detection is multi-layered: creative analysis alone is insufficient when scammers use redirects, payment flows, account infrastructure, and evasion tactics.

Meta's automated data collection terms and developer/API ecosystem show that data access is not a trivial engineering detail. Research design must treat lawful access and permission as a gating issue.

## Research Themes

### Multimodal Moderation

Scam ads often combine visual, textual, and contextual signals. A caption may look harmless while the image contains the suspicious claim. An image may look suspicious but the landing page determines whether the user is asked for payment, credentials, or private-channel migration.

Implication: compare text-only, OCR-only, image-only, and image+text pipelines before committing to expensive multimodal models.

### Landing-Page And Redirect Evidence

Many scam patterns become clear only after clicking through:

- fake checkout pages
- credential capture
- survey-to-subscription traps
- private chat migration
- cloaked content
- payment or personal-data collection

Implication: landing-page evidence has high investigative value but must be legally and operationally gated.

### Cloaking

Cloaking means different users or review systems may see different destination content. It is hard to detect reliably without controlled capture infrastructure and repeated observations.

Implication: document cloaking risk, but do not promise robust cloaking detection in Phase 1.

### Deepfake And AI-Generated Manipulation

Deepfake and AI-generated media can make celebrity/doctor impersonation cheaper and more scalable. However, deepfake detection is uncertain, adversarial, and easy to overclaim.

Implication: treat deepfake as a risk indicator attached to impersonation cases, not as a definitive classifier.

### Review And Triage Systems

Public-sector usefulness depends on reviewer workflow:

- evidence completeness
- reason codes
- high-risk queue quality
- false-positive burden
- missing-evidence clarity

Implication: high/medium/low triage and evidence packets are more useful than raw binary classification.

### Weak Labels And Noisy Ground Truth

Reports, takedowns, keywords, and domain lists can provide weak signals, but they are biased and incomplete. A reported example is not necessarily confirmed fraud; an unreported example is not necessarily benign.

Implication: keep `uncertain` and `insufficient_evidence` labels. Do not collapse everything into binary labels too early.

## Open Problems

- Reliable, lawful data access to real scam ads and benign comparators.
- Distinguishing scams from aggressive but legitimate marketing.
- Measuring off-platform harm when the platform evidence is incomplete.
- Evaluating adversarial drift.
- Preserving privacy while retaining evidence.
- Creating useful explanations without hallucinated model reasoning.

## Industry Pattern Observations

Common anti-scam system patterns:

- Rules for obvious prohibited claims and suspicious CTAs.
- Text classifiers for language risk.
- OCR to recover embedded text.
- Image matching or embeddings for reused creatives.
- Domain reputation and redirect analysis.
- Human review queues for high-risk cases.
- Feedback loops from reviewer decisions.

The budget-fit recommendation follows these patterns but keeps them research-grade and evidence-centric.

## Sources To Review Further

- Meta Automated Data Collection Terms: https://www.facebook.com/legal/automated_data_collection_terms
- Meta Ad Archive/API announcement: https://about.fb.com/news/2018/08/introducing-the-ad-archive-api/
- Meta scam advertiser legal action and cloaking discussion: https://about.fb.com/news/2026/02/meta-takes-legal-action-against-scam-advertisers/
- Meta scam enforcement update: https://about.fb.com/news/2026/03/fighting-scammers-protecting-people-with-new-technology-and-partnerships/
- FTC social media scam loss report: https://www.ftc.gov/news-events/news/press-releases/2023/10/ftc-data-shows-consumers-report-losing-27-billion-social-media-scams-2021

## Synthesis For This Project

The research should not begin with the most complex model. It should begin with evidence availability, taxonomy, and baselines. The first defensible technical move is to test whether image + caption + OCR + landing/metadata evidence improves high-risk triage over text-only or rule-only screening.
