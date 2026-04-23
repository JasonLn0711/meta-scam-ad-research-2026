# Repo Relationships

## First-Principles Axiom

A repo is a decision surface.

It should have one obvious answer to:

1. What kind of object lives here?
2. What future action does this object support?
3. Who owns the durable context?
4. What lifecycle state is the object in?
5. What should a future human or AI agent do next?

The goal is not to connect every file. The goal is to preserve clear ownership so the research can narrow without losing strategic memory.

## Current Topology

```text
/home/jnln3799/every_on_git_ubuntu/
├── planning-everything-track/
│   └── data/projects/2026-04-meta-scam-ad-research.md
├── meta-scam-ad-research-2026/
│   ├── docs/19-repo-relationships.md
│   └── decision-log/0004-create-threads-first-child-repo.md
└── meta-threads-scam-content-research-2026/
    └── docs/21-repo-relationships.md
```

## Canonical Roles

| Repo | Role | Owns | Does not own |
|---|---|---|---|
| `planning-everything-track` | Control plane | Priority, status, capacity, deadlines, next actions, weekly/daily execution memory | Research schemas, annotation details, experiment logs, copied research docs |
| `meta-scam-ad-research-2026` | Umbrella strategy repo | Cross-Meta framing, budget logic, scope tradeoffs, roadmap, why Threads split out | Detailed Threads dataset iterations or baseline outputs |
| `meta-threads-scam-content-research-2026` | Threads execution repo | Threads taxonomy, data contract, annotation guide, phase-1 experiments, baseline logs, evaluation memos | Life planning, all-Meta promises, unrelated platform expansion |

## Ownership Rule

Use this split:

```text
planning repo = why / when / priority / status / reflection / capacity
umbrella research repo = broad strategy / scope history / cross-platform roadmap
Threads repo = what is studied / labeled / tested / evaluated for Threads phase 1
```

## Bridge Documents

| Bridge | Location | Purpose |
|---|---|---|
| Planning project note | `../planning-everything-track/data/projects/2026-04-meta-scam-ad-research.md` | Current priority, next action, and repo pointers |
| Umbrella relationship doc | `docs/19-repo-relationships.md` | Source of truth for repo ownership from umbrella perspective |
| Threads relationship doc | `../meta-threads-scam-content-research-2026/docs/21-repo-relationships.md` | Source of truth for Threads execution repo boundaries |
| Scope split decision | `decision-log/0004-create-threads-first-child-repo.md` | Durable decision explaining why the child repo exists |

## Update Rules

| Event | Planning repo | Umbrella repo | Threads repo |
|---|---|---|---|
| Weekly priority or deadline changes | Update project note or weekly plan | No change | No change |
| Major scope change | Short status update | Decision log and scope docs | Update if Threads scope changes |
| Threads schema or annotation change | No change | No change unless strategy changes | Update schema, docs, and templates |
| Threads experiment result | Short status only | Summary only if it changes strategy | Full experiment log |
| Stakeholder changes budget or authority | Update planning note | Update decision/budget docs | Update phase plan if affected |
| Data governance change | Link to decision | Update governance if broad | Update governance if Threads-specific |

## Anti-Duplication Rules

Do not:

- Copy all Threads docs into this umbrella repo.
- Copy umbrella strategy docs into the Threads repo.
- Store raw or sensitive evidence in any bridge document.
- Turn `planning-everything-track` into the research source of truth.
- Use git submodules, automated sync, or generated mirrors during phase 1.
- Let this umbrella repo continue to imply that phase 1 is broad all-Meta work when Threads is the active focused path.

## Milestone Sync Protocol

At the end of each major milestone:

1. Update the Threads repo with the detailed experiment result or memo.
2. Add a one-paragraph strategic summary here only if the result changes broader scope.
3. Update the planning project note with next action, blocked status, or review date.
4. Record a decision log entry if the milestone changes scope, budget, data posture, or production boundary.

## Current Active Path

The active child execution path is:

```text
../meta-threads-scam-content-research-2026
```

The active phase-1 MVP is Threads scam-like content triage using text, text plus image/OCR, comments/replies, visible redirection signals, and external links when present. It remains research-first and human-review-oriented.
