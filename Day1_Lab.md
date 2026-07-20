# Lab 1 — Idea → Problem Statement → Personas → JTBD → Metrics → ADO Epic

**Day:** 1 · **Duration:** 35 minutes · **Format:** Pairs
**Builds on:** Nothing — this is where the week starts.
**Feeds into:** Lab 2 (your Epic becomes tomorrow's Feature)

## What You'll Need

- [ ] GitHub Copilot Chat open and signed in
- [ ] Access to the Azure DevOps (ADO) sandbox/training project
- [ ] One real, current idea from your own backlog (the messier, the better)
- [ ] A partner

## Learning Goal

Turn a vague idea into a structured problem statement, personas, JTBD, and success metrics using the **Context + Goal + Constraints + Output** (CGCO) prompting pattern — then log it as a properly-fielded ADO Epic.

---

## Step 1 — Write Your Messy One-Liner (10 min)

With your partner, pick one real idea sitting in your backlog right now — something you haven't fully written up yet. Write it as a single, rough sentence, exactly as messy as it actually is in your head. Don't clean it up.

> Example (don't copy — use your own): *"we should probably let people save items for later instead of just adding to cart"*

**Your one-liner:**

```
[write it here]
```

## Step 2 — Structure It with CGCO (10 min)

Paste the following into Copilot Chat, filling in the bracketed parts with your own idea and context. Keep the structure — Context, Goal, Constraints, Output — even if your answers are short.

```
Act as a Senior Product Manager.
Context: [your product/team, your users, what exists today, what doesn't]
Goal: Define the problem statement, target user personas, and top 3 goals for [your idea].
Constraints: [timeline, tech, team size, compliance — whatever actually applies]
Output format: A one-paragraph problem statement, followed by 2 personas (name, role, need),
1 JTBD statement ("When [situation], I want to [motivation], so I can [outcome]"),
and 2 measurable success metrics, in a table.
```

Read the output critically before moving on — does it actually sound like your product, or could it describe anyone's? If it's generic, add one more specific constraint and re-run it.

> **Stuck, or want to see a worked example first?** See `Demo_Preparation_Kit` → Day 1 → Part B for the full Northwind Outfitters version of this exact prompt and its output.

## Step 3 — Log It as an ADO Epic (10 min)

Create a new Epic in the sandbox project and populate these fields directly from Copilot's output — copy, don't retype:

| ADO Field | What to Paste |
|---|---|
| Title | A one-line version of your problem statement |
| Description | The full problem statement paragraph |
| Acceptance Criteria | The 2 personas, JTBD statement, and 2 success metrics, as bullets |
| Area Path | Your team's area path |
| Iteration Path | Your team's current planning period |
| Tags | 1–2 short tags for this idea |

## Step 4 — Share (5 min)

Copy your Epic's link (or take a screenshot) and share it in the session chat. Be ready to talk through it for 60 seconds if called on.

---

## Done When…

- [ ] You have a problem statement that's specific to your product, not generic
- [ ] You have 2 personas and 1 JTBD statement
- [ ] You have 2 measurable (not vague) success metrics
- [ ] An ADO Epic exists with all fields above populated
- [ ] You've shared the Epic link in chat

## Notes / Reflection

*What changed between your one-liner in Step 1 and the structured version in Step 2? Where did Copilot's output surprise you — in a good way or a way you had to correct?*

```
[space for your notes]
```
