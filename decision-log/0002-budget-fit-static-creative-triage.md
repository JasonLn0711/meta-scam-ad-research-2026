# Decision 0002: Budget-Fit Static Creative Triage Path

## Identity

- Date: 2026-04-23
- Status: accepted
- Owner: project starter

## Decision

Use a static creative evidence triage packet as the first meaningful prototype.

The first funded research path should center on caption/post/ad text, OCR from static images and carousel cards, image + caption + OCR evidence, reason codes, evidence completeness scoring, and human reviewer packets.

Landing-page evidence and metadata are conditional add-ons only if lawfully/stakeholder provided. Video, comments, Stories, graph analysis, full platform ingestion, and definitive deepfake detection are postponed.

## Context

The first-pass research map correctly considered the broad design space, but it still left too much apparent room for high-cost branches under an NTD 1.8M budget. A second-pass review identified that the project would become difficult to defend if it promised broad multimodal detection or platform-scale coverage.

## Options Considered

| Option | Pros | Cons | Decision |
|---|---|---|---|
| Full multimodal Meta scam detection | Matches the broad problem statement | Exceeds budget; depends on platform access; high annotation and evaluation burden | Rejected for first phase |
| Video/deepfake-first research | Timely and attention-grabbing | Low ROI under budget; high false-certainty risk; specialist benchmark needed | Rejected for first phase |
| Landing-page/metadata-first system | High investigative value | Gated by legal access, safe capture, and stakeholder data | Conditional |
| Static creative evidence triage | Affordable, explainable, demoable, reviewer-centered | Does not cover every surface | Accepted |

## Rationale

NTD 1.8M should buy clarity, lawful evidence design, defensible baselines, and a narrow prototype. The static creative triage path keeps the strongest low-cost signals and cuts the branches most likely to consume the budget before producing useful evaluation evidence.

## Consequences

- The first demo should not show live scraping, real-time monitoring, video analysis, deepfake detection, or enforcement decisions.
- The first demo may show a redacted or synthetic case set moving through text/OCR/static-image evidence, reason codes, evidence completeness, and reviewer final label fields.
- Future proposals can discuss video, comments, deepfake, landing-page sandboxing, graph analysis, and platform partnership as roadmap items requiring additional authorization, data, and budget.

## Files Updated

- `docs/05-experiment-program.md`
- `docs/07-budget-fit-analysis.md`
- `docs/10-decision-memo.md`
- `docs/16-mvp-definition.md`
- `docs/17-recommended-path.md`
