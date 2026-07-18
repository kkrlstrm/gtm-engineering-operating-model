# Build vs. buy vs. hold

A leader's decision framework for what an agent function builds itself, what it buys off the shelf, and — the category most frameworks miss — what it **holds close** as durable advantage. Getting this wrong in either direction is expensive: build what you should have bought and you burn the team on undifferentiated plumbing; buy what you should have held and you rent your own moat from a vendor.

---

## The classifying question

Don't start from "can we build it?" — you can build almost anything, which makes it the wrong question. Start from **what kind of workflow is this?**, on two axes:

- **Judgment density** — how much of the value is encoded human judgment vs. mechanical execution?
- **Decay rate** — how fast does this workflow go stale as the domain, models, and providers move?

Those two axes give you three decisions.

```
            high judgment density
                     │
        HOLD CLOSE   │   BUILD & MAINTAIN
     (fast-decaying, │   (slow-decaying,
      high-judgment: │    high-judgment:
      the real moat) │    worth the upkeep)
   ──────────────────┼────────────────────  →  decay rate
                     │
          BUY        │      BUY / THIN-WRAP
     (commodity,     │   (commodity, stable:
      fast-decaying: │    someone else's
      rent it)       │    core competency)
                     │
            low judgment density
```

---

## The three decisions

**HOLD CLOSE — high judgment, fast-decaying.** This is the actual advantage: workflows that encode hard-won judgment and go stale fast enough that a competitor can't just copy last year's version. The value isn't the artifact — it's the **capability that keeps regenerating it.** You build these, you keep them private, and you invest in the people who hold the judgment behind them, because that judgment is the appreciating asset and the artifact is the depreciating one. **Most of a function's leverage lives in this quadrant, and most of the mistakes come from treating it like the others** — publishing it, outsourcing it, or letting the person who holds it walk.

**BUILD & MAINTAIN — high judgment, slow-decaying.** Worth building and worth the ongoing upkeep, because the judgment is real and the workflow is stable enough that maintenance pays off. The standards, the playbooks, the durable internal tooling live here.

**BUY — low judgment, commodity.** Someone else's core competency, where the workflow is mechanical and moves fast enough that maintaining your own version is pure cost. Rent it. Building here is the competency trap dressed up as strategy — you're good at building, so you build the thing you should have paid $50/month for. A thin wrapper to keep it swappable is fine; a from-scratch reimplementation is waste.

---

## Provider portability is a hold-close decision in disguise

A specific, recurring case: the **providers** an agent function depends on (data, enrichment, models) are commodity and fast-moving — clearly "buy." But the *workflow that orchestrates them* is often high-judgment and worth holding. The move is to **hold the workflow and keep the providers swappable** — encode your judgment in configuration and capability abstractions, and treat each provider as a replaceable rung. That way you buy the commodity, hold the moat, and never rebuild the workflow when a provider changes underneath you. Vendor lock-in is what happens when you let a "buy" decision quietly capture a "hold" one.

---

## The comp corollary

If the durable advantage is a fast-decaying, high-judgment capability, then it's carried by **people, not artifacts** — and the firm owns the artifact by IP assignment but not the capability, which appreciates and can walk out the door. That's a retention and compensation problem, not just a build decision: the classifying skill that tells you what to hold close also tells you **whose leverage you can't afford to lose.** Treat the two as the same question.

*(This corollary draws on work-in-progress on compensation when leverage becomes capital; the principle is included, the full argument is forthcoming.)*

---

## How to use this

Run any candidate workflow through the two axes before you decide. Then sanity-check the decision against the trap on each side:

- Tempted to **build**? Confirm it's not a commodity you're building out of competency-trap habit.
- Tempted to **buy**? Confirm you're not renting a high-judgment capability that should be your moat.
- Deciding to **hold close**? Confirm you're also holding the *person* who carries the judgment, not just the file.
