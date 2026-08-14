# AiHanLab Competitive Analysis Skill Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add and publish a reusable, evidence-based, cross-industry competitive-analysis Skill named `aihanlab-competitive-analysis`.

**Architecture:** Keep the main `SKILL.md` concise and procedural. Put evidence rules, industry-specific dimensions, and output contracts in three one-level reference files that are loaded only when relevant. Package Apache-2.0 attribution inside this Skill directory so unrelated Skills keep their existing licensing.

**Tech Stack:** Markdown, YAML, Codex Agent Skills, Python validation scripts from the system `skill-creator`, Git, GitHub CLI.

## Global Constraints

- Use the exact Skill name and folder `aihanlab-competitive-analysis`.
- Keep the Skill industry-adaptive; travel is one evaluation case, not the default domain.
- Analyze only public or user-authorized material and never bypass access controls.
- Label material claims as `Verified`, `Indicated`, `Reported`, `Inferred`, or `Not observed`.
- Rate capability quality separately as `Strong`, `Adequate`, `Weak`, `Absent`, or `Unverified`.
- Preserve Apache License 2.0 and upstream attribution without implying Anthropic endorsement.
- Do not publish recordings, local paths, credentials, account details, internal roadmaps, or confidential product plans.
- Work on `agent/add-competitive-analysis-skill` and target `main` through a draft pull request.

---

### Task 1: Establish the no-Skill baseline

**Files:**
- Create: `docs/superpowers/tests/2026-08-13-competitive-analysis-evaluations.md`

**Interfaces:**
- Consumes: The design contract in `docs/superpowers/specs/2026-08-13-aihanlab-competitive-analysis-design.md`.
- Produces: A RED-phase record of omissions that the new Skill must correct, plus three reusable forward-test rubrics.

- [ ] **Step 1: Run a fresh-context baseline**

Give an agent a realistic competitor-analysis request without access to the new Skill. Require it to propose the analysis approach and report structure from a short product recording plus an incomplete comparison brief.

- [ ] **Step 2: Verify the baseline fails for the intended reasons**

Score the response against these exact requirements: five evidence labels, distinction between capability presence and quality, industry-adaptive dimensions, reconstructed user journey, weighted strategic implications, and safety boundaries. The RED phase passes only if at least one required behavior is missing or ambiguous.

- [ ] **Step 3: Record evidence verbatim**

Create the evaluation document with the baseline prompt, the agent's relevant wording, the failed rubric items, and three GREEN-phase scenarios: travel mini program, AI SaaS, and content-platform feature comparison.

- [ ] **Step 4: Commit the plan and baseline record**

```bash
git add docs/superpowers/plans/2026-08-13-aihanlab-competitive-analysis.md docs/superpowers/tests/2026-08-13-competitive-analysis-evaluations.md
git commit -m "test: define competitive analysis evaluations"
```

### Task 2: Scaffold and implement the Skill

**Files:**
- Create: `.codex/skills/aihanlab-competitive-analysis/SKILL.md`
- Create: `.codex/skills/aihanlab-competitive-analysis/agents/openai.yaml`
- Create: `.codex/skills/aihanlab-competitive-analysis/references/evidence-and-ratings.md`
- Create: `.codex/skills/aihanlab-competitive-analysis/references/industry-overlays.md`
- Create: `.codex/skills/aihanlab-competitive-analysis/references/output-templates.md`

**Interfaces:**
- Consumes: Baseline omissions and the approved design contract.
- Produces: A discoverable Skill whose default prompt invokes `$aihanlab-competitive-analysis` and whose references define stable analysis contracts.

- [ ] **Step 1: Initialize through the official scaffold script**

Run `init_skill.py` with `--resources references` and these interface values:

```text
display_name=AiHanLab 竞品分析
short_description=基于证据的跨行业产品竞品分析与战略建议
default_prompt=使用 $aihanlab-competitive-analysis 分析这个产品的竞品定位、真实流程、差异化机会和 MVP 建议。
```

- [ ] **Step 2: Implement the main workflow**

Write a concise imperative `SKILL.md` that frames the decision, gathers evidence, inspects the real journey, selects an industry overlay, compares weighted capability quality, analyzes positioning, and ends with build/match/differentiate/deprioritize decisions.

