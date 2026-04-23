# Data Governance

## Default Policy

Authorization-first. No automated Meta data collection without explicit written authorization, approved API access, or legal/stakeholder approval recorded here.

## Current Data Status

- Real stakeholder data: not yet received.
- Public/manual examples: not yet approved for collection.
- Synthetic examples: allowed for pipeline dry runs.
- Automated Meta collection: not approved.
- Landing-page capture: not approved.
- Metadata collection: not approved unless stakeholder-provided or API-authorized.

## Data Access Decision Log

| Date | Decision | Owner | Notes |
|---|---|---|---|
| 2026-04-23 | Initial posture set to authorization-first | Project starter | No automated Meta collection approved |

## Approved Uses

Currently approved:

- writing research docs
- designing schemas and annotation guidelines
- creating synthetic toy examples
- reviewing public policy/research sources

Not approved:

- scraping Meta surfaces
- collecting comments/replies at scale
- landing-page crawling
- storing raw personal data
- using real case screenshots in public docs

## Evidence Handling Rules

- Preserve source, timestamp, capture method, permission status, and reviewer notes.
- Redact personal data unless necessary and approved.
- Separate raw evidence from derived features.
- Do not share raw evidence outside approved channels.
- Keep local scratch material under `.local/`.

## Future Approval Checklist

Before adding real data:

- data owner identified
- legal/privacy review complete
- allowed fields listed
- retention period defined
- redaction rules defined
- permitted experiments listed
- publication/sharing restrictions listed
