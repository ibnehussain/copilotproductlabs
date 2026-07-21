# Day 2 Lab — Full PRD → Azure DevOps Hierarchy

**Duration:** 45 minutes · **Format:** Individual or pairs
**Builds on:** Your Day 1 Epic
**Feeds into:** Day 4 (this PRD becomes tomorrow's estimated backlog) and Day 5 (this PRD gets reviewed and summarized)

> **This lab now includes optional "Try It Another Way" prompt variants at every step.** The core path (one prompt per step) still fits in 45 minutes — the variants are there so you can compare how a small change in role, framing, or output format changes what Copilot gives you. Try at least one variant somewhere in this lab; it's the fastest way to build real prompting intuition. If you're short on time, skip straight to the primary prompt and come back to variants later.

## What You'll Need

- [ ] GitHub Copilot Chat open and signed in
- [ ] Your Day 1 ADO Epic open in another tab
- [ ] Rough notes for one feature that belongs inside that Epic (a few bullet fragments is enough)

## No Azure DevOps Access?

Same two options as Day 1: set up a free ADO org at `dev.azure.com` (Basic plan, free for the first 5 users) before the session, or capture these same fields offline instead of clicking into a tool.

```
WORK ITEM TYPE: Feature (child of your Day 1 Epic)
Title:
Description:

WORK ITEM TYPE: User Story (child of the Feature above)   — copy this block per story
Title:
Acceptance Criteria (Gherkin):
Tag: DoR-pending
```

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

Read the output critically before moving on — does it actually sound like your feature, or could it describe almost anything?

### 🔀 Try It Another Way (optional)

Run the **same rough notes** through one or more of these variants in a **fresh chat thread**, then compare the resulting PRDs side by side.

**Variant A — Different role, same task:**
```
Act as a skeptical Engineering Lead scoping a new feature. Using the structure
Problem Statement / Goals & Non-Goals / User Stories / Functional Requirements /
Non-Functional Requirements / Acceptance Criteria, turn the notes below into a
full PRD. Flag anything you'd push back on in planning.

Notes:
[paste the same rough notes]
```

**Variant B — UX-first framing:**
```
Act as a PM who cares most about user experience. Using the same PRD structure,
turn the notes below into a full PRD, but put extra emphasis on the User Stories
section — write at least 4 stories covering different user situations, not just
the happy path.

Notes:
[paste the same rough notes]
```

**Variant C — Tighter output constraint:**
```
Using the same PRD structure, turn the notes below into a full PRD — but keep
the entire PRD under 200 words total. Be as concise as possible without dropping
any section.

Notes:
[paste the same rough notes]
```

**Compare:** Which version would you actually hand to an engineer? Which would you hand to a VP? Jot your answer below — you'll use it in the reflection at the end of this lab.

```
[space for your comparison notes]
```

## Step 2 — Convert User Stories to Gherkin (10 min)

Once you have the PRD, run this follow-up prompt in the same chat thread so Copilot has the PRD as context:

```
Convert the user stories above into Gherkin-format acceptance criteria (Given/When/Then).
```

### 🔀 Try It Another Way (optional)

Still in the same thread (so Copilot keeps the PRD as context), try one of these instead of — or in addition to — the primary prompt:

**Variant A — Plain-language instead of Gherkin:**
```
Instead of Gherkin, rewrite the acceptance criteria as plain-language checklist
items a non-technical stakeholder could understand at a glance.
```
*Compare: which format would a QA engineer prefer? Which would a VP prefer in a status update?*

**Variant B — Push for more edge cases:**
```
For each user story, add at least one additional Gherkin scenario covering an
edge case or failure path we haven't discussed yet (e.g., network failure,
empty input, concurrent access).
```
*Compare: did this surface anything you'd genuinely missed?*

## Step 3 — Stress-Test It Once (5 min)

Before you build anything in ADO, run one ambiguity pass and revise the PRD based on what comes back:

```
Act as a Staff Engineer. List every assumption or ambiguity in this PRD that would
block estimation, and suggest a fix for each.
```

Update your PRD with at least one fix from this pass.

### 🔀 Try It Another Way (optional)

Different reviewer roles catch different problems. Try one of these on the same PRD and see what a Staff Engineer's pass missed:

**Variant A — QA Lead's perspective:**
```
Act as a QA Lead. Review this PRD specifically for testability — which
requirements are too vague to write a test case against? What's missing to
make each acceptance criterion verifiable?
```

**Variant B — Security/risk reviewer's perspective:**
```
Act as a security-focused reviewer. Review this PRD for data-handling, access
control, or abuse-risk gaps that aren't addressed anywhere in the requirements.
```

**Compare:** Did the QA or security pass catch something the Staff Engineer pass didn't? This is the core lesson of this variant — no single reviewer role catches everything, which is exactly why Day 5's review demo stacks multiple perspectives on one PRD.

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
- [ ] You tried at least one "Try It Another Way" variant and compared it to your primary output

## Notes / Reflection

*What did the ambiguity-pass prompt catch that you wouldn't have thought to ask about yourself?*

```
[space for your notes]
```

*Of the prompt variants you tried, which one changed the output the most — the role, the framing, or the output-format constraint? What does that tell you about which lever to reach for first when a Copilot output isn't quite right?*

```
[space for your notes]
```
