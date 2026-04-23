# Experiment Program

## Second-Pass Position

The first version mapped the design space broadly. This second pass narrows the experiment program for a defensible NTD 1.8M research project.

The budget-fit center is not "multimodal Meta scam detection." It is a narrow evidence-centric triage study for static/ad-like creatives where text, OCR, image context, and human-review evidence can be compared cheaply and explained clearly.

## What Is Still Too Broad

Cut from the funded core:

- full video/Reels processing
- Stories
- comments/replies as a main branch
- profile graph or account-network analysis
- broad Threads collection
- definitive deepfake detection
- VLM/LLM scoring for every item
- production dashboard, monitoring, or enforcement workflow
- landing-page crawling/cloaking detection unless explicitly approved and safely bounded

These can remain in research discussion and future-roadmap sections, but they should not be in the first prototype promise.

## Refined Program Logic

Every funded experiment must answer one of these narrowing decisions:

1. Does this signal improve high-risk triage enough to reduce human review burden?
2. Can this evidence be collected lawfully and repeatedly?
3. Can reviewers understand and challenge the reason codes?
4. Is the cost low enough to fit an NTD 1.8M research project?

Experiments that only prove technical possibility are low priority. Experiments that help reject scope are valuable.

## Refined Phase Plan

| Phase | Goal | Keep | Cut or postpone | Exit decision |
|---|---|---|---|---|
| Phase 0 | Scope, data, taxonomy, annotation readiness | stakeholder questions, evidence schema, taxonomy, annotation pilot plan | no code, no scraping, no video | Can we lawfully create a small sample? |
| Phase 1 | Cheap evidence baselines | text, OCR, image+caption, carousel-as-image-set, manual rules, keyword patterns, simple text baseline | VLM-heavy scoring, comments, video, deepfake | Which low-cost signals are worth prototype inclusion? |
| Phase 2 | First meaningful prototype | hybrid risk triage, reason codes, evidence completeness, reviewer packet | production dashboard, live ingestion, broad automation | Can reviewers use the output to prioritize cases? |
| Phase 3 | Evaluation and decision memo | human review, error analysis, budget-fit recommendation | new modalities unless they change the decision | What should be funded next? |

## First Meaningful Prototype

The first prototype should be a small, auditable evidence-packet generator, not a full application.

Inputs:

- caption/post/ad text
- screenshot or static image reference
- OCR text extracted from image/carousel cards
- optional landing-page text or screenshot only if lawfully provided
- optional limited metadata only if stakeholder-provided or API-authorized

Outputs:

- high/medium/low risk level
- reason codes
- evidence completeness score
- short reviewer-facing explanation
- missing-evidence list
- final human reviewer label field

The demo should show processed redacted, stakeholder-approved, or synthetic examples. It should not show live Meta collection.

## Experiment Family A: Modality Comparison

| Comparison | Budget-fit status | Hypothesis | Required data | Metrics | Decision use |
|---|---|---|---|---|---|
| Text only | Keep as baseline | Captions/lure language catch cheap scam signals | caption/post text | high-risk precision, recall, review burden | minimum baseline |
| OCR text from image | Keep as core | Scam claims often live inside images | images + OCR output | OCR recall gain, OCR error rate | include if it catches missed claims |
| Image + caption + OCR | Keep as core | Combined context is the best first ROI | paired text/image/OCR | triage quality, reason usefulness | first prototype core |
| Carousel as image-set | Keep but bounded | Treat carousel as several static images, not a new modality | carousel screenshots/cards | incremental recall, annotation time | include if data is available |
| Image only | Downgrade | Visual signal alone is useful but too ambiguous | labeled images | false positives, explanation quality | use as ablation, not product claim |
| Landing page augmentation | Conditional | Destination evidence improves precision | stakeholder-provided URL/screenshot/text | precision, evidence completeness | include only if lawful and safe |
| Metadata augmentation | Conditional | Limited metadata helps prioritize | lawful metadata fields | lift over content-only | include only if provided/authorized |
| Short video keyframe + ASR + OCR | Postpone | May catch video scams but cost rises fast | short videos | cost/item, recall gain | Phase 2 discussion, not first demo |
| Comments/replies | Postpone | May expose induced interaction | comments/replies | review burden, privacy risk | future study only |
| Deepfake indicators | Discussion only | Synthetic manipulation may flag impersonation risk | specialist examples | reviewer usefulness | do not build detector |

