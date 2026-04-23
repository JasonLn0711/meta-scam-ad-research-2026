# Research Questions

## Broad Questions

1. Which Meta-related content surfaces produce the most actionable scam evidence for public-sector investigation?
2. Which scam patterns are visible in the creative itself, and which require landing-page or metadata evidence?
3. How much incremental value is added by OCR, image analysis, landing-page capture, metadata, and video processing?
4. Can a hybrid triage pipeline reduce human review burden while preserving explainable evidence?
5. Which parts of the problem are infeasible without Meta cooperation, stakeholder-provided data, or a larger budget?

## Must Answer Now

These questions must be answered before committing to a prototype:

| Question | Why it matters | Evidence needed |
|---|---|---|
| What data can be lawfully used? | Determines every experiment boundary | Legal review, stakeholder data inventory, API permissions |
| What are the highest-priority scam families? | Prevents vague generic detection | Stakeholder interviews, 165/CIB patterns, public scam reports |
| Which surfaces are common enough to matter? | Avoids building for rare cases | Small sample audit, stakeholder examples |
| What labels can annotators apply reliably? | Determines evaluation quality | Annotation pilot and disagreement analysis |
| What is the operational decision output? | Aligns model output with reviewer action | Triage workflow: high/medium/low, evidence packet, escalation |

## Narrowed Research Questions

1. Does image + caption + OCR outperform text-only screening on high-risk scam families?
2. Does landing-page evidence materially improve precision for investment, fake e-commerce, healthcare, phishing, and subscription-trap scams?
3. Can low-cost rules and keyword/risk patterns provide a strong baseline before adding VLM/LLM scoring?
4. Which explainable reason categories are most useful to human reviewers?
5. What evidence fields are necessary for a reviewer to confirm, reject, or escalate a case?
6. What subset of modalities gives the best value under NTD 1.8M?

## Nice To Explore Later

- Full Reels/short-video temporal modeling.
- Longer video analysis.
- Deepfake detector benchmarking across public-figure scam creatives.
- Comment/reply bot-pattern detection.
- Cross-page/domain reuse clustering.
- Threads-specific scam-lure patterns.
- Live monitoring or production alerting.

## Decision-Oriented Questions

The research should not end with "model A has higher F1." It should answer:

- What should a reviewer inspect first?
- Which evidence is strong enough for escalation?
- Which signals are cheap but noisy?
- Which signals are expensive but decisive?
- Which data sources require negotiation before any realistic system can exist?
- Which promises should be rejected in a public-sector procurement proposal?
