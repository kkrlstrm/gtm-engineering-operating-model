# The GTM Engineering Operating Model

### How to set up and lead an engineering function whose team's real work is running AI agents.

Most writing about AI agents is about the agents. This is about the **people who run them** — how you structure the team, where the leader stands, who owns an outcome no human directly produced, and how judgment survives when the machine does the reps.

It's written from a GTM engineering function that runs autonomous agents against real revenue across ~35 client workspaces. GTM is where this model was forged, but almost none of it is GTM-specific: it applies to any function where a small number of humans now direct a large amount of agent-executed work.

This repository is the **operating model, not the architecture.** The systems the team runs are documented, at the contract level, in [ai-native-gtm-architecture](https://github.com/kkrlstrm/ai-native-gtm-architecture); the implementations stay private. What's here is the human layer around those systems — the part you can't buy, copy, or prompt your way into.

---

## The premise

For fifty years, knowledge-work leadership ran on **expertise**: the leader knew more, and the team were apprentices. AI dissolved that strand. Every operator now queries the same model the leader does; the expertise is public docs, an API call away.

So the question stops being *how do I manage people who do the work?* and becomes *how do I lead people whose work is directing machines that do the work?* That is a different job, and it changes almost everything about how the function is built:

- The leader's leverage moves **a layer up** — into intent and the playbook the agents run on.
- The thing a leader provisions flips from expertise to **protection**.
- The scarce skill becomes **judgment**, exactly as the machine gets fluent at everything except knowing when it's wrong.
- Accountability has to be **designed in**, because you can't reconstruct a decision no human made after it burns you.

This model is the answer to that job, made concrete.

---

## Who this is for

- **A leader standing up an agent-run function** — the structure, roles, and decision rights to put in place before the first agent ships.
- **A new hire joining one** — the thing you wish every VP of Engineering handed you on day one: how we work, what you own, and why.
- **Anyone evaluating whether a function is ready to run agents in production** — the readiness bar and the failure model that keep it honest.

---

## The model at a glance

| Document | The question it answers |
|---|---|
| [Operating principles](principles.md) | What does this team believe about leading agent work, and why? |
| [Operating the team](operating-the-team.md) | How is the team structured — roles, decision rights, span of control, who owns the outcome? |
| [Failure & doubt](failure-and-doubt.md) | How does the team catch silent failure and respond to it without punishing the people who surface it? |
| [Growing judgment](growing-judgment.md) | How do people develop taste when agents have eaten the entry-level reps it used to grow from? |
| [Build vs. buy vs. hold](build-vs-buy.md) | What does the function build, what does it buy, and what does it hold close as durable advantage? |
| [Production-readiness checklist](readiness-checklist.md) | Is the team — not the code — ready to let this agent run unattended? |
| [The thinking behind it](the-thinking.md) | The essays this model is distilled from. |

---

## How to use it

Read [principles](principles.md) first — everything else is downstream of it. Then [operating the team](operating-the-team.md) for the structure, and the [readiness checklist](readiness-checklist.md) before you let anything run unattended. The rest is reference you'll return to as the function grows.

This is a living model. It tracks a system that's still running and still teaching me things; it will change as that system does.

---

*Part of a portfolio on production architecture for systems built around probabilistic models — see the [portfolio map](https://github.com/kkrlstrm). Maintained by [Kai Karlstrom](https://github.com/kkrlstrm).*
