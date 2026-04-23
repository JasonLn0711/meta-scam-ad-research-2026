# Next-Step Execution Plan

## First 2 Weeks

Goal: lock scope, data posture, taxonomy, and first evidence schema.

Tasks:

- Confirm stakeholders and owners: anti-fraud office, CIB, 165 platform owners, legal/policy contact, technical reviewer.
- Run data-access interview: what examples, fields, screenshots, URLs, labels, reports, and metadata can be provided?
- Review platform/legal constraints and record decisions in `governance/data-governance.md`.
- Finalize taxonomy v0.1 from `docs/04-taxonomy.md`.
- Finalize annotation guideline v0.1 from `docs/13-annotation-guideline-draft.md`.
- Define minimum evidence schema from `docs/03-data-strategy.md`.
- Draft procurement-safe scoping memo.
- Create 5-10 synthetic or public non-sensitive examples only for pipeline dry run if real data is not yet approved.

Milestones:

- Data access decision log updated.
- Stakeholder open questions sent.
- Phase 1 surfaces confirmed.
- No automated Meta collection performed.

## First 4 Weeks

Goal: run a governed pilot sample and baseline comparisons.

Tasks:

- Build or collect a small approved pilot sample.
- Label pilot data with two reviewers where possible.
- Record annotation disagreement and revise taxonomy.
- Run manual rule and keyword/risk-pattern baseline.
- Run OCR extraction and OCR + keyword baseline.
- Run text classifier baseline if enough labels exist.
- Test image-only or image-embedding baseline.
- Evaluate image + text + OCR combined pipeline.
- Decide whether landing-page evidence can be included.

Milestones:

- Pilot annotation report.
- Baseline comparison table.
- False positive / false negative examples.
- Phase 2 prototype decision.

## First 8 Weeks

Goal: build and evaluate narrowed research prototype.

Tasks:

- Implement evidence normalization for approved fields.
- Implement hybrid triage scoring.
- Generate evidence packet per case.
- Add reviewer feedback fields.
- Evaluate high/medium/low risk queue.
- Measure evidence completeness and review burden.
- Run ablations: without OCR, without image, without landing page, without metadata.
- Draft final decision memo and budget-fit roadmap.

Milestones:

- Prototype demo on approved or synthetic sample.
- Human-review evaluation.
- Decision memo with scope recommendation.
- Future roadmap for video, comments, deepfake, and platform partnership.

## What Data To Collect First

Priority order:

1. Confirmed or suspected scam examples from stakeholders with permission.
2. Benign comparator examples in the same domains.
3. Captions/post text and screenshots.
4. OCR text from images.
5. Destination URLs and landing-page evidence if authorized.
6. Limited metadata fields if available.
7. Short-video examples only after Phase 1 is stable.

## Prototype To Build First

Build a research prototype that accepts a small case record and outputs:

- risk level
- label suggestion
- reason codes
- evidence completeness score
- reviewer decision fields

Do not build a dashboard first. A Markdown/CSV/JSONL pipeline and evidence packet is enough for early research.

## Checkpoints

| Checkpoint | Decision |
|---|---|
| End of week 2 | Are data and labels viable? |
| End of week 4 | Which modalities improve triage? |
| End of week 8 | Is the budget-fit prototype worth expanding? |
