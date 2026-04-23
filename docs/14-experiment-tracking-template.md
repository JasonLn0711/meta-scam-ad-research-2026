# Experiment Tracking Template

Copy this template into `experiments/YYYY-MM-DD-short-name.md`.

## Experiment Identity

- Experiment ID:
- Date:
- Owner:
- Status: planned / running / completed / dropped
- Related decision:

## Hypothesis

State one testable claim.

Example: "Adding OCR text from scam-ad images improves high-risk recall over caption-only screening without increasing reviewer burden by more than 20%."

## Dataset Slice

- Source:
- Authorization status:
- Number of items:
- Scam families:
- Content forms:
- Benign comparator strategy:
- Known sampling bias:

## Evidence Fields Used

- Caption/post text:
- OCR text:
- Image:
- Video keyframes:
- ASR:
- Landing page:
- Metadata:
- Reviewer labels:

## Model / Pipeline

- Pipeline type:
- Rules or keywords:
- Model name/version:
- Prompt/version if LLM/VLM used:
- Feature extraction:
- Score aggregation:
- Human review step:

## Cost

- Compute cost:
- API/model cost:
- Human annotation minutes:
- Human review minutes:
- Engineering time:

## Metrics

- Precision:
- Recall:
- F1:
- High-risk precision:
- Review burden:
- Evidence completeness:
- Explanation usefulness:
- False-positive themes:
- False-negative themes:

## Results

Summarize quantitative and qualitative results.

## Observations

- What worked:
- What failed:
- What surprised us:
- What evidence was missing:
- Reviewer feedback:

## Decision

Choose one:

- Keep and expand.
- Keep as cheap baseline.
- Revise and rerun.
- Defer.
- Drop.

Decision rationale:

## Next Experiment

- Next hypothesis:
- Required data:
- Scope change:
