# Decision 0001: Initial Docs-First Research Architecture

## Identity

- Date: 2026-04-23
- Status: accepted
- Owner: project starter

## Decision

Organize this repo as documentation-first, experiment-second, code-third.

## Context

The project is a public-sector research effort with professors, anti-fraud domain experts, and engineering teammates as likely collaborators. The main risk is not lack of code; it is premature technical commitment before data access, legal posture, taxonomy, annotation, and budget-fit scope are clear.

## Options Considered

| Option | Pros | Cons | Decision |
|---|---|---|---|
| Code-first prototype | Fast demo | Over-promises and hides data/legal uncertainty | Rejected |
| Docs-only folder | Low friction | Experiments may become scattered | Rejected |
| Docs-first with explicit experiment and data-contract layers | Stable collaboration structure, future-proof, low code pressure | Slightly more upfront structure | Accepted |

## Rationale

The repo should make the reasoning visible before implementation. Data contracts and decision logs prevent hidden assumptions. Experiment subfolders keep technical work organized without requiring a heavy software architecture.

## Consequences

- `docs/` remains the formal research spine.
- `notes/` captures rough thinking and meetings.
- `data-contracts/` defines schemas before code.
- `experiments/` is organized by modality studies, baselines, and evaluation notes.
- `templates/` standardizes repeated Markdown work.
- `src/` remains a placeholder until a prototype is justified.

## Files To Update

- README.md
- AGENTS.md
- docs/18-codex-workflow.md
