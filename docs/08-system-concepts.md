# System Concepts

## Broad Concept

The broad architecture maps all possible evidence layers. It is intentionally larger than the budget-fit prototype so stakeholders can see what is being deferred.

```mermaid
flowchart LR
  A[Meta-related surfaces] --> B[Lawful evidence intake]
  B --> C[Creative media]
  B --> D[Text and OCR]
  B --> E[Metadata]
  B --> F[Landing pages and redirects]
  B --> G[Interactions]
  C --> H[Image/video analysis]
  D --> I[Text risk analysis]
  E --> J[Metadata risk analysis]
  F --> K[Destination risk analysis]
  G --> L[Interaction pattern analysis]
  H --> M[Hybrid risk scoring]
  I --> M
  J --> M
  K --> M
  L --> M
  M --> N[Evidence packet]
  N --> O[Human review]
  O --> P[Decision memo and model refinement]
```

## Narrowed Architecture

The budget-fit architecture removes long video, Stories, broad comment collection, graph analysis, and definitive deepfake detection from the first prototype.

```mermaid
flowchart TD
  A[Approved sample intake] --> B[Evidence normalization]
  B --> C[Caption and post text]
  B --> D[Images and carousel cards]
  B --> E[Landing page evidence if authorized]
  B --> F[Limited metadata if available]
  D --> G[OCR]
  C --> H[Text/risk-pattern baseline]
  G --> H
  D --> I[Image-risk baseline]
  E --> J[Destination-risk baseline]
  F --> K[Metadata-risk baseline]
  H --> L[Hybrid triage score]
  I --> L
  J --> L
  K --> L
  L --> M[High / medium / low queue]
  M --> N[Reviewer evidence packet]
  N --> O[Labels, reason codes, missing evidence]
```

## Recommended Prototype Architecture

Inputs:

- `case_id`
- image or carousel image-set
- caption/post text
- OCR text
- landing URL and landing-page text/screenshot if authorized
- limited metadata fields if available

Processing:

- text normalization
- OCR extraction
- rule and keyword/risk-pattern baseline
- text model baseline
- image embedding/classifier baseline
- optional VLM-assisted reason generation on sample or high-risk queue
- hybrid score aggregation
- evidence packet generation

Outputs:

- risk level: high/medium/low
- primary label suggestion
- reason codes
- evidence completeness score
- reviewer note and final label

## Evidence Flow

```mermaid
sequenceDiagram
  participant S as Source / Stakeholder
  participant I as Intake Log
  participant N as Normalizer
  participant P as Pipelines
  participant E as Evidence Packet
  participant R as Reviewer
  participant D as Decision Log

  S->>I: Provide approved sample or reference
  I->>N: Record source, method, timestamp, permissions
  N->>P: Send normalized text, image, OCR, metadata, landing evidence
  P->>E: Produce score, reason codes, evidence completeness
  E->>R: Present review packet
  R->>D: Record label, triage, notes, missing evidence
  D->>P: Feed error analysis and next experiment decision
```

## Review Flow

```mermaid
flowchart LR
  A[Hybrid score] --> B{Risk queue}
  B -->|High| C[Priority human review]
  B -->|Medium| D[Sampled or capacity-based review]
  B -->|Low| E[QA and drift sample]
  C --> F[Confirm / reject / escalate]
  D --> F
  E --> G[Periodic false-negative audit]
  F --> H[Evidence and decision memo]
```

## Design Choices

- Keep the prototype evidence-centric. A reviewer should understand why a case was flagged.
- Keep ingestion lawful and auditable.
- Treat VLM/LLM outputs as assistive evidence summaries, not final truth.
- Keep landing-page analysis gated by legal approval and security precautions.
- Use high-risk precision as the first optimization target.

## Future Scaled Architecture

Only a future, separately funded program should consider:

- continuous ingestion
- workflow dashboard
- investigator case management
- model monitoring
- deepfake benchmark service
- domain/advertiser cluster analysis
- platform partnership/API integration
