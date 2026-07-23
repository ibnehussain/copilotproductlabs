
Create folders with the following structure. For each
file, create it with the content described — use empty section headers as
placeholders where noted, not filled-in example content.

.github/copilot-instructions.md — rules for this workspace: (1) generated/ holds
untrusted AI drafts; knowledge/ holds only human-reviewed content; ground every
new draft in knowledge/, never in generated/. (2) Moving a file from generated/ to
knowledge/ is the approval step — no version-numbered files (PRD-v1.md etc.), git
tracks history. (3) PRDs use six sections in order: Problem Statement, Goals &
Non-Goals, User Stories, Functional Requirements, Non-Functional Requirements,
Acceptance Criteria (Gherkin). (4) Epics contain a problem statement, 2-3
personas, one JTBD statement, 2-3 measurable success metrics. (5) PBIs always
specify UI states (empty, loading, error, success) where relevant. (6) Default to
Context+Goal+Constraints+Output when drafting from a rough idea. (7) When
reviewing an artifact, actively look for ambiguity, missing edge cases, and
unstated assumptions. (8) Note explicitly which parts of an answer are confirmed
by a source versus inferred. (9) Map every artifact to its ADO equivalent: Epic >
Feature > User Story/PBI > Task. (10) Story point suggestions always include a
one-line rationale, never a bare number. (11) Only artifacts that moved through
generated/ → knowledge/ review should be published to ado/ or written to Azure
DevOps via MCP.

.github/prompts/ — create the folder with just one file, README.md, containing:
"This folder is built out on Day 5, where ad-hoc prompts become reusable
.prompt.md files. Nothing to do here yet."

knowledge/ — BusinessContext.md (empty, for hand-written starting context, not
AI-generated), Vision.md, PRD.md, Personas.md, UserJourneys.md,
CompetitiveAnalysis.md, NFR.md, Risks.md, Assumptions.md, ReleasePlan.md — each
with a one-line header noting its purpose and "approved from generated/", followed
by empty section headers matching that artifact type.

generated/ — just a README.md explaining this is the untrusted AI-draft
scratchpad; nothing gets trusted until moved to knowledge/.

meetings/ — just a README.md explaining this holds real meeting notes and
customer interviews as plain files.

reference/ — just a README.md explaining this holds company standards
(accessibility, security, brand guide) too long for copilot-instructions.md.

ui/ — a Wireframes/ subfolder, plus a README.md noting screenshots should be
organized in subfolders by screen name (e.g., ui/checkout/), not loose at the root.

architecture/ — SolutionArchitecture.md, APIs.md, DataModel.md, Integrations.md —
each with a one-line header noting it's engineering-facing and should route
through engineering review before being treated as final.

ado/ — Epics.md, Features.md, PBIs.md, Tasks.md, TestCases.md,
AcceptanceCriteria.md, Bugs.md — each framed as a log/index (one entry per item,
fields for ADO Work Item ID and parent link) rather than a duplicate source of
truth.

README.md — explain the folder structure, the generated/ → knowledge/ trust
model, and note .github/prompts/ gets built out on Day 5.

Do not populate any file with example/demo content — every file should be a clean,
empty starter template ready for real use.