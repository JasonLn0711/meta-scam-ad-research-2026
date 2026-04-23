# Budget Fit Analysis

## Second-Pass Budget Reality

Approximate subproject budget: NTD 1.8M.

The first-pass plan was directionally right but still too optimistic about how many modalities can be meaningfully tested. NTD 1.8M can support a defensible research answer and a narrow prototype. It cannot support broad multimodal experimentation plus legal data work plus annotation plus a production-like demo.

## Budget Pressure Points

| Pressure point | Why it matters |
|---|---|
| Lawful data access | May require stakeholder coordination, redaction, review, and data contracts before any experiment |
| Annotation | Scam/benign/uncertain labels require domain judgment and hard negatives |
| Landing pages | High value but legally and operationally gated; safe capture can become its own project |
| Video | ASR, OCR, keyframes, storage, and reviewer time raise cost quickly |
| VLM/LLM scoring | API/model cost and consistency risk grow with item count |
| Human review | Public-sector usefulness requires reviewer evaluation, not just model metrics |

## What Is Too Big For This Budget

| Scope item | Budget judgment | Reason |
|---|---|---|
| Full Facebook + Instagram + Threads coverage | Cut from promise | data access and evaluation too broad |
| Stories | Cut | ephemeral and hard to collect lawfully |
| Long video | Cut | high compute and annotation cost |
| Full Reels/short-video pipeline | Postpone | useful later, not first prototype |
| Comments/replies | Postpone | privacy, access, and annotation complexity |
| Profile graph/network analysis | Cut | data access and privacy burden |
| Definitive deepfake detection | Cut | specialist project, high false-certainty risk |
| Full landing-page cloaking detection | Postpone | security/legal infrastructure required |
| Production dashboard/monitoring | Cut | product work, not research starter |
| VLM scoring for every item | Cut | costly and hard to defend before cheap baselines |

## What To Keep

| Kept branch | Why it survives |
|---|---|
| Text and caption analysis | cheap, explainable, high overlap with lure patterns |
| OCR from static images/carousel cards | likely high recall gain for scam creatives |
| Image + text + OCR fusion | strongest first multimodal value without video cost |
| Manual rules and keyword/risk patterns | transparent baseline and stakeholder-friendly |
| Simple text/classical ML baseline | cheap comparator if labels are sufficient |
| Evidence completeness scoring | prevents overconfident weak cases |
| Human review packet | converts model output into operational value |
| Landing-page evidence | keep only as gated optional branch if lawfully provided |
| Limited metadata | keep only if stakeholder-provided or API-authorized |

## Candidate Technical Paths

| Path | Components | Value | Cost | Risk | Second-pass fit |
|---|---|---:|---:|---:|---|
| Cheap baseline | rules, keywords, OCR, simple text baseline | Medium | Low | Low | Must build |
| Budget-fit evidence triage | image + caption + OCR + evidence packet + human review | High | Medium | Medium | Recommended |
| Gated landing/metadata add-on | budget-fit core plus approved landing/metadata | High | Medium-high | Medium-high | Add only if data is ready |
| Video-enhanced pilot | short-video keyframes/ASR/OCR | Medium | High | High | Research discussion or late Phase 2 only |
| VLM-heavy scoring | VLM/LLM for most items | Medium | High | High | Sample only, not core |
| Full multimodal platform system | all surfaces, graph, video, comments, Stories, deepfake | High in theory | Very high | Very high | Not budget-fit |

## Revised Value Versus Cost Ranking

1. Image + caption + OCR triage.
2. Manual rules and keyword/risk-pattern baseline.
3. Reviewer evidence packet with reason codes and evidence completeness.
4. Simple text/classical ML baseline if labels are sufficient.
5. Landing-page evidence only if stakeholder-provided or approved.
6. Limited metadata only if stakeholder-provided or approved.
7. Sampled VLM explanation for qualitative comparison.
8. Short-video keyframe + ASR + OCR pilot.
9. Comments/replies analysis.
10. Deepfake detection, long video, Stories, graph analysis.

## Recommended Budget-Fit Path

Fund this path first:

- scope and data governance
- taxonomy and annotation guideline
- small approved or synthetic dry-run sample
- text/caption baseline
- OCR + keyword baseline
- image + caption + OCR hybrid triage
- evidence completeness scoring
- reviewer packet generation
- human review evaluation
- decision memo with future roadmap

Conditional add-ons:

- landing-page evidence if stakeholders provide screenshots/text/URLs under an approved process
- limited metadata if stakeholders provide lawful fields
- sampled VLM explanations for comparison, not for primary scoring

## Budget Allocation Heuristic

| Workstream | Approximate share | Second-pass interpretation |
|---|---:|---|
| Scoping, stakeholder interviews, governance | 20% | cannot be squeezed; determines lawful data |
| Data contracts, sample prep, annotation pilot | 30% | core research foundation |
| Cheap baselines and ablations | 20% | must prove value over rules/OCR/text |
| Narrow prototype and reviewer packet | 20% | demo-worthy artifact |
| Final evaluation and decision memo | 10% | stakeholder-defensible conclusion |

This allocation leaves little room for video, deepfake, comments, or dashboard work.

## Demo Budget Boundary

Demo should show:

- a small evidence-packet workflow
- static image/caption/OCR examples
- reason codes
- evidence completeness
- high/medium/low queue
- reviewer final label field

Demo should not show:

- live scraping or platform monitoring
- full video analysis
- deepfake detection
- large-scale dashboard
- automatic enforcement
- real sensitive case material unless cleared

## Bottom Line

NTD 1.8M supports a narrow, evidence-centric research prototype and a strong decision memo. The stakeholder-defensible promise is not "we detect Meta scam ads." It is "we identify which affordable evidence signals can support human triage, and what additional data/funding would be required for broader coverage."
