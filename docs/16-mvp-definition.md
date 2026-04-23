# MVP Definition

## Second-Pass MVP Principle

The MVP must be meaningful but not theatrical. It should demonstrate a real research workflow that stakeholders can critique, not a broad product illusion.

The first MVP should be an evidence-packet generator for static/ad-like creatives. It should prove whether text, OCR, and image-context evidence can support human triage under a realistic budget.

## MVP Candidate 1: Scoping And Evidence Readiness MVP

Purpose: make the project safe to execute.

Includes:

- stakeholder question set
- data-governance posture
- data contracts
- taxonomy v0.1
- annotation guideline v0.1
- small synthetic or approved dry-run case format

Use: first 2 weeks.

This is required before any model or demo is credible.

## MVP Candidate 2: Budget-Fit Research MVP

Purpose: demonstrate a narrow but real triage workflow.

Includes:

- small approved or synthetic case set
- text/caption baseline
- OCR + keyword baseline
- image + caption + OCR hybrid triage
- reason codes
- evidence completeness score
- reviewer evidence packet
- human-review result field
- simple ablation table

Does not include:

- live Meta collection
- video/Reels processing
- Stories
- comments/replies
- deepfake detection
- profile graph analysis
- full dashboard
- automated enforcement

Use: primary Phase 1-2 target.

## MVP Candidate 3: Gated Evidence Add-On MVP

Purpose: test whether destination or metadata evidence materially improves triage.

Includes only if approved:

- stakeholder-provided landing-page text/screenshots/URLs
- limited metadata fields
- destination reason codes
- comparison against content-only triage

Use: conditional add-on. Do not promise it until data access is confirmed.

## MVP Candidate 4: Future Scaled System MVP

Purpose: future operational system.

Includes:

- continuous ingestion
- video, comments, Stories, graph signals
- landing-page sandbox
- model monitoring
- reviewer dashboard
- case management
- deepfake benchmark service

Use: future roadmap only. This is not realistic for NTD 1.8M.

## MVP Comparison

| MVP | Research value | Engineering cost | Data risk | Budget fit | Demo? |
|---|---:|---:|---:|---:|---|
| Scoping and evidence readiness | High | Low | Low | Strong | show docs/contracts |
| Budget-fit research MVP | Very high | Medium | Medium | Strong | yes, main demo |
| Gated evidence add-on | High if approved | Medium | Medium-high | Conditional | only if data is ready |
| Future scaled system | High in theory | Very high | Very high | Poor | no |

## Definition Of Done For Budget-Fit Research MVP

- Data access decisions recorded.
- Evidence schema and annotation schema defined.
- Pilot case set created with approved or synthetic data.
- Manual rule and keyword baseline completed.
- OCR baseline completed.
- Image + caption + OCR hybrid triage completed.
- Evidence packet generated for each case.
- Human reviewer can assign final label, triage, and notes.
- Evaluation reports high-risk precision, review burden, evidence completeness, false-positive themes, and false-negative themes.
- Decision memo clearly states what to keep, cut, postpone, and fund next.

## Demo Boundary

Demo the research workflow, not a surveillance product.

Demo:

- static creative evidence packet
- small case set
- transparent baselines
- reason codes
- triage queue
- reviewer judgment field

Do not demo:

- live scraping
- real-time monitoring
- deepfake claims
- video pipeline
- comments/replies mining
- enforcement decisions
