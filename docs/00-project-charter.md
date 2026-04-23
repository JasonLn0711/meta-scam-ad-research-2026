# Project Charter

## Objective

Design and evaluate a realistic research program for detecting scam-like advertisements and ad-adjacent content related to Meta platforms. The project should help public-sector stakeholders decide what can be measured, what can be triaged, what can be prototyped, and what should not be promised under an approximate NTD 1.8M research budget.

## Problem Framing

The practical problem is not simply "classify an ad as scam or not scam." Real scam-ad operations combine several layers:

- Creative layer: images, captions, video, celebrity or brand impersonation, fake endorsements, urgency language, unrealistic financial or health claims.
- Interaction layer: comments, replies, direct-message lures, engagement bait, off-platform chat migration.
- Destination layer: landing pages, redirects, cloaking, forms, fake payment pages, subscription traps.
- Actor layer: advertiser/page/profile metadata, repeated domains, reused creatives, suspicious account behavior.
- Review layer: human investigators need evidence, triage priority, and explainable reasons, not just model scores.

The core research question is: which affordable evidence pipeline gives investigators the best combination of coverage, precision, recall, explainability, and review-burden reduction?

## Non-Goals

- No production enforcement system.
- No guarantee of full coverage across Facebook, Instagram, Threads, Stories, Reels, comments, and external pages.
- No unauthorized scraping or automated collection from Meta products.
- No definitive deepfake detector.
- No replacement for human legal, investigative, or platform-policy review.
- No permanent database of personal data unless approved by the data-governance process.

## Success Criteria

The project succeeds if it produces:

- A clear map of candidate surfaces, modalities, evidence sources, and budget tradeoffs.
- A lawful, documented data strategy with fragile assumptions made explicit.
- A scam-pattern and evidence taxonomy usable by annotators and engineers.
- Baseline experiments comparing rules, text, OCR, image, multimodal, landing-page, and hybrid review approaches.
- A narrow prototype design that supports high/medium/low triage and evidence packets.
- A decision memo that tells stakeholders what should be done first under NTD 1.8M.

## Budget Reality

NTD 1.8M is enough for a serious research sprint, not a full Meta-scale safety system. The budget should be spent on:

- Scoping and stakeholder alignment.
- Legal/data-access review.
- Small but meaningful dataset design.
- Annotation guideline and pilot labels.
- Baseline and hybrid pipeline experiments.
- Human-review evaluation.
- Final recommendation and future roadmap.

It should not be spent trying to build every ingestion path, every video model, every deepfake detector, and every platform integration in one pass.

## Why Progressive Narrowing Is Required

The project starts broad because early narrowing may miss high-value surfaces, especially landing-page and metadata signals. It must then narrow quickly because unrestricted scope will exceed budget and produce weak evidence.

Narrowing criteria:

- Lawful data access.
- Investigative value.
- Annotation feasibility.
- Compute cost.
- Explainability.
- Human review usefulness.
- False-positive harm.
- Stakeholder ability to act on results.

## Working Principle

Explore wide. Measure cost. Preserve evidence. Narrow hard. Prototype only the slice that is defensible.
