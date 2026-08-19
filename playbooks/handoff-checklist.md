# Handoff Checklist (Template)

The gate between "the FDE built something" and "the team owns something." Nothing here is optional; each unchecked box is a specific way handoffs fail. The FDE and the incoming owner walk this together; the sponsor signs the bottom.

## Ownership

- [ ] **Named owner** on the host team (a person, not a team name), and their manager has this in their goals
- [ ] Owner has run the workflow **solo for 2+ weeks** while the FDE was still reachable — including at least one incident or anomaly handled without FDE intervention
- [ ] Backup owner named (vacation/departure coverage)
- [ ] Escalation path written: what the owner handles, what goes to platform, what pages whom

## Operations

- [ ] Runs entirely on **production access paths** — no FDE credentials, laptops, or personal accounts anywhere in the loop (grep the config for the FDE's name; you'll be surprised)
- [ ] Monitoring live on the quality metrics from the [scorecard](pilot-scorecard.md), with alert thresholds and a named recipient
- [ ] **Runbook** exists and has been tested by the owner performing each procedure at least once: restart/recover, common failure signatures, how to pause the AI path and fall back gracefully
- [ ] Costs (inference, tooling) land in the host team's budget line, and the owner knows the run-rate

## The AI-specific layer

- [ ] **Eval set** lives in a shared location the owner can run; owner has run it and can read the results
- [ ] Re-eval triggers written down: model version changes, prompt/agent changes, [cadence] — and the owner knows a *capability upgrade* is also a trigger (the workflow may be able to do more now, not just still work)
- [ ] Prompt/agent/config under version control the *host team* can access, with change process defined (who can edit, what requires re-eval)
- [ ] Autonomy level documented: where the human gates are, and the pre-agreed conditions for loosening or tightening them
- [ ] Known failure modes listed with examples — what the AI gets wrong, how it looks when it does, what the human should check

## The team

- [ ] Full team trained — **by the champion, not the FDE** (the org must watch its own people running this)
- [ ] Old path **retired** (or retirement date set and communicated); any parallel-run period has an explicit end
- [ ] The scorecard results shared with the team, with the champion's name on the win

## The loop

- [ ] **Field report** delivered to the platform team/backlog: hand-rolled components (graduation candidates), platform gaps hit, surprises, advice for the next engagement in this domain
- [ ] Pattern write-up published to the internal library (or the "genuinely bespoke because X" note filed)
- [ ] **30-day and 90-day health checks** scheduled — calendar invites sent now, with the metric review as the agenda
- [ ] Engagement retro held: what the *FDE practice* should do differently next time

---

**Handoff accepted:**

Owner: ____________ Champion: ____________ Sponsor: ____________ FDE: ____________ Date: ________

*After the 90-day check passes, the engagement is closed. If the 30-day check finds the workflow reverted to the old path, that's not the team's failure — it's a handoff that gated on the wrong things. Reopen, diagnose, fix the checklist.*
