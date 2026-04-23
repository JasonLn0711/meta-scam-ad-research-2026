# AGENTS.md

This repository is a Markdown-first research operating system for the Meta scam-ad research project.

## Mission

Help maintain a serious, budget-aware research program for scam-like advertising and ad-adjacent content on Meta platforms. The repo should support stakeholder scoping, evidence design, annotation, experiments, evaluation, and recommendation memos.

## Hard Boundaries

1. Do not automate Meta data collection without explicit written authorization, approved API access, or legal/stakeholder approval recorded in `governance/data-governance.md`.
2. Do not commit raw personal data, screenshots containing unnecessary personal information, credentials, tokens, exported browser profiles, or sensitive investigative material.
3. Do not claim the project can solve full-platform scam-ad detection in production.
4. Do not turn this repo into a web app, dashboard, database product, or heavy ML platform unless a later decision log explicitly authorizes that scope.
5. Preserve evidence fields and uncertainty. Suspicion is not guilt; weak evidence must stay labeled as weak evidence.

## Working Style

- Prefer Markdown, CSV, JSONL, and simple Python.
- Keep the repo documentation-first, experiment-second, code-third.
- Create clean docs, notes, data contracts, and experiment plans before adding code.
- Keep public-sector usability in mind: explain what can be defended, what is fragile, and what requires stakeholder data or platform cooperation.
- Every experiment should state hypothesis, dataset slice, pipeline, cost, results, and the narrowing decision it informs.
- Every model or rule output should preserve explainable reasons and evidence references.
- Legal, platform, and privacy constraints are first-class research constraints.

## Priority Order

1. Sustainability and lawful data handling
2. Research clarity
3. Evidence quality
4. Budget fit
5. Operational usefulness
6. Automation
7. Aesthetics

## Future Agent Workflow

- Start with `README.md`, `docs/00-project-charter.md`, `docs/17-recommended-path.md`, and `governance/data-governance.md`.
- Use `notes/` for meeting notes and rough thinking before promoting durable conclusions.
- Before changing scope, update `docs/01-scope-map.md`, `docs/07-budget-fit-analysis.md`, and `decision-log/`.
- Before relying on a data field, define it in `data-contracts/`.
- Before changing annotation labels, update `docs/04-taxonomy.md` and `docs/13-annotation-guideline-draft.md`.
- Before adding experiments, create or update an experiment log under `experiments/modality-studies/`, `experiments/baselines/`, or `experiments/evaluation-notes/`.
- Keep `scripts/` and `src/` minimal until experiments justify code.
