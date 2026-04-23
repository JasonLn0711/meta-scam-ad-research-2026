# Scope Map

## Broad Exploration Map

The candidate space includes paid ads, ad-like posts, scam-like organic lures, user interactions, and off-platform destinations. The project should inspect this broad map first, then narrow based on evidence value and feasibility.

| Layer | Candidate evidence | Examples | Main risk |
|---|---|---|---|
| Creative | image, caption, video, carousel | fake celebrity endorsement, investment promise, fake health product | multimodal ambiguity |
| Text lure | caption, post text, profile bio, CTA | "join LINE group", "limited slots", "guaranteed return" | benign marketing overlap |
| Interaction | comments, replies, engagement bait | fake testimonials, bot-like replies, induced DMs | data access and privacy |
| Metadata | page/profile/post/ad fields | repeated domains, page age, advertiser name, region | incomplete availability |
| Destination | landing page, redirects, forms | fake payment page, survey trap, cloaked content | legal/platform and dynamic capture |
| Manipulation | deepfake, AI generated, impersonation | altered public-figure voice/image | detection uncertainty |

## Prioritization Matrix

| Surface / modality | Investigative value | Technical feasibility | Data acquisition difficulty | Annotation difficulty | Model/system complexity | Compute cost | FP/FN challenge | Phase | Budget realism |
|---|---|---|---|---|---|---|---|---|---|
| Static images | High | High | Medium | Medium | Low-medium | Low-medium | Scam visuals resemble legitimate ads | Phase 1 | Realistic |
| Image + caption posts/ads | Very high | High | Medium | Medium | Medium | Medium | Context changes meaning | Phase 1 | Best fit |
| Text-only lure / redirect content | High | High | Low-medium | Low-medium | Low | Low | Marketing vs deception boundary | Phase 1 | Best fit |
| OCR from images | High | High | Medium | Medium | Medium | Low-medium | OCR errors, stylized text | Phase 1 | Best fit |
| Carousel posts | Medium-high | Medium | Medium-high | Medium | Medium | Medium | Weak signal in only one card | Phase 1 as image-set variant | Realistic if bounded |
| Landing / redirected pages | Very high | Medium | High | Medium | Medium | Medium | Cloaking, time variance, legal risk | Phase 1 if authorized | High value but gated |
| Profile/post metadata | High | Medium | High | Medium | Low-medium | Low | missing fields, weak proxies | Phase 1 limited | Realistic if provided |
| Short video / Reels | High | Medium | High | High | Medium-high | Medium-high | keyframe miss, ASR/OCR errors | Phase 2 | Selective only |
| Comments / replies / engagement bait | Medium-high | Medium-low | High | High | Medium-high | Medium | sarcasm, bots, privacy | Phase 2 limited | Only if data is provided |
| Longer video | Medium | Low | High | High | High | High | temporal reasoning, high review cost | Defer | Not budget-fit |
| Stories | Medium | Low | Very high | High | High | Medium-high | ephemeral, hard to capture lawfully | Defer | Not budget-fit |
| Deepfake indicators | High for specific cases | Low-medium | High | Very high | High | High | false certainty, evasion | Phase 2 as risk flag | Do not promise definitive detection |
| Threads-wide content | Unknown-medium | Low-medium | High | Medium-high | Medium | Medium | API/data access unclear | Defer unless clarified | Not first cut |

## Recommended First-Cut Focus Areas

Phase 1 should include:

- Static image creatives.
- Image + caption combinations.
- OCR text from images and carousel images.
- Text-only lure / redirect language.
- Landing-page evidence if lawfully provided or approved.
- Limited metadata fields if stakeholder-provided or API-authorized.

Phase 2 should test:

- Short-video keyframe + ASR + OCR pipeline.
- Comment/reply pattern sampling where authorized.
- Deepfake or AI-generated manipulation indicators as risk explanations, not final truth.

Deferred:

- Stories.
- Long-form video.
- Full Threads collection.
- Full graph/profile network analysis.
- Production enforcement pipeline.

## Why This First Cut

The recommended first cut captures the highest expected ROI: image, text, OCR, and destination evidence are common in scam ads, comparatively cheap to process, easier to explain to investigators, and more realistic under NTD 1.8M. Video, Stories, comments, and deepfake detection should not be ignored, but they should be used as exploratory expansion only after the lawful data path and baseline value are proven.
