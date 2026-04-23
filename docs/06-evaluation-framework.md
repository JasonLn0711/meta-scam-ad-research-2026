# Evaluation Framework

## Evaluation Principle

Evaluate for operational usefulness, not only model performance. A model with strong F1 but weak evidence, poor explainability, or excessive review burden is not a good public-sector research outcome.

## Core Evaluation Dimensions

| Dimension | Metric / observation | Why it matters |
|---|---|---|
| Precision | precision overall, precision at high-risk threshold | Avoids harming legitimate advertisers or benign content |
| Recall | recall overall, recall by scam family | Shows whether important scam types are missed |
| Triage quality | high/medium/low accuracy, high-risk yield | Aligns with investigator workflow |
| Review burden | items reviewed per confirmed/high-risk case | Measures operational value |
| Evidence completeness | presence of text, OCR, image, URL, redirect, metadata, reason codes | Tells reviewers whether case is actionable |
| Explainability quality | reviewer-rated reason usefulness | Supports trust and correction |
| Robustness | performance by scam family, platform, language, media quality | Avoids brittle conclusions |
| Drift sensitivity | degradation over time or campaign changes | Scam tactics change quickly |
| Cost | compute/API cost per 1000 items and human minutes per item | Keeps NTD 1.8M constraints visible |
| Legal/data viability | whether evidence can be obtained lawfully and repeatably | Prevents impossible prototype claims |

## Classification Metrics

Use conventional metrics, but interpret them carefully:

- Precision, recall, F1.
- ROC-AUC and PR-AUC only when probability scores are meaningful.
- Calibration error for risk scores.
- Macro-F1 for scam-family taxonomy.
- Confusion matrix across `scam_like`, `benign`, `uncertain`, and `insufficient_evidence`.

## Operational Metrics

Recommended primary operational metrics:

- High-risk review yield: percent of high-risk queue confirmed or escalated by reviewers.
- Reviewer workload reduction: reduction in items needing manual review at fixed recall.
- Evidence packet usefulness: reviewer score from 1 to 5.
- Missing-evidence rate: percent of model decisions lacking enough evidence for action.
- False positive burden: benign or legitimate content incorrectly escalated.
- False negative case analysis: high-harm scam examples missed by the pipeline.

## Human Review Design

Reviewer workflow:

1. Reviewer sees evidence packet, not just label.
2. Reviewer assigns primary label: `scam_like`, `benign`, `uncertain`, or `insufficient_evidence`.
3. Reviewer assigns triage: `high_risk`, `medium_risk`, `low_risk`.
4. Reviewer selects reason codes.
5. Reviewer notes what extra evidence would change the decision.

Review design:

- Use at least two reviewers on a pilot subset when possible.
- Measure disagreement by label, triage, and reason codes.
- Track which cases are ambiguous because evidence is missing rather than because the taxonomy is poor.
- Keep adjudication notes concise and evidence-based.

## High / Medium / Low Triage Evaluation

| Triage level | Desired behavior | Evaluation |
|---|---|---|
| High | Strong evidence, urgent reviewer attention | high precision, evidence completeness, severe scam-family coverage |
| Medium | Suspicious but incomplete | useful second queue, missing-evidence clarity |
| Low | Mostly benign or weak evidence | low false-negative rate for severe scams |

The system should be tuned for high-risk precision first. Public-sector review teams need a queue that is worth opening.

## Evidence Completeness Scoring

Score each case from 0 to 5:

- 0: no usable evidence.
- 1: only text or only image, no context.
- 2: text/image plus weak reason codes.
- 3: content plus OCR or metadata.
- 4: content plus landing-page or destination evidence.
- 5: multi-layer evidence: creative, text/OCR, metadata, landing/redirect, reviewer note.

## Error Analysis Required

Every evaluation report must include:

- Top false positive categories.
- Top false negative categories.
- Scam families with poor performance.
- Surfaces with missing data.
- Model/rule explanations that reviewers rejected.
- Whether extra evidence would likely fix the error.

## Acceptance Target For Phase 1

Phase 1 does not need production-grade performance. It should show:

- A simple baseline exists.
- At least one multimodal/evidence combination improves review usefulness over text-only.
- The top recommended prototype can be explained and evaluated.
- The deferred scope is justified by data, cost, or evidence weakness.
