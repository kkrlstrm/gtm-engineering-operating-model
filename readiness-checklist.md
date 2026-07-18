# Production-readiness checklist

Before an agent runs unattended against real work, the question to answer is **not** "does the code work?" — it's "is the *team* ready to own what this agent does?" Readiness is an organizational property, not a technical one. A perfectly-built agent with no named owner and no stop authority is not ready; a modest agent with clear ownership, a kill switch, and a blameless review culture is.

This is the bar. It deliberately says nothing about implementation — that's held close. It's about whether the human operating model around the agent is in place.

---

## Ownership

- [ ] **One named human owns this workflow's outcome.** Not a team, not a rotation, not the model. One name, on record, before it runs.
- [ ] That owner **owns the rails** — they can change the intent, guardrails, and playbook the agent runs inside.
- [ ] That owner has **real authority**, not just accountability. They aren't set up to be blamed for something they can't control.

## Control

- [ ] **Kill authority is pre-authorized**, not requested mid-incident. Someone can stop this now, without a meeting.
- [ ] **Anyone can halt a run on suspicion**, without pre-justifying it, at no cost to their standing.
- [ ] **Spend and irreversible actions cross an explicit human gate.** Nothing unrecoverable happens fully unattended.
- [ ] The **fleet is bounded** to a size the owner can still hold ground truth on. Throughput past that line is added as a new human-plus-fleet unit, not a bigger fleet.

## Oversight

- [ ] **Escalations reach a human by default.** When the system is unsure, that's a human decision, not an agent guess.
- [ ] **Routine runs are sampled on a cadence** — not eyeballed one-by-one, but not unwatched either.
- [ ] The **process is observable, not just the output.** You can tell the lucky run from the clean run after the fact.

## Culture

- [ ] **The false alarm is funded.** Stopping a run that turns out fine is a thanked event, on the record, not a quiet ding.
- [ ] **Failure routes to the rails, not the person.** The post-incident question is "what let this through?", never "whose fault?"
- [ ] The owner is **protected** — the leader absorbs blame upward when the agent, not the person, is what failed.

## Judgment

- [ ] Whoever operates this **can tell when its confident output is wrong** — they've done predict-then-compare reps on it, not just watched it run.
- [ ] The workflow is **classified** ([build vs. hold](build-vs-buy.md)): you know whether it's a commodity you're renting or a high-judgment capability you're holding close — and if the latter, whose leverage it depends on.

---

## Scoring

This isn't a percentage. **Ownership** and **Control** are gating — if any box in those two sections is unchecked, the agent is not ready to run unattended, full stop, regardless of how good the rest looks. **Oversight**, **Culture**, and **Judgment** are the difference between an agent that runs safely for a week and one that runs safely for a year; gaps there are debt you're choosing to carry, and you should carry them knowingly, with a date to close them.

The checklist earns its keep by making the human model **explicit before launch** — so that when something does go wrong (it will), the ownership, the stop authority, and the blameless response are already in place, not improvised under pressure.
