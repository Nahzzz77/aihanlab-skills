# Competitive Analysis Skill Evaluations

## Purpose

Use these evaluations to compare ordinary competitive-analysis behavior with behavior after loading `$aihanlab-competitive-analysis`. The rubric tests reusable analysis discipline rather than travel-specific conclusions.

## RED baseline

### Prompt

The fresh-context agent received a 75-second travel mini-program recording scenario with five direct observations and explicit unknowns. It was asked for an analysis approach and exact report outline that could later transfer to AI SaaS and content-platform work. It was not allowed to inspect the repository or use a custom competitive-analysis Skill.

### Useful baseline behavior

The baseline correctly treated the recording as limited interface evidence, reconstructed a journey, separated unknowns from weaknesses, proposed strategic priorities, adapted a universal workflow across industries, and included privacy safeguards.

Relevant wording:

> “I would treat the 75-second recording as interface evidence, not proof of underlying intelligence, data access, reliability, or business model.”

> “Unknowns are never converted into competitor weaknesses.”

> “Publicly accessible content is not automatically appropriate for unrestricted profiling.”

### Observed failures

| Required behavior | Baseline result | RED finding |
|---|---|---|
| Use the exact evidence contract | Used `Observed—high confidence`, `Observed—medium confidence`, `Inferred—low confidence`, and `Unknown` | Failed: it omitted the distinct `Indicated`, `Reported`, and `Not observed` evidence types and mixed evidence basis with confidence. |
| Separate capability quality from evidence status | Proposed `0 — Not evidenced` through `3 — Differentiated/advanced` plus `A–U` confidence | Partial: the separation idea was present, but the quality scale did not use the stable `Strong`, `Adequate`, `Weak`, `Absent`, `Unverified` contract. |
| Use a genuinely weighted capability matrix | Proposed a formula and a `0–3 / A–U` scorecard | Failed: no dimension weights, weighted totals, or sensitivity note were specified. |
| Adapt analysis to the industry | Mapped travel, AI SaaS, and content-platform equivalents | Passed. |
| Reconstruct the real user journey | Used `Discover → Enter trip constraints → ... → Recover from disruptions` | Passed. |
| End with prioritized strategic action | Produced P0/P1/P2 and “do not copy yet” | Passed. |
| State public-data and access boundaries | Included consent, provenance, sensitive-trait, precise-location, minors, deletion, and opt-out safeguards | Passed. |

### Baseline pattern to correct

Without a shared Skill, a capable agent invents a plausible taxonomy for each task. The result may be thoughtful but is not comparable across analyses. The Skill must make the evidence vocabulary, capability-quality vocabulary, weighting method, and output order stable while preserving industry adaptation.

## GREEN forward-test rubric

Every scenario passes only if the response:

- uses `Verified`, `Indicated`, `Reported`, `Inferred`, and `Not observed` correctly;
- uses `Strong`, `Adequate`, `Weak`, `Absent`, or `Unverified` only for capability quality;
- never turns an untested feature into `Absent` or a visible control into `Verified` depth;
- reconstructs the relevant user journey;
- selects category-specific dimensions and explains why they matter;
- shows weights for material comparison dimensions and explains low-confidence ratings;
- leads with the competitor's center of gravity;
- ends with prioritized `match`, `differentiate`, `deprioritize`, and `validate` decisions;
- records evidence limits, sources or artifact provenance, and research date;
- respects public/user-authorized access, privacy, platform terms, and copyrighted content.

## Scenario A: Travel mini program from a recording

```text
Use $aihanlab-competitive-analysis to analyze a travel mini program against an AI itinerary assistant.

Recording observations: the home screen asks for destination and dates; preference tags are visible; a day-by-day plan appears after generation; itinerary cards are visibly rearranged; a share control is visible. Pricing, reminder behavior, collaboration depth, source provenance, recommendation freshness, route feasibility, and disruption handling were not tested.

Our strategic question: which capabilities are table stakes for MVP, and where could explainable preference matching and safe public social-content signals create differentiation?
```

Expected category emphasis: preference matching, itinerary feasibility, freshness and provenance, maps or routing, in-trip use, disruption handling, and privacy around location or social signals.

## Scenario B: AI SaaS from mixed sources

```text
Use $aihanlab-competitive-analysis to compare fictional AI SaaS product ModelDesk with our team workspace.

Official page claims: multi-model chat, citations, team workspaces, SSO, and usage analytics. A hands-on trial verified chat, model switching, document upload, inline citations, and export. An SSO settings entry is visible but was not configured. Three recent reviews report slow answers on large documents; the sample is small and self-selected. Admin analytics, retention, pricing exceptions, grounding accuracy at scale, and enterprise support were not tested.

Decision: choose parity requirements and two differentiation bets for a six-week beta.
```

Expected category emphasis: grounding, controllability, correction, latency, administration, permissions, security, integrations, adoption, cost, and switching risk.

## Scenario C: Content-platform feature comparison

```text
Use $aihanlab-competitive-analysis to analyze the discovery feature of fictional content platform ClipCircle.

Hands-on observations: new users choose interests; the feed mixes followed and recommended posts; users can hide a topic; creator analytics show impressions and saves. The public creator guide describes recommendation eligibility. Community posts report that niche creators struggle with cold start, but no representative dataset is available. Ranking weights, moderation appeals, creator payouts, long-term retention, and advertiser controls were not observed.

Decision: decide what our learning community should match, reject, or differentiate before launching discovery.
```

Expected category emphasis: supply health, discovery quality, ranking controls, cold start, creator incentives, moderation, community loops, trust, and feedback signals.

## Results log

Record each forward-test result here after the Skill exists.

| Scenario | Evidence contract | Industry overlay | Weighted comparison | Strategic action | Safety | Result |
|---|---|---|---|---|---|---|
| A: Travel | Pass: all five labels used appropriately | Pass: feasibility, freshness, routing, disruption, location/social privacy | Pass: 7 rows, 100% weights, 50% coverage, sensitivity stated | Pass: match, three differentiators, deprioritize, validation, threat | Pass | Pass |
| B: AI SaaS | Pass: claims, visible SSO, reviews, and unknowns separated | Pass: grounding, latency, permissions, governance, security gates | Pass: 7 rows, 100% weights, 45% coverage, directional caveat | Pass: parity, two beta bets, defer, validate, threat | Pass | Pass |
| C: Content platform | Pass: direct, reported, inferred, and unknown evidence separated | Pass: discovery, cold start, creator feedback, moderation, trust | Pass: 7 rows, 100% weights, 70% coverage, sensitivity stated | Pass: match, reject, differentiate, deprioritize, validation | Pass | Pass |

## Additional generalization checks

- **Connected hardware:** Passed. The response adapted to pairing, battery, local/cloud boundaries, connectivity recovery, repairability, warranty, accessibility, and long-term reliability. It kept official specifications, visible controls, small-sample reviews, and missing evidence separate.
- **Services marketplace:** Passed. The response adapted to liquidity, supply density, trust operations, dispute recovery, provider economics, take rate, and repeat booking. With only 25% weighted quality coverage, it correctly withheld an overall score and prioritized a single-city validation gate.

## GREEN conclusion

Across five categories, the Skill produced the same evidence and quality vocabulary while changing the decision dimensions. The RED controls produced thoughtful work but invented incompatible taxonomies such as `[OBS]/[TEST]/[UNK]`, `Observed/Vendor-claimed/N/T`, and `[VISIBLE]/[DOC]/NR`. The Skill therefore adds repeatability and cross-report comparability rather than merely adding more analysis prose.
