# Decision 0005: Record Threads Controlled Launch Bridge

## Identity

- Decision ID: `DEC-0005`
- Date: `2026-04-23`
- Status: accepted
- Owner: Jason

## Decision

Add a non-sensitive umbrella governance bridge for the first governed Threads pilot:

```text
governance/threads-pilot-v1-controlled-launch-bridge.md
```

The bridge records the relationship between the umbrella Meta scam-risk research repo and the Threads child execution repo, while keeping the filled controlled launch record outside git.

## Context

The active Phase 1 execution path moved to:

```text
../meta-threads-scam-content-research-2026
```

That child repo now contains the detailed Threads-specific schema, annotation guidance, launch packet, preflight workflow, local workspace instructions, and first 10-15 item checkpoint protocol.

The umbrella repo still owns broader Meta scam-risk strategy, budget realism, scope tradeoffs, and cross-platform roadmap memory. It therefore needs a short governance bridge so future reviewers can see why the Threads pilot is allowed to proceed only under narrow conditions, without copying sensitive child-repo or outside-git details into the umbrella repo.

## Options Considered

| Option | Pros | Cons | Decision |
|---|---|---|---|
| Store the filled controlled launch record in the umbrella repo | Easy to find in one place | Could expose sensitive source, storage, access, retention, redaction, or investigative details; violates data-minimization posture | Rejected |
| Store no umbrella record | Avoids duplication | Umbrella repo would not reflect the current gated Threads launch posture | Rejected |
| Store a non-sensitive governance bridge only | Keeps strategy traceable while preserving child-repo and outside-git boundaries | Requires users to follow links to the child repo for execution details | Accepted |

## Rationale

The bridge is needed because the umbrella repo is the strategic memory for the broader Meta scam-risk project. The Threads child repo is the execution surface, but the umbrella repo should still record:

- why Threads is the active Phase 1 path
- which pilot limits matter strategically
- what is not approved
- why the first 10-15 item checkpoint comes before 50 items
- why sensitive controlled launch details remain outside git

This prevents future scope creep, especially accidental moves toward scraping, production scoring, broad Meta collection, or storing raw evidence in git.

## Consequences

- The umbrella repo now has a non-sensitive bridge record for the Threads pilot.
- The filled controlled launch record remains outside git.
- The Threads child repo remains the source of truth for item-level workflow, schema, annotation, preflight, and checkpoint details.
- No real Threads item should be collected until the child repo item-1 preflight passes with `ERROR: 0` after outside-git controlled launch confirmation.

## Files To Update

- [x] `governance/threads-pilot-v1-controlled-launch-bridge.md`
- [x] `governance/data-governance.md`
- [x] `decision-log/README.md`
