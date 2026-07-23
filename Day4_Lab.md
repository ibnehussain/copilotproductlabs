# Day 4 Lab — AI Workspace Setup + PRD → ADO Backlog + Simulated Sprint Planning

**Duration:** 10 min (workspace setup, done once) + 45 minutes (lab)
**Builds on:** Your Day 2 PRD (and Day 1 Epic / Day 3 requirements if you have them)
**Feeds into:** Day 5 (this same PRD gets reviewed and summarized; `.github/prompts/` gets built out)

## What You'll Need

- [ ] GitHub Copilot Chat open and signed in, in an IDE with a workspace open (VS Code, Visual Studio, or JetBrains)
- [ ] Your Day 1 Epic, Day 2 PRD, and Day 3 UI requirements — wherever they currently live (chat history, notes, or already-saved files)
- [ ] Your ADO sandbox with at least one open sprint/iteration created

---

## Step 0 — Set Up Your AI Workspace (10 min)

Today we give your artifacts a permanent, version-controlled home instead of leaving them scattered across chat history. Run the scaffold prompt below **once, in Plan mode**, review what it proposes, then approve to switch to **Agent mode** and have it actually create the structure.

> **Mode: Plan → Agent.** Plan mode will read your request and show you exactly which folders and files it intends to create before anything is written — review that list, then approve to move to Agent mode and build it.

The full scaffold prompt is provided separately as `scaffold-workspace-prompt.md` — paste its contents into Copilot Chat now.

**What you'll end up with:**

```
PM-Workspace/
├── .github/
│   ├── copilot-instructions.md   ← standing rules, applied automatically
│   └── prompts/                  ← empty for now — Day 5 builds this out
├── knowledge/     ← trusted, human-reviewed artifacts only
├── generated/     ← AI drafts — scratchpad, not trusted until reviewed
├── meetings/      ← real meeting notes, interviews, feedback
├── reference/     ← company standards, checklists
├── ui/            ← real screenshots, organized by screen name
├── architecture/  ← today's technical summaries and API expectations
└── ado/           ← local mirror of your Azure DevOps hierarchy
```

**The trust model in one line:** Copilot drafts go into `generated/` first. Nothing is trusted until you've reviewed it and moved it into `knowledge/` yourself — that move *is* the approval, no extra "approved" folder needed.

### Backfill What You Already Have

Once the structure exists, bring your earlier work into it. In the same chat thread:

```
I have existing artifacts from earlier work: [paste or reference your Day 1 Epic,
Day 2 PRD, and Day 3 UI requirements]. Move the reviewed versions of these into
the matching knowledge/ files (Vision.md, PRD.md, UserJourneys.md) and log
matching entries in ado/Epics.md, ado/Features.md, and ado/PBIs.md.
```

This is real Agent-mode file writing — review what it proposes before approving, same as any other write action.

---

## ⚡ Have the Azure DevOps MCP Server Set Up? (Optional)

