# Day 3 Lab — Sample Screen → Requirements → ADO PBIs/Tasks

**Duration:** 45 minutes · **Format:** Pairs
**Builds on:** Your Day 2 Feature
**Feeds into:** Day 4 (these PBIs join tomorrow's backlog)

## What You'll Need

- [ ] GitHub Copilot Chat open and signed in
- [ ] Your Day 2 Feature open in another tab
- [ ] A UI screen to describe — a real one from your product, or the provided sample screen

## Learning Goal

Translate a plain-language description of a UI screen into a user flow, functional requirements, and explicit UI states — then log the results as ADO Product Backlog Items (PBIs), tagged and linked correctly.

---

## Step 1 — Describe Your Screen in Plain Language (10 min)

Pick a real screen from your own product, or use the provided sample below if you don't have one ready. Write a plain-language description — layout, sections, key controls. No image needed; the description itself is the technique being taught.

**Provided sample (use if you don't have your own):**
```
Checkout page layout: header shows the store logo. Left column is a shipping
address form. Right column is an order summary card containing: a line-item
list, subtotal, a "Promo code" text input with an "Apply" button directly
beneath the subtotal, a discount line that is hidden until a code is applied,
tax, shipping, order total, and a large "Place Order" button at the bottom
of the right column.
```

**Your screen description:**
```
[write it here, or copy the sample above]
```

## Step 2 — Generate the Flow, Requirements & States (15 min)

Run these three prompts in the same Copilot Chat thread, in order, so each builds on the last:

```
1) Generate the user flow for a customer using this screen: [paste your screen description]

2) Extract the functional requirements from this flow.

3) Define the UI states for the key interactive elements on this screen:
   loading, error, empty, and success.
```

> **Want a worked example first?** See `Demo_Preparation_Kit` → Day 3 for the full Northwind Outfitters checkout-screen version of all three prompts and their sample outputs.

## Step 3 — Log the ADO PBIs (15 min)

Create 2–3 PBIs under your Day 2 Feature. Split by concern, not by screen — e.g., one PBI for input/validation, one for the resulting display change, one for a button's state handling.

| PBI | Title | Acceptance Criteria | Tag |
|---|---|---|---|
| 1 | [name the input/validation piece] | Paste the relevant empty/loading/error/success bullets | UX |
| 2 | [name the resulting display change] | Describe exactly what appears/changes and when | UX |
| 3 (optional) | [name any remaining state-dependent control] | Describe its enabled/disabled/loading behavior | UX |

## Step 4 — Attach the Design Context (5 min)

Paste your Step 1 screen description into the Description or a comment on at least one PBI, so the context travels with the ticket rather than living only in this worksheet.

---

## Done When…

- [ ] You have a written screen description (yours or the sample)
- [ ] You generated a user flow, functional requirements, and explicit UI states
- [ ] 2–3 PBIs exist under your Day 2 Feature, tagged `UX`
- [ ] At least one PBI's Acceptance Criteria explicitly covers a UI state (loading/error/empty/success)
- [ ] The screen description is attached to at least one PBI

## Notes / Reflection

*Which UI state would engineering most likely have had to ask you about, if it hadn't been captured here?*

```
[space for your notes]
```
