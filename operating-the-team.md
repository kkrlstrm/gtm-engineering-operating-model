# Operating the team

How the function is structured once you accept that a small number of humans now direct a large amount of agent-executed work. This is the org design that follows from the [principles](principles.md) — roles, decision rights, span of control, and the accountability model.

---

## The shape: small human teams over agent swarms

The instinct when agents get capable is to scale the swarm — more agents, more parallel work, one operator riding all of it. That's the wrong axis. The constraint isn't how many agents you *can* run; it's how many a human can still **hold ground truth on**. Past that line, the human is no longer leading the work — they're laundering it, signing off on output they can't actually evaluate.

So the unit that scales is the **small human team with agent leverage**, not the lone operator with an unbounded fleet. Fleet size per human is capped at the point where they can still catch a wrong-but-confident result. When you need more throughput, you add a human-plus-fleet unit, not more agents under the same human.

---

## Roles

Three roles, defined by **which layer they operate at**, not by seniority.

**The GTM engineer (operator).** Runs the agents against real work. Owns the runs, the escalations from their own fleet, and the ground truth for their slice. This is where the reps happen and where judgment is grown ([growing judgment](growing-judgment.md)). Their fleet is bounded so they can still hold the truth on it.

**The reviewer (the friction).** The second pair of eyes whose job is to **disconfirm**, not approve — to ask again when the answer came back too clean ([principle 3](principles.md)). Review is a distinct role, not a courtesy the operator does to their own work; you can't be the friction against your own confident output.

**The leader (a layer up).** Owns the intent, the playbook, and the standards the agents run on — not the runs ([principle 1](principles.md)). Builds the first reference, then hands it off ([principle 6](principles.md)). Dips back into the execution layer deliberately to stay calibrated, but does not live there. Provisions protection ([principle 2](principles.md)) and owns the outcomes the function is accountable for.

The point of defining roles by layer: a person can move between them, but the *work* at each layer is different, and collapsing two layers into one person is how a function loses either its leverage (leader does the work) or its safety net (operator reviews themselves).

---

## Decision rights

Autonomy is not uniform, and pretending it is destroys either speed or safety. Decision rights are allocated deliberately — and **who gets the autonomy ratchet is a fairness question**, watched as closely as comp.

| Decision class | Who decides | Why |
|---|---|---|
| How a run is executed within the playbook | The operator, autonomously | This is the leverage; gate it and you've killed it |
| Stopping a run on suspicion of drift | **Anyone**, without pre-justification | Silent failure is the expensive class; make the stop cheap ([principle 5](principles.md)) |
| Spend and irreversible actions | A named human, at an explicit gate | You can't undo these; they cross a human boundary by design ([principle 8](principles.md)) |
| Changing the playbook / standards | The leader | This is the layer the leader owns |
| Expanding an operator's autonomy or fleet | The leader, earned on demonstrated judgment | The autonomy ratchet is a reward and a fairness signal, not a default |

---

## The accountability model

The hard question in agent systems is *who owns an outcome no human directly produced?* This function answers it with one rule and three consequences.

**The rule:** every agent workflow has **one named human owner before it runs.** Not a committee, not "the team," not the model. One name.

That owner:

1. **Owns the rails** — the intent, guardrails, and playbook the agent runs inside. Governance is the architecture the agent runs *within*, decided in advance, not a report reconstructed afterward.
2. **Reviews the escalations** — the cases the system flags as ambiguous or high-stakes get human eyes, every time.
3. **Samples the rest** — spot-checks the routine runs on a cadence. Deliberately **not** eyeball-every-action: that's the fig leaf that doesn't scale and gives false comfort. Owning the rails plus sampling beats pretending to watch everything.

Because that owner is accountable for outcomes they didn't individually produce, they get two things in return: **real authority** over the rails (empowerment without authority is a setup), and the **protection** of a leader who absorbs blame upward when the agent — not the person — is what failed ([principle 2](principles.md)).

---

## Span of control, restated

Classic span of control asks how many *people* a manager can lead. Here the binding limit is different: how many *agent workflows* a named human can genuinely own — hold the rails, review the escalations, sample the rest — without it becoming a rubber stamp. That number is smaller than the number of agents you could technically point at one person, and honoring the gap is what keeps accountability real instead of nominal.

---

## What this deliberately is not

- **Not a swarm you scale infinitely.** The human's grip on ground truth is the ceiling, on purpose.
- **Not human-in-the-loop on every action.** It's human-owns-the-rails plus sampling — a stance, not a bottleneck.
- **Not flat autonomy.** Decision rights are allocated by class and earned by demonstrated judgment.
- **Not the architecture.** The systems that implement these rails are held close; this is the operating model around them.
