# Recommended Path

## 2026-04-23 Threads-First Update

This document records the umbrella repo's sharp second-pass recommendation for a broad Meta scam-ad research path. Later on `2026-04-23`, the active phase-1 execution surface narrowed to Threads scam-like content and moved into the sibling child repo:

```text
../meta-threads-scam-content-research-2026
```

For current Threads-specific schema, annotation, comments/replies, OCR, link-signal, and phase-1 experiment decisions, use the child repo. This umbrella repo keeps the broader strategy, budget logic, and scope history.

## Sharp Second-Pass Recommendation

Sell and build this as evidence-centric scam-ad triage research, not Meta-wide scam-ad detection.

The first prototype should be a static creative evidence triage packet for text, OCR, and image+caption evidence. It should help reviewers prioritize and explain cases. It should not imply live monitoring, platform-scale detection, or deepfake capability.

## Keep Now

- authorization-first data posture
- stakeholder and professor-facing scoping docs
- data contracts before code
- scam taxonomy and annotation guideline
- text/caption baseline
- OCR from images and carousel cards
- image + caption + OCR hybrid triage
- high/medium/low risk queue
- reason codes
- evidence completeness scoring
- reviewer evidence packet
- human review evaluation

## Conditional Add-Ons

Add only if data access is confirmed:

- landing-page text/screenshots/URLs
- redirect or destination evidence
- limited post/profile/page metadata
- sampled LLM/VLM explanation comparison on approved redacted samples

These should be framed as gated experiments, not promised core deliverables.

## Cut From First Prototype

- live Meta ingestion
- automated scraping
- production dashboard
- full Facebook/Instagram/Threads coverage
- Stories
- long video
- full short-video/Reels pipeline
- comments/replies analysis for the broad all-Meta prototype; sampled Threads replies/comments now live in the child repo
- profile graph/network analysis
- definitive deepfake detection
- VLM/LLM scoring for every item
- automated enforcement decisions

## Postpone To Future Roadmap

- short-video keyframe + ASR + OCR pilot
- landing-page sandbox and cloaking study
- comment/reply interaction pattern analysis
- domain/account clustering
- deepfake risk benchmark
- reviewer dashboard
- platform partnership/API integration

## Strongest Modality / Surface Candidates

| Candidate | Why strong | Status |
|---|---|---|
| Caption/post text | cheap, explainable, directly captures lure language | core |
| OCR from static images | likely catches embedded scam claims | core |
| Image + caption + OCR | best first multimodal ROI | core |
| Carousel as image-set | can reuse static-image/OCR pipeline | bounded core |
| Landing-page evidence | high investigative value | conditional |
| Limited metadata | useful for prioritization if provided | conditional |

## First Meaningful Prototype

Build a Markdown/CSV/JSONL-level prototype that generates one reviewer packet per case.

Packet fields:

- case ID
- authorization status
- content form
- caption/text
- OCR text
- optional landing/metadata fields if approved
- risk level
- reason codes
- evidence completeness score
- missing evidence
- reviewer final label and notes

This is enough to demo the research value without over-engineering code.

## Demo Versus Discussion

Show:

- small redacted or synthetic case set
- text/OCR/static-image evidence flow
- baseline comparison
- triage queue
- evidence packet
- human review loop

Discuss only:

- Meta-wide data access
- live platform monitoring
- video/Reels
- comments/replies
- deepfake detection
- production dashboard

## Why This Is Budget-Defensible

NTD 1.8M should buy clarity, evidence, and a narrow prototype. The recommended path protects that budget by cutting expensive modalities, avoiding unauthorized collection, and proving value against transparent baselines before adding heavier AI.

## Final Position

Do the narrow prototype first. Use the broad map to explain what was considered and why it was cut. The strongest stakeholder-facing message is: this project identifies the highest-value affordable evidence signals for human triage and defines what additional data, authority, and budget would be needed for broader detection.
