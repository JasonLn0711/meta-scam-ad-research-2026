# 2026-04-23 Project Setup And Scope Refinement

## Identity

- Date: 2026-04-23
- Session type: project setup, research strategy, scope refinement
- Participants: Jason + Codex
- Related planning note: `/home/jnln3799/every_on_git_ubuntu/planning-everything-track/weeks/2026-W17/days/2026-04-23.md`

## Context

Jason received an opportunity related to a Criminal Investigation Bureau / Executive Yuan anti-fraud office research project on "Meta platform scam-ad detection." The heard budget context was about NTD 3.0M total, split roughly into NTD 1.2M for 165 information-platform integration research and NTD 1.8M for Meta scam-ad detection research.

The initial concern was that the full problem space is too large for NTD 1.8M: Facebook, Instagram, Threads, static images, captions, short video/Reels, longer video, Stories, carousel posts, comments/replies, metadata, landing pages, redirection, and possible deepfake indicators.

## What Was Done

- Created a new sibling repo: `/home/jnln3799/every_on_git_ubuntu/meta-scam-ad-research`.
- Initialized it as an independent Git repo on `main`.
- Created a documentation-first research starter kit.
- Added formal docs `00` to `18`.
- Added data governance, experiment templates, proposal folder, logs, and minimal scripts/source placeholders.
- Added collaboration scaffolding: `notes/`, `templates/`, `data-contracts/`, `decision-log/`, and experiment subfolders.
- Ran a second-pass refinement to cut overly broad or low-ROI branches from the first prototype.
- Created separate Git commits for the initial repo, budget narrowing, and collaboration scaffolding.

## Key Decision

The project should be framed as:

> evidence-centric scam-ad triage research

not:

> Meta-wide scam-ad detection system

This distinction protects the NTD 1.8M budget from scope creep and makes the project easier to defend to professors, anti-fraud domain experts, public-sector stakeholders, and engineering teammates.

## Strongest First Scope

Keep as first prototype core:

- caption/post/ad text
- OCR from static images
- image + caption + OCR
- carousel as image-set variant
- manual rules and keyword/risk-pattern baselines
- evidence completeness scoring
- human reviewer packet

Conditional only:

- landing-page text/screenshots/URLs
- redirect/destination evidence
- limited post/profile/page metadata
- sampled VLM explanation comparison

Cut from first prototype:

- live Meta ingestion
- automated scraping
- production dashboard
- Stories
- long video
- full Reels / short-video pipeline
- comments/replies analysis
- profile graph/network analysis
- definitive deepfake detection
- VLM/LLM scoring for every item
- automated enforcement decisions

## Git Checkpoint

- `4a38dc2 docs: initialize Meta scam ad research repo`
- `da62db8 docs: narrow budget-fit research path`
- `a473630 docs: add collaboration scaffolding`

## Next Step

Draft a one-page stakeholder scoping memo using:

- `templates/scoping-memo.md`
- `docs/12-open-questions-for-stakeholders.md`
- `docs/10-decision-memo.md`
- `docs/17-recommended-path.md`

The memo should ask what data can be lawfully provided, which scam families matter most, what reviewer workflow exists, and what this research should explicitly avoid promising.

## Promote / Park

- Promoted to durable decision: `decision-log/0002-budget-fit-static-creative-triage.md`.
- Parked: video, comments, Stories, deepfake, graph, live ingestion, and production dashboard.
