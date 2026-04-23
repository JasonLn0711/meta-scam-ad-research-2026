# Decision Memo: What Should We Actually Do First?

## Updated Recommendation

Under an approximate NTD 1.8M budget, build a documentation-led, evidence-centric triage research prototype focused on static/ad-like creative evidence:

- caption/post/ad text
- OCR from static images and carousel cards
- image + text + OCR combined review
- manual rules and keyword/risk-pattern baselines
- simple text/classical ML baseline if labels are sufficient
- high/medium/low triage
- reason codes
- evidence completeness scoring
- reviewer-facing evidence packet

Landing pages and metadata should be conditional add-ons, not assumed core features. Video, comments, Stories, graph analysis, and deepfake detection should remain future-roadmap or research-discussion items.

## Why This Is The Defensible First Move

The strongest first research contribution is not a flashy model. It is a clear answer to which cheap, lawful, explainable evidence signals help reviewers prioritize scam-like Meta content.

This path is defensible because it:

- fits the budget better than broad multimodal coverage
- produces something demoable without live platform collection
- gives domain experts reason codes they can critique
- supports human review instead of automatic enforcement
- makes data gaps visible rather than hiding them behind a model score

## What To Cut From The First Prototype

- live Meta ingestion
- automated scraping
- production dashboard
- Stories
- long video
- full Reels/short-video processing
- comments/replies analysis
- profile graph/network analysis
- definitive deepfake detection
- VLM/LLM scoring for every item
- full landing-page crawling or cloaking detection

## What To Keep

- scope and data-governance work
- stakeholder scoping questions
- evidence contracts
- taxonomy and annotation guideline
- small governed sample or synthetic dry run
- text/OCR/static-image baselines
- image + caption + OCR hybrid triage
- reviewer evidence packet
- human review evaluation
- budget-fit recommendation

## What To Postpone

- short-video keyframe + ASR + OCR pilot
- landing-page sandboxing
- metadata enrichment beyond provided fields
- VLM-assisted explanations beyond a small sampled comparison
- comment/reply interaction patterns
- deepfake risk indicator benchmarking
- case-management dashboard

## First Meaningful Prototype

Prototype name: static creative evidence triage packet.

The prototype should take a small approved or synthetic case set and produce one review packet per case:

- source and authorization status
- content form
- caption/post text
- OCR text
- optional image reference
- risk level
- reason codes
- evidence completeness score
- missing evidence
- reviewer final label and notes

Implementation can be Markdown/CSV/JSONL first. A web UI is unnecessary for the first demo.

## Demo Guidance

Show in demo:

- 10-30 redacted, approved, or synthetic examples
- text/OCR extraction and simple baselines
- high/medium/low risk queue
- reason codes and evidence completeness
- reviewer packet before/after human judgment
- an ablation showing why OCR or image+text matters

Keep as research discussion:

- live platform ingestion
- broader Meta data access
- landing-page cloaking detection
- video/Reels pipeline
- comments/replies
- deepfake detection
- production enforcement workflow

## Decision

Proceed with the static creative evidence triage research MVP. Treat landing pages and metadata as gated add-ons. Treat video, comments, Stories, graph analysis, and deepfake detection as future scope requiring additional authorization, data, and budget.
