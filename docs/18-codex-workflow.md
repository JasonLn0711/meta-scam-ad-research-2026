# Codex Workflow

## Purpose

Future Codex sessions should keep this repo coherent, evidence-based, and low chaos.

## Startup Routine

1. Read `README.md`.
2. Read `AGENTS.md`.
3. Read `docs/00-project-charter.md`.
4. Read `docs/17-recommended-path.md`.
5. Check `git status --short`.
6. Before touching data-related files, read `governance/data-governance.md` and `data-contracts/README.md`.

## File Update Rules

- If rough thinking or a meeting is not yet durable, put it under `notes/`.
- If scope changes, update `docs/01-scope-map.md`, `docs/07-budget-fit-analysis.md`, and add or revise a record under `decision-log/`.
- If labels or reason codes change, update `docs/04-taxonomy.md` and `docs/13-annotation-guideline-draft.md`.
- If a data shape changes, update `data-contracts/` before code or experiments rely on it.
- If experiments change, update `docs/05-experiment-program.md` and add an experiment log under the relevant `experiments/` subfolder.
- If data posture changes, update `governance/data-governance.md` before implementation.
- If proposal language changes, keep non-promises consistent with `docs/10-decision-memo.md`.
- If code becomes useful, keep it minimal and make sure it follows an existing data contract.

## Branch Strategy

- Use short branch names when a branch is needed, such as `docs/scoping-memo` or `exp/ocr-baseline`.
- Do not create branches, commits, pulls, or pushes without explicit user confirmation in the current session.
- Keep generated artifacts out of Git unless intentionally approved.

## Experiment Note Discipline

Every experiment must have:

- hypothesis
- dataset slice
- authorization status
- pipeline
- cost
- metrics
- observations
- narrowing decision

Do not add experiments that do not inform a scope, data, model, or review decision.

Use these experiment subfolders:

- `experiments/modality-studies/` for modality comparisons.
- `experiments/baselines/` for rules, keyword, OCR, classical ML, and text/image baselines.
- `experiments/evaluation-notes/` for reviewer feedback, error analysis, and metric interpretation.

## Data Safety

- Do not commit raw sensitive evidence.
- Use `.local/` for local scratch work.
- Use redacted examples in docs.
- Preserve source, timestamp, capture method, and permission status for evidence.
- Avoid personal-data expansion.

## How To Avoid Chaos

- Keep docs decision-oriented.
- Prefer tables over long essays when comparing scope.
- Keep filenames stable, explicit, and future-proof.
- Use `templates/` for repeated Markdown artifacts.
- Do not add a dashboard before the research workflow is proven.
- Do not add heavy dependencies before simple baselines are evaluated.
- Do not add code before the data contract and experiment purpose are clear.
- Do not let deepfake, video, or graph work steal Phase 1 focus unless stakeholder data makes it unavoidable.

## Done Criteria For A Codex Session

- Files changed are listed in the final response.
- Any assumptions are explicit.
- Any tests or verification commands are reported.
- No hidden data collection or platform automation occurred.
