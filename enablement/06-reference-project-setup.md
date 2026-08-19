# A Reference Project Setup

[Sprint zero](05-sprint-zero.md) says what an agent-ready project must have. This doc shows what one actually looks like: the shape on disk, the infrastructure behind it, what the people need, and a worked example. Tool names below are examples, not endorsements; swap in your org's equivalents. The shape is the point.

## The shape on disk

The center of an agent-ready project is a **plain repository of files**. Not a proprietary workspace, not a wiki, not a database: a versioned folder tree. This is a deliberate architectural choice, because files are the one substrate that every agent, every tool, and every human can read, diff, and link. If it matters to the project, it lives in the tree.

```
project-root/
├── AGENTS.md                  # AI instructions: the project's standing brief
│                              # (CLAUDE.md, or your runtime's convention)
├── README.md                  # human orientation: what, who, status
├── .skills/                   # skills manifest + project-local skills
│   ├── MANIFEST.md            # which global skills are active, with versions
│   └── summarize-vendor-spec/ # a project-local skill (candidate for global)
├── personas/
│   ├── delivery.md            # who runs the project: humans AND agents,
│   │                          # with mandates, boundaries, escalation rules
│   └── target/                # who the project serves, one file per persona
├── intake/                    # knowledge intake pipeline
│   ├── inbox/                 # raw documents land here, unprocessed
│   └── processed/             # originals move here after processing
├── knowledge/                 # the living knowledge base (pipeline output)
│   ├── INDEX.md               # agent-maintained map of what's known
│   ├── requirements/          # extracted, per-source
│   ├── research/              # summaries with project-relevant findings
│   └── reference/             # indexed specs, data dictionaries
├── meetings/                  # meeting record pipeline
│   ├── transcripts/           # raw notes and transcriptions land here
│   └── processed/             # per-meeting extraction output
├── decisions/
│   └── DECISION-LOG.md        # append-only: date, decision, deciders, rationale
├── backlog/                   # or a two-way link to Jira/ADO/Linear
│   ├── proposed/              # pipeline output awaiting human confirmation
│   └── accepted/
└── src/                       # the actual work product, if this is a software project
```

Three properties matter more than the exact names:

1. **Convention over configuration.** Every project in the org uses the same tree, so a skill written once ("sweep `meetings/transcripts/` for new files") works everywhere, and an agent dropped into any project knows where things are without being told.
2. **Proposed vs. accepted is structural.** Pipeline output lands in `proposed/` locations; humans move (or approve the move) into accepted ones. The human gate is a directory boundary, visible in every diff, not a policy hoped about.
3. **Everything is reviewable history.** Because the tree is a git repo, every agent action is a commit: inspectable, attributable, revertible. This is your audit trail and your trust-building mechanism in one.

## The infrastructure stack, in three tiers

Stand this up incrementally. Tier 1 delivers most of the value and costs an afternoon; don't gold-plate tiers 2 and 3 before the project has earned them.

### Tier 1: The minimum (repo + agent + conventions)

| Component | What it is | Example |
|---|---|---|
| Repository host | Versioned home for the tree, with permissions and PR review | GitHub, GitLab, Azure DevOps |
| Agent runtime | A coding/knowledge agent that operates on the tree | Claude Code or equivalent agentic CLI |
| Org template | The tree above as an instantiable template repo | GitHub template repository |
| Instructions file | `AGENTS.md` at root, inheriting an org-global instructions file | Managed by the platform/enablement team |
| Skills | Org skill library pulled in per project, plus locals | A shared `skills/` repo, versioned |
| Model access | API or subscription access for the runtime, with spend visibility | Org-managed keys, per-project tags |

