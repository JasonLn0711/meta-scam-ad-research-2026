# Decision 0003: Rename Repo With Project Year

## Identity

- Date: 2026-04-23
- Status: accepted
- Owner: Jason

## Decision

Rename the repository directory from:

```text
meta-scam-ad-research
```

to:

```text
meta-scam-ad-research-2026
```

## Context

The project is tied to a 2026 public-sector research opportunity. The original name was intentionally research-first and avoided over-promising a production detection system, but it did not make the project year visible in the folder name.

## Rationale

`meta-scam-ad-research-2026` keeps the original meaning while making the project/grant year explicit. This helps future file organization if later anti-fraud research projects or follow-on phases appear.

## Consequences

- Planning references should point to `/home/jnln3799/every_on_git_ubuntu/meta-scam-ad-research-2026`.
- The Git history remains intact because only the parent directory name changed.
- The project should still be framed as research, not a production detection system.

## Files To Update

- planning day note
- planning project locator
- weekly plan correction
- research repo session note
- research repo decision index
