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

- Created a new sibling repo, later renamed to include the project year: `/home/jnln3799/every_on_git_ubuntu/meta-scam-ad-research-2026`.
- Initialized it as an independent Git repo on `main`.
- Created a documentation-first research starter kit.
- Added formal docs `00` to `18`.
- Added data governance, experiment templates, proposal folder, logs, and minimal scripts/source placeholders.
- Added collaboration scaffolding: `notes/`, `templates/`, `data-contracts/`, `decision-log/`, and experiment subfolders.
- Ran a second-pass refinement to cut overly broad or low-ROI branches from the first prototype.
- Created separate Git commits for the initial repo, budget narrowing, and collaboration scaffolding.

## Same-Day Threads-First Update

After the umbrella repo was set up, the project scope was updated based on stakeholder discussion: phase 1 should focus on Threads-related scam or scam-like content rather than all Meta platforms at once.

What changed:

- Created the dedicated sibling repo `/home/jnln3799/every_on_git_ubuntu/meta-threads-scam-content-research-2026`.
- Chose `meta-threads-scam-content-research-2026` to align with the `meta-scam-ad-research-2026` naming family while reflecting Threads-specific content, not only ads.
- Added a repo-series naming rule: `meta-[scope]-[risk-domain]-[content-surface]-research-[year]`.
- Built the Threads repo as a docs-first research scaffold with README, AGENTS, docs `00` to `21`, governance, data contract, templates, notes, and experiment folders.
- Defined Threads phase-1 scope around text posts, text plus image posts, replies/comments, OCR text, visible redirection signals, external links, and human-review-oriented triage.
- Deferred long video, heavy short-video pipelines, deepfake detection as a mainline workstream, full Meta cross-platform integration, automated collection, production deployment, and heavy model training.
- Connected the planning repo, umbrella repo, and Threads repo with explicit relationship documents rather than submodules, sync scripts, or duplicated live docs.

The updated repo split is:

```text
planning-everything-track = priority / status / capacity / next action
meta-scam-ad-research-2026 = umbrella strategy / broad Meta scope / decision memory
meta-threads-scam-content-research-2026 = Threads execution / schema / annotation / experiments / evaluation
```

## Key Decision

The project should be framed as:

> evidence-centric scam-ad triage research

not:

> Meta-wide scam-ad detection system

This distinction protects the NTD 1.8M budget from scope creep and makes the project easier to defend to professors, anti-fraud domain experts, public-sector stakeholders, and engineering teammates.

Same-day update:

> Threads-first scam-like content triage is the active phase-1 execution path.

This umbrella repo remains the broad strategy and decision-memory surface. The Threads repo owns the current executable research scaffold.

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
- sampled LLM/VLM explanation comparison on redacted samples

Cut from first prototype:

- live Meta ingestion
- automated scraping
- production dashboard
- Stories
- long video
- full Reels / short-video pipeline
- comments/replies analysis for the broad all-Meta umbrella prototype; sampled replies/comments later moved into the Threads child repo phase-1 scope
- profile graph/network analysis
- definitive deepfake detection
- VLM/LLM scoring for every item
- automated enforcement decisions

## Git Checkpoint

- `4a38dc2 docs: initialize Meta scam ad research repo`
- `da62db8 docs: narrow budget-fit research path`
- `a473630 docs: add collaboration scaffolding`

Rename note:

- Directory renamed from `meta-scam-ad-research` to `meta-scam-ad-research-2026` after setup.

Additional same-day artifacts:

- `decision-log/0004-create-threads-first-child-repo.md`
- `docs/19-repo-relationships.md`
- `../meta-threads-scam-content-research-2026/docs/21-repo-relationships.md`
- `../planning-everything-track/data/projects/2026-04-meta-scam-ad-research.md`

## Next Step

Draft a Threads-first stakeholder scoping memo using:

- the umbrella repo for broad stakeholder framing
- `../meta-threads-scam-content-research-2026/docs/16-open-questions-for-stakeholders.md`
- `../meta-threads-scam-content-research-2026/docs/18-recommended-path-v1.md`
- `../meta-threads-scam-content-research-2026/docs/09-phase-1-experiment-plan.md`

The memo should ask what Threads samples can be lawfully provided, what counts as report-worthy Threads content, which scam families matter most, what reviewer workflow exists, and what this research should explicitly avoid promising.

## Promote / Park

- Promoted to durable decision: `decision-log/0002-budget-fit-static-creative-triage.md`.
- Promoted to durable decision: `decision-log/0004-create-threads-first-child-repo.md`.
- Parked for umbrella phase 1: Stories, long video, heavy short-video pipelines, deepfake as a mainline workstream, graph/network analysis, live ingestion, production dashboard, and automated enforcement.
- Moved to Threads child repo phase 1: sampled replies/comments, OCR, visible redirection, and link-signal analysis.