## Experiment Family B: Pipeline Comparison

| Pipeline | Status | Why |
|---|---|---|
| Manual rule baseline | Keep | transparent, cheap, proposal-defensible |
| Keyword/risk-pattern baseline | Keep | strong cheap comparator for text/OCR |
| OCR + keyword baseline | Keep | likely high ROI for scam-image claims |
| Classical ML text baseline | Keep if labels are enough | cheap but needs labels |
| Transformer text baseline | Conditional | use only if classical baseline is weak or language context matters |
| Image embedding/classifier baseline | Conditional | useful as ablation; avoid overclaiming visual fraud detection |
| VLM-assisted explanation | Sample only | useful for qualitative review, too costly/variable as main scoring path |
| Hybrid scoring + human review | Keep as target | aligns with investigation and budget |

## Experiment Family C: Scope Comparison

| Scope | Status | Decision |
|---|---|---|
| All candidate forms | Discussion only | Use as scope map, not funded experiment |
| Most feasible first subset | Keep | text + OCR + image-caption is first prototype |
| Best ROI subset | Keep | add landing/metadata only if approved |
| Highest investigative value subset | Conditional | landing/domain evidence may be strongest, but only with safe access |
| Full multimodal subset | Defer | requires new budget/data partnership |

## Experiment Family D: Operational Comparison

| Output mode | Status | Why |
|---|---|---|
| Binary classification | Baseline only | too blunt for public-sector review |
| Multi-class taxonomy | Reporting layer | useful for analysis, not first triage output |
| High/medium/low triage | Keep as primary | fits reviewer prioritization |
| Evidence completeness scoring | Keep | prevents overconfident weak cases |
| Reviewer workload reduction | Keep | strongest operational value metric |

## Experiment Family E: Budget Comparison

| Path | Status | Components | Demo suitability |
|---|---|---|---|
| Cheap path | Keep | rules, keywords, OCR, simple text baseline | yes, as transparent baseline |
| Budget-fit path | Recommended | image+caption+OCR, optional landing/metadata, human review packet | yes, main demo |
| Ambitious path | Research discussion only | video, comments, graph, deepfake, full ingestion | no |

## Low-ROI Branches For This Budget

- Video-first pipeline: high processing and annotation cost before data access is proven.
- Deepfake-first pipeline: attractive topic but fragile and easy to overpromise.
- Comments/replies branch: privacy and access cost likely exceed Phase 1 value.
- Metadata-only scoring: useful only if trustworthy fields are provided.
- VLM-heavy scoring for all items: likely costly, inconsistent, and hard to defend without simpler baselines.
- Full landing-page cloaking detection: high value but security/legal heavy; discuss, do not demo unless approved.

## Demo Versus Research Discussion

Show in demo:

- redacted or synthetic examples
- text/OCR/static image evidence extraction
- rule/keyword and simple model baseline comparison
- high/medium/low triage
- reason codes and evidence completeness
- reviewer packet and final label field

Keep as research discussion:

- live Meta ingestion
- automated scraping
- full video/Reels processing
- Stories
- comments/replies
- deepfake detection claims
- profile graph/network analysis
- production dashboard

## Required Experiment Discipline

Each experiment log must state:

- hypothesis
- data slice and authorization status
- evidence fields
- pipeline
- compute/API/model cost
- human review cost
- metrics
- reviewer observations
- decision: keep, revise, defer, or drop
