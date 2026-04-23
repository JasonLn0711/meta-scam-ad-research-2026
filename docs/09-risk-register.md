# Risk Register

| Risk ID | Category | Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|---|---|
| R01 | Data | No lawful access to enough real examples | Medium | High | Start authorization-first; use stakeholder examples, manual samples, synthetic only for pipeline tests |
| R02 | Platform | Meta API / Ad Library access is limited or unsuitable | High | High | Treat API access as open question; do not make it core dependency |
| R03 | Legal/ethical | Unauthorized automated collection violates terms or creates privacy risk | Medium | High | Record data decisions; no automation without written approval |
| R04 | Annotation | Reviewers disagree on scam vs aggressive marketing | High | Medium | Use reason codes, uncertainty labels, adjudication notes |
| R05 | False positives | Legitimate finance, medical, celebrity, or political ads are flagged | High | High | Use hard negatives and human review |
| R06 | False negatives | Sophisticated scams hide key evidence off-platform | High | High | Include landing-page/destination evidence where lawful |
| R07 | Deepfake overclaim | Project implies it can reliably detect deepfakes | Medium | High | Use "risk indicator" language only; no definitive claims |
| R08 | Scope creep | Stakeholders expect all Meta surfaces and modalities | High | High | Use scope matrix and budget-fit memo in every meeting |
| R09 | Compute/API cost | VLM or LLM scoring becomes too expensive | Medium | Medium | Use sampled VLM scoring and cheap baselines |
| R10 | Security | Landing pages may be malicious | Medium | High | Use isolated capture environment only after approval |
| R11 | Drift | Scam tactics shift after pilot data | High | Medium | Evaluate drift sensitivity and update taxonomy |
| R12 | Evidence quality | Screenshots lack source, timestamp, or chain of custody | Medium | High | Enforce minimum evidence fields |
| R13 | Procurement | Proposal wording over-promises system capability | Medium | High | Maintain explicit non-promises in charter and decision memo |
| R14 | Reviewer burden | Prototype produces too many medium-risk cases | Medium | Medium | Optimize high-risk precision and evidence completeness |
| R15 | Public sensitivity | Cases may involve public figures or political content | Medium | High | Add special annotation handling and legal review |

## Highest Priority Mitigations

1. Authorization-first data strategy.
2. Clear non-goals and budget-fit scope.
3. Human review and uncertainty labels.
4. Evidence packet design before model sophistication.
5. Explicit deferral of full video, Stories, graph, and definitive deepfake detection.

## Risk Review Cadence

- Review R01-R04 before any data collection.
- Review R05-R08 before stakeholder demo or proposal language.
- Review R09-R12 before prototype experiments.
- Review R13-R15 before external delivery.
