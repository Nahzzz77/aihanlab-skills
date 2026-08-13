# AiHanLab Competitive Analysis Skill Design

## Goal

Create a reusable, industry-adaptive competitive analysis Skill named `aihanlab-competitive-analysis`. It should analyze AI products, apps, mini programs, SaaS, content platforms, marketplaces, hardware, and other product categories without hard-coding the travel example.

The Skill must turn incomplete inputs such as URLs, screenshots, recordings, product descriptions, or local files into an evidence-bounded competitive brief that supports product strategy, positioning, feature prioritization, and MVP decisions.

## Product position

The Skill is not a generic feature checklist and is not a one-off travel analysis template. Its core promise is:

> Inspect what the competitor actually enables users to do, distinguish proof from inference, adapt the comparison dimensions to the industry, and end with decisions the user's product team can act on.

## Trigger scope

Use the Skill when the user asks to:

- analyze, compare, review, or tear down one or more competitors;
- inspect a competing app, mini program, website, SaaS product, platform, or device;
- compare a specific feature area across products;
- identify parity requirements, differentiation opportunities, threats, or MVP priorities;
- turn screenshots, recordings, links, or product notes into a competitive brief;
- create a battlecard, executive summary, positioning comparison, or monitoring plan.

Do not trigger it for:

- a pure UX audit with no competitive or strategic question;
- general market research with no product comparison;
- implementation work that only happens to mention a competitor;
- copying a competitor's protected assets or bypassing access controls.

## Core workflow

1. **Frame the decision.** Identify the competitor, focus, user product, target user, and decision to inform. Infer low-risk context from supplied material instead of blocking on every missing field.
2. **Build the evidence set.** Prefer direct product experience, official pages, release notes, pricing, policies, reviews, community discussion, job postings, and credible reporting. Record the research date.
3. **Inspect the real journey.** Reconstruct entry, setup, core task, result, edit/confirm, continued use, collaboration, monetization, and failure/recovery where observable.
4. **Grade every claim.** Use `Verified`, `Indicated`, `Reported`, `Inferred`, or `Not observed`. Never convert a visible button into a proven capability.
5. **Select industry dimensions.** Start from buyer or user tasks, then load only the relevant industry overlay. Examples include AI quality and control, SaaS administration, marketplace liquidity, content discovery, travel personalization, or hardware ecosystem lock-in.
6. **Compare capability quality.** Rate capabilities as `Strong`, `Adequate`, `Weak`, `Absent`, or `Unverified`. Include why each capability matters; do not count features equally.
7. **Analyze positioning.** Compare target user, category claim, differentiator, promised outcome, proof, and vulnerable claims.
8. **Synthesize strategy.** State parity requirements, differentiation bets, deprioritized work, threats, nightmare scenario, validation questions, and monitoring triggers.
9. **Deliver the requested artifact.** Use concise prose plus tables for genuine comparisons. Mark assumptions and time-sensitive findings.

## Evidence contract

Every material claim must be traceable to one of these statuses:

| Status | Meaning | Allowed language |
|---|---|---|
| Verified | Directly observed in the product or an authoritative primary source | “Supports”, “shows”, “provides” |
| Indicated | An entry point or control is visible but depth was not tested | “Appears to”, “has an entry point for” |
| Reported | A user, reviewer, or credible third party states it | “Users report”, with source and caveat |
| Inferred | Analyst conclusion from multiple observations | “This suggests”, with reasoning |
| Not observed | Not present in the available evidence | “Not observed”, never “definitely absent” |

Marketing claims must not be treated as product proof. Reviews must not be treated as representative without noting sample limits. Time-sensitive claims require a date.

## Industry adaptation

The Skill uses a universal core and an optional overlay. The universal core always examines:

- target user and job to be done;
- acquisition and activation;
- core workflow and time to value;
- output quality and user control;
- continued-use loop and retention mechanism;
- collaboration, integrations, pricing, trust, and switching costs;
- strengths, weaknesses, opportunities, threats, and strategic implications.

