# Output Templates

Choose the smallest artifact that answers the user's decision. Default to the full brief when the user does not specify a format.

## Default competitive brief

```markdown
# [Competitor or feature] Competitive Brief

**Decision:** [Decision this analysis informs]
**Scope:** [Products, segment, geography, tier, workflow]
**Evidence base:** [Hands-on, official, reported, inferred]
**Research date:** [YYYY-MM-DD]

## 1. Executive verdict
[Competitor's center of gravity, why it matters, and the decision implication in 3–6 sentences.]

## 2. Evidence and confidence boundary
| Material claim | Status | Source or artifact | Limitation |

## 3. Competitor overview
| Target user | Job to be done | Category claim | Promised outcome | Proof | Business model |

## 4. Real user journey
| Stage | User goal | Observed experience | Evidence | Friction or advantage |

## 5. Weighted capability matrix
| Dimension | Why it matters | Weight | Competitor quality | Evidence | Our quality | Evidence | Implication |

Coverage: [percentage of weighted dimensions with quality evidence]
Sensitivity: [which uncertain weights or ratings could change the conclusion]

## 6. Positioning
[Target user, differentiator, promised outcome, proof, switching logic, vulnerable claim.]

## 7. Strengths and weaknesses
[Only evidence-supported strengths and weaknesses; keep unknowns separate.]

## 8. Opportunities and threats
[Opportunity spaces, direct threats, substitutes, and plausible competitor responses.]

## 9. Product decisions
- Match: [table stakes and why]
- Differentiate: [1–3 bets and why]
- Deprioritize: [work that does not improve the decision]
- Validate: [highest-value unknowns, method, and success signal]

## 10. Nightmare scenario and monitoring
[How the competitor could win, leading indicators, and review triggers.]

## 11. Sources
[Public links or authorized artifact descriptions with dates.]
```

## Executive one-pager

Use for leadership review or a short Feishu-ready document:

1. Decision and executive verdict
2. Three verified advantages
3. Three material unknowns
4. Weighted comparison summary
5. Match / differentiate / deprioritize / validate
6. Main threat and next checkpoint
7. Sources and research date

## Battlecard

Use for sales, partnerships, or customer-facing competition:

| Field | Content |
|---|---|
| Best-fit customer | Evidence-supported segment |
| Competitor promise | Their public positioning, attributed |
| Their advantages | Verified or clearly labeled evidence |
| Their weak points | Evidence-supported; never use unknowns as attacks |
| Our differentiator | Specific outcome and proof |
| Discovery questions | Questions that reveal fit, switching cost, or risk |
| Objection response | Accurate, non-defamatory response with caveats |
| Do not claim | Unverified, outdated, confidential, or misleading statements |

## Feature-area teardown

Use when the decision concerns one workflow rather than the full product:

1. User job and success condition
2. Entry point and prerequisites
3. Step-by-step observed journey
4. Recovery, edge cases, accessibility, and trust
5. Weighted comparison of workflow quality
6. Reusable pattern versus product-specific implementation
7. Build, copy, improve, reject, and validate decisions

## Writing rules

- Put verdicts before inventories.
- Use tables for exact comparisons, not for paragraphs that read better as prose.
- Give every material rating a reason and evidence status.
- Keep `Not observed` in an explicit unknowns section.
- Tie each recommendation to a target user, decision, and evidence.
- Prefer prioritized bets over long feature wish lists.
- Distinguish a parity requirement from a differentiator.
- Mark directional totals when evidence coverage is low.

## Final quality checklist

- [ ] The opening states the competitor's true center of gravity.
- [ ] Evidence status and capability quality are separate.
- [ ] A visible control is not treated as a complete capability.
- [ ] The journey includes continued use and recovery where observable.
- [ ] Dimensions and weights match the selected industry and decision.
- [ ] Unknowns remain `Not observed` or `Unverified`.
- [ ] Recommendations include match, differentiate, deprioritize, and validate.
- [ ] Time-sensitive claims include dates and sources.
- [ ] Private, copyrighted, or access-controlled material is handled safely.
