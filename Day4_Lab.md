# Day 4 Lab — PRD → ADO Backlog + Simulated Sprint Planning

**Duration:** 45 minutes · **Format:** Individual or pairs
**Builds on:** Your Day 2 PRD
**Feeds into:** Day 5 (this same PRD gets reviewed and summarized)

## What You'll Need

- [ ] GitHub Copilot Chat open and signed in
- [ ] Your Day 2 PRD (in Copilot Chat history, or pasted into a note)
- [ ] Your ADO sandbox with at least one open sprint/iteration created

## Learning Goal

Break a PRD into an estimable backlog, sequence it into a two-week sprint, and practice translating a technical constraint into a business-impact summary a steering committee could actually use.

---

## Step 1 — Break the PRD into a Full Backlog (15 min)

Paste your Day 2 PRD into Copilot Chat with this prompt:

```
Break this PRD into a full backlog: Feature, User Stories, and Tasks, with a
suggested story-point estimate (1/2/3/5/8) and rationale for each:

[paste your Day 2 PRD]
```

Read the rationale for each estimate, not just the number — you'll need it in Step 2.

## Step 2 — Populate ADO with Story Points (10 min)

For each User Story already created on Day 2 (plus any new ones Copilot suggested), set:

| Field | Value |
|---|---|
| Story Points | The number Copilot suggested — treat it as a starting point for team discussion, not a final answer |
| Comment | The one-line rationale, so the reasoning travels with the ticket |

Create any Task-level items Copilot suggested under their matching parent Story.

## Step 3 — Sequence a Two-Week Sprint (10 min)

```
Generate a two-week sprint backlog from these stories, sequencing by dependency and priority.
```

Set **Iteration Path** on each story to match the sprint Copilot assigned it to (Sprint 1 vs. Sprint 2, or your sandbox's actual iteration names).

> **Want a worked example?** See `Demo_Preparation_Kit` → Day 4 for the full Northwind Outfitters "Promo Code at Checkout" version, including a sample sprint split and rationale.

## Step 4 — Translate One Technical Constraint (10 min)

Think of one real technical constraint on your feature (or invent a plausible one — e.g., a schema migration, a third-party API limit, a security review). Write it down, then prompt:

```
Translate this technical constraint into a one-paragraph business-impact
summary for a steering committee: [your constraint]
```

Share the resulting paragraph in the session chat.

---

## Done When…

- [ ] Every User Story under your Feature has a Story Points value set
- [ ] Each story's Iteration Path reflects a specific sprint
- [ ] At least one story has a rationale comment explaining its estimate
- [ ] You've written one technical-constraint → business-impact paragraph and shared it

## Notes / Reflection

*Did any of Copilot's story-point estimates surprise you — higher or lower than you expected? Why might that be?*

```
[space for your notes]
```
