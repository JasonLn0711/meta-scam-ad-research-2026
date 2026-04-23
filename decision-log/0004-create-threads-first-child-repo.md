# Decision 0004: Create Threads-First Child Research Repo

## Identity

- Date: 2026-04-23
- Status: accepted
- Owner: Jason

## Decision

Create and treat `meta-threads-scam-content-research-2026` as the active Threads-first child research repo for phase-1 scam-like content research.

Keep `meta-scam-ad-research-2026` as the umbrella strategy repo for broader Meta scam-ad and ad-adjacent research framing.

The planning system remains in `planning-everything-track` and owns priority, status, capacity, deadlines, and next actions.

## Context

The original repo mapped the broader Meta scam-ad research opportunity across Facebook, Instagram, Threads, static creative evidence, landing-page evidence, video, comments, and future deepfake risk. Later stakeholder discussion suggested that Threads receives a high volume of scam-content reports, making Threads the best first narrow research target.

The project needs a sharper phase-1 execution surface without losing the broader strategic memory. A separate sibling repo gives Threads research its own taxonomy, schema, annotation guide, and experiment logs while preserving this umbrella repo as the place for cross-platform reasoning and future scope decisions.

## Options Considered

| Option | Pros | Cons | Decision |
|---|---|---|---|
| Keep all work in this umbrella repo | One location; no relationship layer needed | Threads phase-1 details would conflict with broader scope docs and create ambiguity | Rejected |
| Replace this repo with the Threads repo | Sharp focus | Loses broad Meta strategy, original budget framing, and future platform roadmap | Rejected |
| Create a sibling Threads child repo with explicit bridge docs | Clear ownership, preserves strategy, avoids duplication | Requires small cross-repo maintenance discipline | Accepted |
| Use git submodules or automated sync | Technical linkage | Adds maintenance cost before research needs it | Rejected for phase 1 |

## Rationale

First principle: a repo is a decision surface. Each repo should answer one primary question.

- `planning-everything-track`: what matters now, when, and with what capacity?
- `meta-scam-ad-research-2026`: what is the broader Meta scam-risk research strategy?
- `meta-threads-scam-content-research-2026`: what exactly are we studying, annotating, and testing for Threads phase 1?

This split keeps the work traceable without turning the repos into a monorepo, dashboard, or duplicated documentation pile.

## Consequences

- Threads-specific schemas, annotation rules, experiment logs, and phase-1 MVP details live in `../meta-threads-scam-content-research-2026`.
- This repo keeps the umbrella scope, budget logic, cross-platform roadmap, and major scope decisions.
- The planning repo links to both repos but does not copy research artifacts.
- Cross-repo updates should happen only at decision points, milestones, or status changes.
- No raw evidence, automated collection, or sensitive data should move between repos.

## Files To Update

- `docs/19-repo-relationships.md`
- `README.md`
- `docs/18-codex-workflow.md`
- `../meta-threads-scam-content-research-2026/docs/21-repo-relationships.md`
- `../planning-everything-track/data/projects/2026-04-meta-scam-ad-research.md`
