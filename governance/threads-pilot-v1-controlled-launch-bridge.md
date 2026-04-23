# Threads Pilot v1 Controlled Launch Bridge

## Purpose

This is the umbrella repo's non-sensitive bridge record for the first governed Threads scam-like content pilot in:

```text
../meta-threads-scam-content-research-2026
```

It records the strategic and governance relationship between the broader Meta scam-risk research program and the active Threads child repo.

It is not the filled controlled launch record. The filled controlled launch record may contain sensitive source, storage, access, retention, redaction, or investigative details and must remain in the approved controlled location outside git unless explicitly sanitized and approved for commit.

## Bridge Identity

| Field | Value |
|---|---|
| Bridge ID | `BRIDGE-THREADS-PILOT-V1-2026-04-23` |
| Date opened | `2026-04-23` |
| Umbrella repo | `meta-scam-ad-research-2026` |
| Child execution repo | `meta-threads-scam-content-research-2026` |
| Child repo path | `../meta-threads-scam-content-research-2026` |
| Dataset or batch ID | `threads_pilot_v1_2026-05` |
| Source candidate ID | `SRC-REAL-PILOT-APPROVED-2026-04-23` |
| Authorization ID | `AUTH-THREADS-PILOT-V1-2026-04-23` |
| Work order ID | `PWO-THREADS-PILOT-V1-2026-05` |
| Current umbrella status | `go_with_limits_item_1_preflight_passed_ready_for_manual_rehearsal` |
| Current child repo status | outside-git controlled launch confirmed; local workspace initialized; item-1 preflight passed with `ERROR: 0` |

## What Is Approved At The Umbrella Level

The umbrella repo accepts the Threads child repo as the active Phase 1 execution surface.

Approved strategic posture:

- Threads-first Phase 1 pilot, not all-Meta production detection.
- Manual or stakeholder-provided examples only.
- 50 pilot items maximum.
- First 10-15 item checkpoint before completing the 50-item pilot.
- Text, selected replies/comments, OCR, visible link/redirection, and redacted screenshot-reference evidence only where approved.
- Human-review-oriented research labels and risk triage.
- Aggregate, non-sensitive reporting in git.

Not approved:

- scraping
- crawling
- browser automation
- bulk export
- redirect-chain expansion
- landing-page capture
- profile or account graph review
- production scoring
- public accusation or legal fraud determination
- raw evidence storage in git

## Non-Sensitive Approved Field Summary

The detailed field contract lives in the Threads child repo. The umbrella-level summary is:

| Field or evidence type | Umbrella bridge status | Notes |
|---|---|---|
| `post_text` | approved with redaction | Store only approved visible text in local child-repo workflow. |
| `reply_texts` | approved with redaction | Selected relevant replies/comments only. |
| `ocr_text` | approved with limits | Risk-relevant OCR after privacy review. |
| screenshot references | approved with limits | Redacted references only; raw screenshots outside git. |
| `external_links` | approved with limits | Normalized or redacted visible-link references only; no crawling. |
| contact handles | approved with redaction | Category or redacted handle only. |
| visible redirects | approved | Platform/category labels allowed. |
| source URLs | approved with limits | Redacted reference only in repo-visible files. |
| raw screenshots | not approved for git | Store outside git only if approved. |
| landing-page snapshots | not approved | No capture or crawling in this pilot. |
| profile/account context | not approved | Item-level evidence only. |

## Controlled Details That Must Stay Outside Git

The following must be completed in the approved controlled location before item 1, but should not be written into this repo if sensitive:

- outside-git controlled workspace review and approval
- exact source or exact source category
- exact raw evidence storage location
- exact access list for raw evidence
- exact access list for redacted or derived evidence
- retention or deletion rule
- redaction limits
- screenshot policy
- OCR policy
- source URL and visible-link policy
- handle/contact-info policy
- permitted fields
- forbidden fields and contexts
- collector, annotator, reviewer, adjudicator, and research engineer IDs where sensitive
- unresolved uncertainties, marked blocking or non-blocking
- final controlled launch status: `ready_for_rehearsal` or `ready_for_first_10_15_items`

## Required Confirmation Before Item 1

The project owner or governance reviewer should confirm, without revealing sensitive values in git:

```text
The outside-git controlled launch record for threads_pilot_v1_2026-05 is complete.
It includes exact source/source category, raw storage location, access list,
retention/deletion rule, redaction limits, screenshot/OCR/URL/link/handle/reply
policies, permitted and forbidden fields, role IDs, unresolved uncertainties,
and final status ready_for_rehearsal or ready_for_first_10_15_items.
```

After that confirmation, the child repo can run:

```bash
python scripts/init_pilot_workspace.py --ack-controlled-details
python scripts/check_pilot_preflight.py --before-item-1 --ack-controlled-details
```

Proceed only if item-1 preflight reports `ERROR: 0`.

## Canonical Child Repo Artifacts

| Purpose | Child repo artifact |
|---|---|
| Launch plan | `../meta-threads-scam-content-research-2026/docs/37-approved-pilot-launch-plan.md` |
| Local workspace | `../meta-threads-scam-content-research-2026/docs/39-local-pilot-workspace.md` |
| Item-1 preflight | `../meta-threads-scam-content-research-2026/docs/40-pilot-preflight-verification.md` |
| First checkpoint protocol | `../meta-threads-scam-content-research-2026/docs/38-first-pilot-checkpoint-protocol.md` |
| Data governance | `../meta-threads-scam-content-research-2026/governance/data-governance.md` |
| Launch packet | `../meta-threads-scam-content-research-2026/governance/pilot-launch/` |
| Start note | `../meta-threads-scam-content-research-2026/experiments/evaluation-notes/0009-first-10-15-real-pilot-start-note.md` |

## First 10-15 Item Gate

The first real batch is a checkpoint, not a scale-up.

Target diagnostic mix:

| Bucket | Target count |
|---|---:|
| likely scam or high-risk scam-like | 3-5 |
| likely non-scam comparator | 3-5 |
| uncertain or ambiguous | 2-3 |
| insufficient-evidence or low-context | 1-3 |

The 50-item pilot remains blocked unless the child repo checkpoint decision is:

- `continue_to_50`
- `continue_with_limits`

Any other decision pauses or stops the pilot until the relevant governance, collection, annotation, or schema issue is resolved.

## Why This Bridge Exists

This bridge prevents the umbrella repo from drifting away from the active Threads execution path.

It also preserves three boundaries:

1. Strategic ownership stays here.
2. Threads execution details stay in the child repo.
3. Sensitive controlled launch details stay outside git.

This lets future reviewers understand why the broader Meta scam-risk project narrowed to a Threads-first pilot without copying raw evidence, duplicating child-repo operating docs, or implying that a governed 10-15 item checkpoint is already a production detector.

## Current Decision

Umbrella decision:

```text
record_bridge_only_controlled_workspace_scaffold_created_pending_owner_completion
```

Meaning:

- The umbrella repo records the approved strategic relationship and launch limits.
- The child repo remains the execution source of truth.
- The outside-git controlled launch record has been confirmed as `ready_for_first_10_15_items`.
- The child repo local workspace has been initialized and item-1 preflight reports `ERROR: 0`.
- The next governed action is 1-2 manual rehearsal records, followed by the first 10-15 item checkpoint workflow if rehearsal passes.