At tier 1, the pipelines run **on demand**: a human drops files into `intake/inbox/` or `meetings/transcripts/` and tells the agent to process the new arrivals (or it happens as a standing step in the team's daily rhythm). This is not a lesser version; it's the assistive-first posture, and many projects never need more.

### Tier 2: Automation (the pipelines run themselves)

| Component | What it is | Example |
|---|---|---|
| Scheduled agent runs | The intake and meeting sweeps run on a timer or on file arrival | CI pipelines, scheduled agent jobs, cron-triggered runs |
| CI integration | Processing triggered by push: a new transcript lands, the pipeline PR appears | GitHub Actions or equivalent |
| Notifications | Pipeline output surfaces where the team lives | A channel post: "3 action items proposed from today's standup" |
| Review flow | Proposals arrive as pull requests, so confirmation is a code-review motion | PR review on `proposed/` → `accepted/` moves |

The key design at tier 2: **agent output arrives as pull requests, not as direct writes.** The team already knows how to review a PR; you're reusing an existing trust mechanism instead of inventing one.

### Tier 3: Integration (connected to where information is born)

| Component | What it is | Example |
|---|---|---|
| Source connectors | Agents read the systems where documents and conversations already live | MCP servers or native connectors for Drive/SharePoint, Slack/Teams, email |
| Meeting capture | Transcripts flow in automatically | Teams/Zoom transcription auto-exported to `meetings/transcripts/` |
| Tracker sync | Accepted backlog items flow to the org's tracker and back | Jira/ADO/Linear two-way integration |
| Knowledge query | The knowledge base is searchable from chat, not just from the repo | An org assistant grounded on `knowledge/` |

Tier 3 is where the "common sources" question gets answered structurally: instead of humans ferrying documents into the inbox, the connectors watch the places information is born (the meeting, the mailbox, the shared drive, the tracker) and land it in the tree automatically. Build connectors by the [third-time rule](../GLOSSARY.md): the third project that hand-ferries from SharePoint justifies the SharePoint connector, and the connector belongs to the platform, not the project.

## What the people need

### Every developer (or knowledge worker) on the project
- The agent runtime installed and authenticated, with access to the project repo
- The org's instructions and skills inherited automatically (they should never copy-paste setup)
- A sandbox norm: agents work on branches, humans merge
- One habit: route documents and meeting records into the tree instead of into private inboxes. The pipelines can only process what lands in them. This habit is the single biggest cultural component of the whole setup.

### The FDE or enablement engineer standing it up
- **Rights to instantiate**: create repos from the template, wire CI, register connectors, without a ticket queue in the way
- **The org template and skill library** as their starting kit, plus the authority to file template feedback (every project setup improves the template)
- **Access on behalf of agents**: service accounts and scoped credentials for the sources the pipelines read. Sort this in sprint zero; it is the access-optimism trap from the [engagement lifecycle](../forward-deployment/02-engagement-lifecycle.md) in miniature.
- **Spend and audit visibility**: model usage per project, and the commit history as the action log

### The platform team behind them
- Owns the template repo, the global skill library, the org-global instructions file, and the connector catalog
- Runs the graduation path: local skill wanted three times → global library; hand-ferry done three times → connector
- Sets the paved-road defaults (approved models, data tiers, logging) so projects inherit governance instead of applying for it

## Worked example: "Meridian", a claims-triage project

A concrete fiction to make it tangible. An internal FDE pair embeds with a claims team to build AI-assisted triage. Sprint zero, tier 1, takes them one day:

1. **Instantiate.** `gh repo create claims-triage --template org/project-template`. The tree above exists in minute one.
2. **Write the brief.** `AGENTS.md` gets the project's purpose ("cut claim first-touch from 3 days to 4 hours"), scope ("triage only; no adjudication"), constraints ("PII stays in the claims system; the tree holds claim IDs, never claim contents"), conventions, and pointers.
3. **Define the personas.** `personas/delivery.md` names the humans (sponsor: claims VP; problem owner: senior adjuster; champion: the adjuster everyone already asks; the FDE pair; platform on-call) and the agents: "Intake Processor" (classifies and processes inbox arrivals, writes only to `proposed/` and `knowledge/`, escalates unclassifiable documents) and "Meeting Analyst" (sweeps transcripts, proposes actions/decisions/refinements as PRs, never writes the decision log directly). `personas/target/adjuster.md` captures what discovery found: the adjuster's goal (clear the queue without missing a fraud flag), pain (re-keying between three systems), protected judgment (coverage calls stay theirs), and their verification behavior (they'll spot-check routing for weeks before trusting it, and the check must take seconds).
4. **Attach skills.** `MANIFEST.md` activates four global skills: `process-requirements-doc`, `summarize-research`, `extract-meeting-actions`, `maintain-knowledge-index`. One local skill gets stubbed: `summarize-claims-policy` (it knows the insurer's policy-document format). It's noted as a graduation candidate, since two other insurance-adjacent projects exist.
5. **Seed the intake.** The kickoff dump goes into `intake/inbox/`: the current triage SOP, two vendor specs, a compliance memo, an old consulting deck. The agent classifies each, processes by type, and files output: the SOP becomes `knowledge/requirements/triage-sop.md` with 14 extracted rules; the compliance memo yields 3 constraints that also get appended to `AGENTS.md`'s constraints section (via PR); the deck gets summarized to one page with a note that its volume numbers are stale.
6. **Smoke-test the meeting pipeline.** Kickoff meeting transcript lands in `meetings/transcripts/2026-08-19-kickoff.md`. The extraction run opens a PR: 5 proposed action items (with owners), 2 decisions for the log ("manual review stays for claims over $50k", decided by the sponsor, with rationale), and 1 refinement attaching an acceptance criterion to an existing backlog item. The champion reviews the PR, rejects one action item as misheard, merges the rest. The pipeline works; sprint zero's definition of done is met.
7. **File template feedback.** The FDE notes that classifying the consulting deck needed a document type the template's mapping lacked ("third-party analysis") and files it against the template repo.

From day two, the rhythm is set: documents and transcripts flow into the tree, proposals flow out as PRs, the champion confirms in minutes a day, and the knowledge base and decision log stay current without anyone maintaining them by hand. When the team later wants transcripts to arrive automatically (tier 2/3), the structure doesn't change; only the ferrying does.

## What to avoid

- **A workspace agents can't reach.** If project knowledge lives primarily in a proprietary wiki or someone's drive, every agent interaction starts with an export. The tree is primary; other surfaces mirror it.
- **Standing up tier 3 in sprint zero.** Connectors and sync are platform work, justified by repetition. A project that spends its first month on integration is [platform-before-proof](03-failure-modes.md) at project scale.
- **Per-project snowflake infrastructure.** If the project needs a component the template lacks, that's template feedback, not a local invention (unless it's genuinely bespoke, in which case document why).
- **Agents with human credentials.** Pipelines run on scoped service identities from day one. The handoff checklist's "grep the config for the FDE's name" applies here from the start, not at the end.
