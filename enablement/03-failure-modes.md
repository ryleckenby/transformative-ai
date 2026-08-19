# Failure Modes: How Enablement Programs Die

Enablement programs rarely die dramatically. They die of politeness: slowly, with good dashboards. This catalog is for spotting the pattern early, while it's still cheap to correct. Each entry: what it looks like, why it happens, and the counter-move.

## 1. Adoption theater

**Looks like:** Impressive activity metrics (seats provisioned, weekly actives, prompts sent, "AI champions trained") with no workflow that works differently than it did a year ago.

**Why it happens:** Activity is easy to measure and easy to buy; outcomes are neither. Programs report what makes the program look good.

**Counter-move:** Every quarterly review must name specific workflows and their before/after numbers. If the program can't name three, it's at Stage 1 wearing a Stage 3 costume. See [04-measuring-impact.md](04-measuring-impact.md).

## 2. The slide factory (center of excellence without deployment)

**Looks like:** A central AI team producing strategies, guidelines, vendor evaluations, and maturity assessments: everything except shipped workflow changes. Business teams learn to route around it.

**Why it happens:** Central teams are staffed with strategists instead of builders, and measured on governance artifacts instead of deployments.

**Counter-move:** Require the central team to spend a majority of its time embedded with business teams, shipping. This is the core argument for the [forward-deployment model](../forward-deployment/00-overview.md): the center exists to serve deployments, not the reverse.

## 3. Platform before proof

**Looks like:** Six months building the internal "AI platform" (gateway, vector store, agent framework) before any workflow win exists. The platform ships; nobody comes.

**Why it happens:** Platform work feels strategic and is comfortable for engineers; sitting with the claims-processing team feels like consulting. Also, infrastructure has no users to disappoint, yet.

**Counter-move:** Platform components must be *extracted from* working deployments, never speculated in advance. Rule of thumb: build a shared component when the third deployment needs it.

## 4. The pilot graveyard

**Looks like:** Dozens of pilots, none in production. Every demo impresses; nothing survives contact with security review, data access requests, or the budget cycle.

**Why it happens:** Pilots are scoped for demo-ability, not production-ability. The hard constraints (data access, compliance, who maintains this) are deferred rather than confronted.

**Counter-move:** Scope every pilot with its production path in view: use real data (or realistic scale) from week one, involve security/compliance at kickoff rather than at handoff, and name the long-term owner *before* the pilot starts. A pilot with no willing owner should not begin.

## 5. Tool-first thinking

**Looks like:** The program is organized around tools ("roll out X to all departments") rather than workflows. Success is defined as deployment completion.

**Why it happens:** Procurement is the muscle organizations already have. Buying is legible; workflow redesign is not.

**Counter-move:** Reorganize the roadmap by workflow, not by tool: not "deploy copilot to legal" but "cut contract first-pass review from 3 days to 3 hours." Tools become means, which is what they are.

## 6. Champion burnout

**Looks like:** The early enthusiasts who drove the first wins go quiet. They were doing enablement *on top of* their day job, unrecognized, and the org treated their extra output as the new baseline.

**Why it happens:** Enablement labor is invisible in most performance systems.

**Counter-move:** Give champions allocated time (real percentage, on their manager's books), visibility (their wins presented by name), and career credit. What happens to the first champions is broadcast to every potential future one.

## 7. Trust collapse

**Looks like:** An early, visible AI failure (a hallucinated figure in a client deliverable, a bad automated reply) and usage craters org-wide, including in workflows that were working.

**Why it happens:** Verification steps were designed out too early (autonomy before track record), and expectations weren't set that error rates are nonzero and managed, not zero.

**Counter-move:** Assistive-before-autonomous as a hard default; explicit verification gates on anything outward-facing; and pre-agreed error budgets ("we expect X%, we catch them here") so a failure is an expected event inside a system, not a scandal.

## 8. Governance as veto

**Looks like:** Every use case requires a review board that meets monthly and defaults to no. Shadow AI flourishes; sanctioned AI stagnates. The org gets all the risk and none of the value.

**Why it happens:** Risk functions are accountable for failures, not for foregone gains. Their rational move is to block.

**Counter-move:** Governance as a *paved road*, not a gate: pre-approved patterns, tools, and data tiers where teams can move without asking, and review reserved for genuinely novel risk. Make the risk function co-own an adoption metric so "no" stops being free.

## 9. Frontier blindness

**Looks like:** The program's assumptions about what AI can't do were set 18 months ago and never revisited. Whole categories of work sit untouched because "we tried that in the GPT-4 era and it didn't work."

**Why it happens:** Evaluation is expensive, and organizations calcify conclusions.

**Counter-move:** Keep the eval sets from every killed pilot and re-run them on a cadence (or at each major model release). A kill decision has a shelf life; treat "not yet" and "no" as different verdicts.

---

**Meta-observation:** almost every failure mode above is a feedback-loop failure. Between the center and the edge (2, 3), between activity and outcome (1, 5), between risk and value (7, 8), or between effort and reward (6). The programs that survive are the ones that wire the loops deliberately. That is, at bottom, what [forward deployment](../forward-deployment/00-overview.md) is: a feedback loop with a job title.
