# The Engagement Lifecycle

How a single forward-deployment engagement runs, from qualification to handoff. Written to work for both arenas — vendor→customer and internal platform→business team — with notes where they differ. Timeboxes are typical for an AI workflow engagement; scale to taste.

```
Qualify → Charter → Discover → Build → Prove → Harden → Hand off
 (gate)   (1 wk)    (1–2 wks)  (2–6 wks) (2–4 wks) (2–4 wks)  (designed from day 1)
```

## 0. Qualify — decide whether to engage at all

Forward deployment is expensive; qualification is the throttle. Take the engagement when:

- there's an **accountable sponsor** with budget/authority and a named problem owner who wants this (pull, not push)
- the workflow at stake is **frequent, painful, and measurable** (same criteria as the [adoption playbook](../enablement/02-adoption-playbook.md), because it's the same decision)
- **data and system access are achievable** within the engagement window — access is the #1 schedule killer; test it now, not in week four
- the engagement can **teach the platform something** — if you've done this exact deployment five times, it should be product by now, not an engagement

Decline (or descope) when the sponsor wants a demo for a board meeting, when no one will own the result, or when access can't be granted. A declined bad engagement is a win.

## 1. Charter — one page, signed

Before anyone builds: a one-page charter (template: [engagement charter](../playbooks/engagement-charter.md)) naming the workflow, the measurable target, the timebox, the people (sponsor, problem owner, FDE, champion), the access required and when it lands, and **the end state** — who owns this when the FDE leaves. Unsigned charters produce unbounded engagements.

## 2. Discover — learn the work before changing it

1–2 weeks embedded with the people who do the work. Shadow real sessions, not walkthroughs. Map the workflow as it is (inputs, judgments, outputs, pain, failure cost — the [Phase 2 method](../enablement/02-adoption-playbook.md)). Collect **golden examples**: real inputs with known-good outputs, which become the seed eval set.

Discovery's deliverable is a *revised* charter: the problem as found is never quite the problem as chartered. Renegotiate now, in writing — this is the cheapest moment to change scope you will ever have.

**Vendor note:** discovery is also where you earn the room. Show up curious about their work, not eager about your product.

## 3. Build — the thin path, in their context

Ship the smallest end-to-end version that touches real data and real users — in weeks, not months. Principles:

- **In their systems, not beside them.** The output lands in the ticket queue / CRM / document repo they already live in.
- **Assistive first.** Human gates on every consequential output until a track record exists.
- **Evals grow with the build.** Every failure found in testing becomes an eval case. By Prove, you have a harness, not vibes.
- **Log everything.** Instrumentation for the before/after measurement goes in now.
- **Borrow depth from platform.** The FDE pulls platform engineers for hard sub-problems rather than hand-rolling; every hand-rolled piece is future graduation debt.

## 4. Prove — side-by-side, measured

Run new path alongside old with the champion and a small user group, against the baseline captured in Discover. Weekly retros; expect and pre-announce the week-1–2 dip. End with an explicit verdict against the charter's target: **harden** or **kill**. A clean kill with documented reasons (and a preserved eval set — capability moves) protects the relationship and your credibility. See [measuring impact](../enablement/04-measuring-impact.md) for the scorecard discipline.

## 5. Harden — make it survive your departure

The difference between a pilot and a deployment is everything in this phase:

- production access paths (no FDE laptop in the loop), monitoring and alerting on quality metrics, a documented runbook
- **the old path retired** on a named date — dual paths decay into the old one
- full-team rollout with training led by the champion (not the FDE — the org must see its own people running this)
- ongoing eval cadence and an owner for model/prompt/agent updates

## 6. Hand off — the designed ending

Handoff was designed in the charter; now execute it: named owner operating independently for 2+ weeks before the FDE exits, a written handoff doc ([checklist](../playbooks/handoff-checklist.md)), and a scheduled 30/90-day health check.

Then the FDE's last deliverable: the **field report** — what the platform lacked, what was hand-rolled (graduation candidates), what surprised, what the next engagement in this domain should do differently. This document is where the engagement pays its dividend to the loop.

## Anti-patterns across the lifecycle

- **The permanent engagement.** No end state in the charter → FDE becomes staff augmentation. The fix is always in the charter.
- **Demo-driven scoping.** Building for the steering-committee meeting instead of the daily user. Demos should be byproducts of real progress.
- **Access optimism.** "Security will grant it by week 3" — it never lands by week 3. Gate the engagement start on access being in flight with a date.
- **Skipping the baseline.** No before-measurement → no defensible claim → the renewal/expansion conversation runs on anecdote.
- **Hero handoff.** The FDE hands off to... no one, or to a doc. If the owner didn't run it alone for two weeks while the FDE was still reachable, it isn't handed off.
