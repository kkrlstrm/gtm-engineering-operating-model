# Failure & doubt

Agent failure doesn't look like a crash. It looks like a green run that quietly produced the wrong thing. This is how the function catches that class of failure and responds to it without punishing the people who surface it.

---

## The failure you actually have to fear is silent

A system that crashes tells you it failed. An agent usually doesn't. It returns a clean, confident, well-formatted answer that is wrong — and the run stays green. Dashboards are built to catch the loud failures; the expensive ones are silent and compounding, drifting a little more wrong each cycle until a metric finally turns red long after the cause.

That means your primary detector for the worst class of failure is **not** a monitor. It's a human who notices something is off before they can articulate what — and who is allowed to act on that.

---

## Permission for inarticulate doubt

The most valuable early-warning signal in an agent function is a person saying *"this looks wrong, I can't say why yet."* That sentence is worthless if the culture requires you to justify it before you're allowed to stop. Judgment often arrives as a feeling first and an explanation second; if you gate the stop on the explanation, you lose the window.

So the rule is explicit: **anyone can halt a run on an unarticulated hunch, without pre-justifying it.** The articulation can come after. The stop cannot wait for it.

→ *[Permission for Inarticulate Doubt](https://www.linkedin.com/pulse/permission-inarticulate-doubt-kai-karlstrom-5glue)*

---

## Fund the false alarm

The rule above only holds if stopping a run that turns out fine is a **non-event** — better than that, a thanked event. If a false alarm costs the person who raised it any standing, you've priced the signal out of existence, and you'll only hear about drift once it's red.

**Fund the false alarm.** The person who halts a run that turns out fine made the right call with the information they had. Treat it as the system working, not as a mistake to be corrected. The occasional wasted run is the premium you pay for catching the silent-drift case, and it's cheap.

---

## Blameless because the agent failed, not the person

When an agent produces a bad outcome, the default question in most orgs — *whose fault is this?* — is both wrong and corrosive. Usually the honest answer is that the agent failed and a person is standing near it. Punishing that person does two things, both bad: it makes them hide the next failure, and it makes them shrink the agent's autonomy to cover themselves, killing the leverage.

So blame is routed to where it belongs — the rails, the playbook, the guardrail that let it through — and the leader **absorbs it upward** rather than pushing it down onto the operator ([protection](principles.md)). The review after a failure asks *what in the rails allowed this, and what do we change?* — never *who do we blame?* This is Edmondson's psychological safety and learning-from-failure, applied to a setting where the failing actor is often a machine.

---

## Surfacing beats catching

Because failure is silent, the function optimizes for **surfacing** it early over **catching** it late:

- **Make the stop cheap** — no pre-justification, no standing cost, so doubt gets voiced at the first flicker.
- **Escalate ambiguity to a human by default** — when the system isn't sure, that's a human decision, not an agent guess.
- **Sample the routine runs** — spot-checks on a cadence catch the drift that never triggered an escalation.
- **Review the process, not just the output** — two runs with identical output can differ entirely in how they got there; the lucky run and the clean run look the same until you look at the path. Conformance to the intended process is a signal in its own right.

---

## What "good" looks like

A healthy agent function is not one where nothing ever fails. It's one where:

- failures surface **early and cheaply**, usually from a human hunch, not a red metric;
- the person who surfaces one is **thanked**, whether or not it turned out real;
- the fix lands in the **rails**, so the same failure can't recur;
- and no one is tempted to **hide** a failure or **shrink** an agent to protect themselves.

If those four are true, the silent-failure problem is under management. If any is false, you're accumulating drift you won't see until it's expensive.
