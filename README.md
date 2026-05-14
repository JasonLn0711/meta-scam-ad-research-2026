# Meta Scam Ad Research

<img src="http://estruyf-github.azurewebsites.net/api/VisitorHit?user=JasonLn0711&repo=meta-scam-ad-research-2026&countColor=%237B1E7B" alt="Visitor count"/>
Research starter kit for the "Meta platform scam-ad detection" project. The working scope includes scam-like advertising and ad-adjacent content on Facebook, Instagram, Threads, and related off-platform landing pages where lawful evidence is available.

This repository is intentionally framed as a research program, not a production detection product. The budget reality is approximately NTD 1.8M for this subproject. That can support serious scoping, evidence design, a governed dataset slice, exploratory baselines, and a budget-fit prototype. It cannot support full cross-platform production ingestion, complete deepfake detection, comprehensive video moderation, or guaranteed enforcement accuracy across all Meta surfaces.

## Why This Is Research, Not A Full Product

Scam ads are a moving adversarial target. Public reporting and Meta's own public updates point to tactics such as celebrity impersonation, brand impersonation, cloaking, subscription fraud, investment lures, fake e-commerce, AI-generated media, and off-platform redirection. A credible project must therefore answer three questions before building too much:

- What evidence can be lawfully and repeatably obtained?
- Which content surfaces have high investigative value at acceptable data, annotation, and compute cost?
- Which prototype can reduce review burden or improve triage without pretending to replace platform enforcement?

The first principle is: start broad enough to map the opportunity space, then narrow based on evidence, cost, feasibility, and operational value.

## Scope Assumptions

- Primary research target: scam-like ad creatives and ad-adjacent content involving Meta platforms.
- Phase 1 scope: static images, image + caption posts/ads, text lure content, OCR text, carousel-as-image-set, landing-page evidence if authorized, and limited metadata if lawfully available.
- Phase 2 scope: short video/Reels keyframes, ASR, video OCR, limited comment/reply patterns, and deepfake risk indicators.
- Deferred: Stories, long-form video, full Threads-wide collection, full profile graph analysis, and definitive deepfake detection.
- Data posture: authorization-first. Do not automate Meta data collection without written permission, approved API access, or a legally reviewed stakeholder-provided dataset.

## High-Level Roadmap

| Phase | Goal | Main outputs | Stop/go question |
|---|---|---|---|
| Phase 0 | Problem framing and data audit | Charter, stakeholder questions, legal/data access review, taxonomy v0.1 | What evidence can we use safely? |
| Phase 1 | Broad scan and exploratory baselines | Small governed sample, rules/keywords/OCR/text/image baselines, annotation guideline v0.1 | Which low-cost signals have real triage value? |
| Phase 2 | Narrowed multimodal prototype | Hybrid triage prototype for best-ROI surfaces, reviewer workflow, evidence pack | Can this reduce review burden with explainable evidence? |
| Phase 3 | Evaluation and decision memo | Metrics, human review results, budget-fit recommendation, future roadmap | What should be funded next, if anything? |
| Phase 4 | Future expansion | Optional video, graph, deepfake, and cross-platform roadmap | What requires new budget or platform partnership? |

## Recommended First Technical Path

Build an evidence-centric hybrid triage pipeline for:

- text and captions
- OCR from static images and carousel images
- static image risk signals
- landing-page evidence when lawfully obtained
- limited post/profile/page metadata when lawfully obtained
- human review with explainable risk reasons

This path is the best fit for NTD 1.8M because it maximizes investigative usefulness while avoiding the most expensive and fragile parts of the problem: full video understanding, Stories, Threads-wide collection, profile graph modeling, and definitive deepfake detection.

## Repo Structure

```text
docs/           Formal research design, scope, evaluation, and stakeholder-facing memos
notes/          Rough thinking, meeting notes, and early synthesis before promotion
experiments/    Experiment plans and results, organized by modality, baselines, and evaluation
templates/      Reusable Markdown templates for notes, decisions, interviews, and experiments
data-contracts/ Stable dataset schemas and evidence field definitions
data/           Governance-only data layout; raw sensitive data should not be committed
decision-log/   Durable architecture, scope, and research-direction decisions over time
governance/     Data access, privacy, legal, and platform-risk notes
proposals/      Procurement-facing drafts and future proposal text
logs/           General project logs and lightweight history
scripts/        Minimal helper scripts only when useful; standard library first
src/            Future prototype code, if approved; code is third priority
notebooks/      Exploratory notebooks; do not commit sensitive outputs
.local/         Ignored local-only working area
```

## Related Repos

This repo is now the umbrella strategy repo for the Meta scam-risk research family.

| Repo | Role |
|---|---|
| `../planning-everything-track` | Personal/project control plane for priority, status, deadlines, and next actions. |
| `../meta-threads-scam-content-research-2026` | Active Threads-first child research repo for phase-1 scam-like content triage. |

Read `docs/19-repo-relationships.md` and `decision-log/0004-create-threads-first-child-repo.md` before moving scope between repos.

## How To Use This Repo

1. Read `docs/00-project-charter.md` to understand the project boundary.
2. Read `docs/01-scope-map.md` and `docs/07-budget-fit-analysis.md` before promising scope.
3. Use `notes/meetings/` for stakeholder and professor meetings; promote only durable conclusions.
4. Use `data-contracts/` before creating code or experiment files that assume a data shape.
5. Use `docs/13-annotation-guideline-draft.md` before labeling any examples.
6. Log every experiment under `experiments/modality-studies/`, `experiments/baselines/`, or `experiments/evaluation-notes/`.
7. Keep durable scope and architecture decisions in `decision-log/`.
8. Keep data access decisions in `governance/data-governance.md`.
9. Use `docs/19-repo-relationships.md` to route work between the planning repo, umbrella repo, and Threads child repo.

## Collaboration Order

The repo is documentation-first, experiment-second, code-third.

1. Documentation first: clarify scope, taxonomy, data contracts, stakeholder needs, and budget-fit boundaries.
2. Experiments second: run small, explicit studies that answer narrowing decisions.
3. Code third: add minimal scripts or prototype code only after the data contract and experiment need are clear.

## Evidence Anchors

These sources should be reviewed and cited carefully in proposals and literature scans:

- Meta Automated Data Collection Terms: https://www.facebook.com/legal/automated_data_collection_terms
- Meta Ad Archive/API announcement: https://about.fb.com/news/2018/08/introducing-the-ad-archive-api/
- Meta legal action against scam advertisers, celeb-bait, deepfake, cloaking, subscription fraud: https://about.fb.com/news/2026/02/meta-takes-legal-action-against-scam-advertisers/
- Meta 2026 scam enforcement and partnership update: https://about.fb.com/news/2026/03/fighting-scammers-protecting-people-with-new-technology-and-partnerships/
- FTC social media scam loss report: https://www.ftc.gov/news-events/news/press-releases/2023/10/ftc-data-shows-consumers-report-losing-27-billion-social-media-scams-2021

## Non-Promise Statement

This project should not promise to solve Meta scam ads across every platform, modality, and adversarial tactic. It should promise a defensible research path: map the problem, govern the data, compare feasible evidence pipelines, build a narrow prototype, and produce a decision memo that tells public-sector stakeholders what is realistic next.