- [ ] **Step 3: Implement evidence and rating rules**

Define the five evidence statuses, five capability ratings, source hierarchy, claim ledger, wording contract, recency handling, and the rule that a visible control proves only an entry point until tested.

- [ ] **Step 4: Implement industry adaptation**

Define a universal comparison core plus overlays for AI products, travel, SaaS, content platforms, marketplaces, consumer apps, and hardware. For unknown categories, derive dimensions from jobs, switching criteria, and failure costs.

- [ ] **Step 5: Implement output contracts**

Provide the default competitive brief, weighted matrix, executive one-pager, battlecard, and validation checklist. Keep verdicts and decisions ahead of feature inventories.

### Task 3: Add licensing, attribution, and repository documentation

**Files:**
- Create: `.codex/skills/aihanlab-competitive-analysis/LICENSE`
- Create: `.codex/skills/aihanlab-competitive-analysis/NOTICE`
- Modify: `README.md`

**Interfaces:**
- Consumes: Apache License 2.0 and the upstream `anthropics/knowledge-work-plugins` source notice.
- Produces: A redistributable derivative with visible modification notice and a root README that indexes all Skills.

- [ ] **Step 1: Add the Apache-2.0 license text**

Place the complete Apache License 2.0 inside the new Skill directory.

- [ ] **Step 2: Add a modification notice**

Name the upstream repository and source Skill, identify AiHanLab's substantial changes, retain upstream attribution, and state that neither Anthropic nor OpenAI endorses the derivative.

- [ ] **Step 3: Rewrite the root README as a collection index**

Describe all three Skills, installation and invocation examples, directory layout, evidence/privacy boundaries, and per-Skill licensing. Do not present the repository as an official Anthropic or OpenAI project.

### Task 4: Validate RED → GREEN and package quality

**Files:**
- Modify if needed: `.codex/skills/aihanlab-competitive-analysis/**`
- Modify: `docs/superpowers/tests/2026-08-13-competitive-analysis-evaluations.md`

**Interfaces:**
- Consumes: The implemented Skill and the three evaluation prompts.
- Produces: Recorded forward-test results and a structurally valid, privacy-safe package.

- [ ] **Step 1: Run structural validation**

```bash
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py .codex/skills/aihanlab-competitive-analysis
```

Expected: validation succeeds with no frontmatter or naming errors.

- [ ] **Step 2: Run three fresh-context forward tests with the Skill**

Use the travel, AI SaaS, and content-platform scenarios from the evaluation document. Each output must use evidence labels, adapt dimensions to the category, distinguish presence from quality, state uncertainty, and end with prioritized product decisions.

- [ ] **Step 3: Refactor only observed gaps**

If a forward test misses a rubric item, update the smallest relevant instruction or reference, then rerun that scenario. Record the observed gap and correction in the evaluation document.

- [ ] **Step 4: Run content and privacy scans**

Search the staged scope for local absolute paths, recording filenames, credential patterns, private account data, and unsupported claims of endorsement. Confirm all links are public and intended.

- [ ] **Step 5: Inspect the full diff and commit**

```bash
git diff --check
git diff -- README.md .codex/skills/aihanlab-competitive-analysis docs/superpowers
git add README.md .codex/skills/aihanlab-competitive-analysis docs/superpowers
git commit -m "feat: add competitive analysis skill"
```

### Task 5: Publish for review

**Files:**
- No additional repository files expected.

**Interfaces:**
- Consumes: A verified branch containing only the approved Skill, README, attribution, and authoring records.
- Produces: A remote feature branch and draft pull request against `Nahzzz77/aihanlab-skills:main`.

- [ ] **Step 1: Normalize public commit identity**

Read the authenticated GitHub account identity. Configure a repository-local public name and GitHub noreply address, then amend any unpushed commit that exposes a local machine account.

- [ ] **Step 2: Re-run final verification**

Run the structural validator, content scans, `git diff --check`, `git status -sb`, and review the exact commit range against `main`.

- [ ] **Step 3: Push the named branch**

```bash
git push -u origin agent/add-competitive-analysis-skill
```

- [ ] **Step 4: Open a draft pull request**

Create a draft PR against `main` whose description states what changed, why, licensing/attribution, safety boundaries, and the validation performed.
