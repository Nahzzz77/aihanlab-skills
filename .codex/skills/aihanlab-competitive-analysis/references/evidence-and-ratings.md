# Evidence and Ratings

Read this file before labeling claims, scoring capabilities, or building a comparison matrix.

## Keep two axes separate

Evidence status answers: **How do we know?**

Capability quality answers: **How well does it solve the relevant user job?**

Never combine them into one score. A capability can be `Strong` with `Reported` evidence, or `Unverified` despite an `Indicated` entry point.

## Evidence status contract

| Status | Use when | Allowed phrasing | Do not claim |
|---|---|---|---|
| `Verified` | Directly observed end to end, or confirmed by an authoritative primary source for that exact fact | “Supports”, “shows”, “provides” | Hidden quality, reliability, or scale not tested |
| `Indicated` | An entry point, control, label, or partial step is visible but depth was not tested | “Appears to”, “has an entry point for” | A complete or effective workflow |
| `Reported` | A named user, reviewer, study, or credible third party states it | “Users report”, followed by provenance and caveat | Representative prevalence from a small or biased sample |
| `Inferred` | Multiple observations support an analyst conclusion | “This suggests”, followed by reasoning | Direct product fact |
| `Not observed` | The available evidence does not show the capability or fact | “Not observed in the available evidence” | “Absent”, “does not support”, or “cannot do” |

Marketing pages are authoritative evidence of positioning and published claims, not automatic proof of product quality. Release notes verify that a vendor announced a change; hands-on evidence is still needed to judge depth.

## Capability quality contract

| Rating | Meaning |
|---|---|
| `Strong` | Solves the user job reliably with meaningful depth, control, or advantage. |
| `Adequate` | Solves the common case with acceptable usability; important limits remain. |
| `Weak` | Exists but creates material friction, gaps, or failure risk. |
| `Absent` | Sufficient evidence shows the capability is not offered in the evaluated scope. |
| `Unverified` | Evidence is insufficient to judge quality. Use this instead of guessing. |

Do not infer `Strong` from marketing language, `Absent` from silence, or `Weak` from a single complaint. If the evidence supports presence but not quality, use `Unverified` and explain what must be tested.

## Source hierarchy

Prefer the strongest available evidence for each claim:

1. Direct hands-on observation or user-supplied authorized artifact
2. Official product documentation, pricing, policies, release notes, and public filings
3. Reproducible demos or vendor-authored tutorials
4. Credible independent reporting, research, or structured benchmarks
5. Attributed reviews, community posts, and social content
6. Analyst inference

Lower-ranked sources can reveal important questions but should not silently override direct evidence. Record conflicts instead of averaging them away.

## Claim ledger

Maintain these fields for material claims:

| Field | Required content |
|---|---|
| Claim | One falsifiable statement |
| Evidence status | One of the five exact labels |
| Source or artifact | URL, document title, recording segment, screenshot, or observation note |
| Date | Publication date when known and research date |
| Scope | Product tier, market, device, account type, or tested flow |
| Confidence note | Ambiguity, missing step, sample limitation, or conflict |

## Weighted comparison

Use weights only to clarify a product decision, never to manufacture precision.

1. Choose 5–10 decision-relevant dimensions.
2. Assign weights totaling 100% based on target-user importance and strategic relevance.
3. Map quality ratings to calculation values only for the total: `Strong=3`, `Adequate=2`, `Weak=1`, `Absent=0`. Exclude `Unverified` from the numeric total.
4. Show the original word rating, evidence status, rationale, and weight in the visible table.
5. Report coverage: the percentage of total weight with a verified quality rating.
6. If uncovered weight exceeds 25%, label the total directional and prioritize validation.
7. If plausible weight changes reverse the conclusion, state the sensitivity instead of naming a definitive winner.

Suggested matrix columns:

| Dimension | Why it matters | Weight | Competitor rating | Evidence | Our rating | Evidence | Implication |
|---|---|---:|---|---|---|---|---|

## Common mistakes

| Mistake | Correction |
|---|---|
| “There is a share button, so collaboration is strong.” | Label the entry point `Indicated`; test permissions, co-editing, notifications, and recovery before rating quality. |
| “The website says enterprise-ready, so security is verified.” | Treat enterprise-ready as a positioning claim; verify named controls and scope separately. |
| “Three reviews dislike latency, so latency is weak.” | Use `Reported`, note the sample, and keep quality `Unverified` until direct or representative evidence exists. |
| “Nothing in the recording shows reminders, so reminders are absent.” | Use `Not observed`; test the relevant lifecycle before `Absent`. |
