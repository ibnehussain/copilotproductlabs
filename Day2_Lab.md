# Day 2 Lab — Full PRD → Azure DevOps Hierarchy

**Duration:** 45 minutes · **Format:** Individual or pairs
**Builds on:** Your Day 1 Epic
**Feeds into:** Day 4 (this PRD becomes tomorrow's estimated backlog) and Day 5 (this PRD gets reviewed and summarized)

## What You'll Need

- [ ] GitHub Copilot Chat open and signed in
- [ ] Your Day 1 ADO Epic open in another tab
- [ ] Rough notes for one feature that belongs inside that Epic (a few bullet fragments is enough)

## Learning Goal

Turn rough notes into a complete PRD, convert its user stories into testable Gherkin acceptance criteria, and build the resulting Feature → User Story hierarchy natively in ADO.

---

## Step 1 — Generate the Full PRD (15 min)

Write 3–5 rough, messy bullet notes about one feature within your Day 1 Epic — don't polish them.

**Your rough notes:**
```
[write them here]
```

Paste this prompt into Copilot Chat, with your notes at the end:

```
Act as a Senior PM. Using the structure Problem Statement / Goals & Non-Goals /
User Stories / Functional Requirements / Non-Functional Requirements / Acceptance Criteria,
turn the notes below into a full PRD for this feature, which sits inside the following Epic:
[paste your Day 1 Epic's title + description]

Notes:
[paste your rough notes from above]
```

## Step 2 — Convert User Stories to Gherkin (10 min)

Once you have the PRD, run this follow-up prompt in the same chat thread so Copilot has the PRD as context:

```
Convert the user stories above into Gherkin-format acceptance criteria (Given/When/Then).
```

## Step 3 — Stress-Test It Once (5 min)

Before you build anything in ADO, run one ambiguity pass and revise the PRD based on what comes back:

```
Act as a Staff Engineer. List every assumption or ambiguity in this PRD that would
block estimation, and suggest a fix for each.
```

Update your PRD with at least one fix from this pass.

> **Want a worked example?** See `Demo_Preparation_Kit` → Day 2 for the full Northwind Outfitters "Promo Code at Checkout" version of every prompt above, including sample outputs.

## Step 4 — Build the ADO Hierarchy (15 min)

| ADO Item | Type | What to Enter |
|---|---|---|
| Feature | Feature (child of your Day 1 Epic) | Title = feature name; Description = Problem Statement + Goals & Non-Goals |
| Story 1 | User Story (child of Feature) | Title from PRD; Acceptance Criteria = matching Gherkin block |
| Story 2 | User Story (child of Feature) | Title from PRD; Acceptance Criteria = matching Gherkin block |
| Story 3 (optional) | User Story (child of Feature) | Title from PRD; Acceptance Criteria = matching Gherkin block |

Tag each story `DoR-pending` until you're confident the acceptance criteria are engineering-ready.

---

## Done When…

- [ ] You have a full PRD with all 6 standard sections
- [ ] Each user story has Gherkin-format acceptance criteria
- [ ] You ran the ambiguity pass and made at least one real revision
- [ ] Your Feature exists in ADO as a child of your Day 1 Epic
- [ ] At least 2 User Stories exist under the Feature with Acceptance Criteria populated

## Notes / Reflection

*What did the ambiguity-pass prompt catch that you wouldn't have thought to ask about yourself?*

```
[space for your notes]
```