If your Copilot is already connected to Azure DevOps through the **Azure DevOps MCP server** (GitHub's official integration — works with GitHub Copilot in **Agent Mode** in VS Code or Visual Studio), you can skip the manual copy-paste-into-ADO steps entirely. Instead of reading Copilot's output and typing it into the ADO UI yourself, you can ask Copilot to create and update the work items directly, in natural language, in the same chat.

**This is entirely optional.** Steps 2 and 3 below work exactly the same manually if you don't have MCP set up — look for the **"⚡ MCP SHORTCUT"** boxes at each step if you do.

**Don't have it set up yet, but want to try it?** It requires VS Code or Visual Studio with Copilot Agent Mode, plus the Azure DevOps MCP server added to your project (`microsoft/azure-devops-mcp` on GitHub has a two-minute setup guide). Not worth doing mid-session — try it after this course if it looks useful.

**One habit to keep either way:** MCP write actions create real changes in your actual ADO org, not a sandbox preview. Read what Copilot is about to create before confirming, the same way you'd review a PR before merging it.

## No Azure DevOps Access?

Same two options as Day 1: set up a free ADO org at `dev.azure.com` before the session, or capture these fields in `ado/Tasks.md` (or on paper, if you skipped the workspace setup) — same format either way.

```
WORK ITEM: [Story title from Day 2]
Story Points:
Rationale (from Copilot):
Iteration Path / Sprint:

TASK (child of the story above)   — copy this block per task
Title:
```

## Learning Goal

Give your Days 1–3 artifacts a permanent, version-controlled home, then break the PRD into an estimable backlog, sequence it into a two-week sprint, and practice translating a technical constraint into a business-impact summary a steering committee could actually use.

---

## Step 1 — Break the PRD into a Full Backlog (15 min)

**Mode: Plan** (drafting only — nothing gets written yet)

Reference your PRD directly from the workspace instead of pasting it:

```
Break #knowledge/PRD.md into a full backlog: Feature, User Stories, and Tasks,
with a suggested story-point estimate (1/2/3/5/8) and rationale for each.
```

(No workspace set up yet, or working outside an IDE? Paste the PRD text directly instead of using `#knowledge/PRD.md` — everything else below works the same either way.)

Read the rationale for each estimate, not just the number — you'll need it in Step 2.

## Step 2 — Populate ADO with Story Points (10 min)

**Mode: Agent** (this step writes — to `ado/Tasks.md` and/or real ADO)

For each User Story already created on Day 2 (plus any new ones Copilot suggested), set:

| Field | Value |
|---|---|
| Story Points | The number Copilot suggested — treat it as a starting point for team discussion, not a final answer |
| Comment | The one-line rationale, so the reasoning travels with the ticket |

Create any Task-level items Copilot suggested under their matching parent Story. If you're using the workspace, ask Copilot to log all of this into `ado/Tasks.md` in the same pass:

```
Log this backlog breakdown — stories, story points, rationale, and tasks — into
ado/Tasks.md, following the format already in that file.
```

> **⚡ MCP SHORTCUT — populate real ADO directly, not just the local log**
> ```
> Using the Azure DevOps MCP server, update the User Stories under [your Feature name]
> in [your project name] with the story points and rationale from the backlog
> breakdown above. Add each rationale as a comment on its story. Then create the
> suggested Task items as children of their matching parent story.
> ```
> Copilot will confirm what it's about to change before writing — review the list against what you actually expect before approving. Afterward, verify with:
> ```
> List the current work items under [your Feature name] with their Story Points
> and any Tasks, so I can confirm what was created.
> ```

## Step 3 — Sequence a Two-Week Sprint (10 min)

**Mode: Plan**, then **Agent** once you're ready to write the Iteration Path

```
Generate a two-week sprint backlog from these stories, sequencing by dependency and priority.
```

Set **Iteration Path** on each story to match the sprint Copilot assigned it to (Sprint 1 vs. Sprint 2, or your sandbox's actual iteration names).

> **⚡ MCP SHORTCUT — skip the manual entry above**
> ```
> Using the Azure DevOps MCP server, set the Iteration Path on each story under
> [your Feature name] to match the sprint sequencing above (e.g., [Sprint 1 name]
> for the foundational stories, [Sprint 2 name] for the dependent one).
> ```

> **Want a worked example?** See `Demo_Preparation_Kit` → Day 4 for the full Northwind Outfitters "Promo Code at Checkout" version, including a sample sprint split and rationale.

## Step 4 — Translate One Technical Constraint (10 min)

**Mode: Plan**

Think of one real technical constraint on your feature (or invent a plausible one — e.g., a schema migration, a third-party API limit, a security review). Write it down, then prompt:

```
Translate this technical constraint into a one-paragraph business-impact
summary for a steering committee: [your constraint]
```

Share the resulting paragraph in the session chat.

---

## Done When…

- [ ] Your PM-Workspace structure exists, with Days 1–3 artifacts backfilled into `knowledge/` and `ado/`
- [ ] Every User Story under your Feature has a Story Points value set
- [ ] Each story's Iteration Path reflects a specific sprint
- [ ] At least one story has a rationale comment explaining its estimate
- [ ] You've written one technical-constraint → business-impact paragraph and shared it

## Notes / Reflection

*Did any of Copilot's story-point estimates surprise you — higher or lower than you expected? Why might that be?*

```
[space for your notes]
```

*If you used the MCP shortcut: did having Copilot write directly to ADO change how carefully you reviewed its output before accepting it — more, less, or about the same as reading a suggestion and typing it in yourself?*

```
[space for your notes]
```