The overlay adds only relevant dimensions. For example:

- **AI products:** grounding, controllability, transparency, correction, latency, cost, safety.
- **Travel:** content freshness, preference matching, itinerary feasibility, maps, disruption handling.
- **SaaS:** permissions, administration, reporting, integrations, implementation, security.
- **Content platforms:** supply, discovery, ranking, creator incentives, moderation, community loops.
- **Marketplaces:** supply density, demand quality, liquidity, trust, fulfillment, take rate.
- **Consumer apps:** onboarding, habit loop, notifications, sharing, subscription, privacy.

Unknown categories should derive dimensions from user tasks and switching criteria rather than force-fit an existing overlay.

## Output contract

Default brief sections:

1. Decision and scope
2. Executive verdict
3. Evidence and confidence boundary
4. Competitor overview
5. Real user journey
6. Weighted capability matrix
7. Positioning analysis
8. Strengths and weaknesses
9. Opportunities and threats
10. Strategic implications: build, match, differentiate, deprioritize
11. Validation gaps and monitoring triggers
12. Sources and research date

The executive verdict must lead with the competitor's true center of gravity, not a list of features. Strategic implications must be concise, prioritized, and tied back to the user's decision.

## Safety and privacy boundaries

- Analyze public or user-authorized material only.
- Do not bypass login, paywalls, rate limits, anti-bot systems, permissions, or technical protection.
- Do not publish private recordings, internal roadmaps, credentials, account details, personal file paths, or confidential product plans.
- Summarize protected content; do not republish substantial copyrighted text, images, recordings, or datasets.
- Treat social posts and reviews as evidence with provenance, date, sample limitations, and potential commercial bias.
- Phrase “avoid” or “warning” findings as aggregated, attributed opinions unless independently verified facts support them.

## Repository structure

```text
.codex/skills/aihanlab-competitive-analysis/
├── SKILL.md
├── LICENSE
├── NOTICE
├── agents/
│   └── openai.yaml
└── references/
    ├── evidence-and-ratings.md
    ├── industry-overlays.md
    └── output-templates.md
```

The repository root `README.md` becomes an index for multiple AiHanLab Skill categories. It will add the new Skill, installation instructions, example triggers, repository structure, and per-Skill licensing guidance.

## License and attribution

The design is a substantial, industry-adaptive derivative inspired by Anthropic's `competitive-brief` Skill from `anthropics/knowledge-work-plugins`.

The upstream repository is licensed under Apache License 2.0. The new Skill directory will include:

- a copy of Apache License 2.0;
- a `NOTICE` file naming the upstream source and stating that AiHanLab changed the name, structure, evidence model, industry adaptation, safety rules, and output contract;
- no claim that Anthropic endorses or maintains this Skill.

The license applies to this Skill directory only. It does not silently relicense unrelated Skills in the repository.

## Validation

Validate before publishing:

1. Run `quick_validate.py` for structure and frontmatter.
2. Confirm `agents/openai.yaml` matches `SKILL.md`.
3. Run a baseline comparison prompt without the Skill and record omissions.
4. Run at least three forward tests with the Skill:
   - a travel mini program from a recording;
   - an AI SaaS product from official pages and reviews;
   - a content platform feature comparison.
5. Check each result for evidence labels, industry-adapted dimensions, honest uncertainty, and actionable implications.
6. Scan the staged files for private paths, recordings, credentials, internal plans, and unlicensed copied content.

## Publishing strategy

- Target repository: `Nahzzz77/aihanlab-skills`.
- Repository visibility: public.
- Work on branch `agent/add-competitive-analysis-skill`.
- Commit only the new Skill directory, the updated root README, and the design/plan documents required by the authoring workflow.
- Push the branch and open a draft pull request for final review before merge.
