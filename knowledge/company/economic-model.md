# Economic Model

What PraxisFive needs to be true to make money. These are **targets, not current state** — set deliberately as goals in the [2026-08-05 operating model working session](../meetings/2026-08-05-operating-model-working-session.md).

> The staffing model these numbers price is in [Delivery model](delivery-model.md). The prices themselves are in [Service offerings](service-offerings.md).

---

## The targets

| Level | Target |
|-------|--------|
| **Project gross margin** | **70%** *(raised 2026-08-05 session 2, from ~50%)* |
| **Net profit** | **50%** |
| **Blended bill rate** | **$350/hour average** (working band $280–350) |
| **Book of business per pod** | **$1.5M – $2.5M** annually |

**Worked example.** At 70% gross margin, a $75K engagement must cost **≤$22.5K** to deliver. The earlier target was ≤$35K.

> ⚠️ **This is a material tightening, and it was set by looking it up rather than by modelling delivery.** Marc: *"I looked it up last night… I was more or less right."* 70% gross margin is achievable in services only with heavy reuse and automation; **50% net profit is exceptionally high** for a services business — it leaves roughly 20 points for acquisition cost, commissions, and all overhead. One phrase in the session — *"if it's 70, 35 is what we got to get"* — is ambiguous and may describe something different again.
>
> The prior figures (~50% gross margin, 30% firm EBITDA) came from the same week. **Both cannot be operative.** Reconcile before either is used to price or to model the pod.

**Scaling.** A $5M firm is 2–3 pods. That assumption is only as good as the mix underneath it — one $2.5M project and fifty $50K projects are not the same business, and the average engagement value is still unknown. See open items below.

---

## The rate card

$350/hour is the **blended average**, not a list price. Internally the card runs three tiers — **junior · manager · senior** — and individual rates can sit as low as $150/hour. What matters is that the *average across an engagement* holds at ~$350.

The original working number was $500/hour. It was pulled down to $350 as the more defensible planning assumption. Neither number is client-visible.

**Pricing is effort-based.** Size is driven by how hard the problem is and how much capacity it consumes — not by the client's ARR. The t-shirt sizes are packaging on top of a time-and-materials reality.

---

## The multiple

PraxisFive plans against a **3X** model. MBB firms run at 10–14X. At 3X the business works.

> ⚠️ **Definition needed.** The 3X was invoked without being defined, and a "5 to 1" was floated alongside it in the same exchange. Whether this is revenue-to-cost, revenue-per-head, or something else materially changes the model. Flagged in [open-questions](../decisions/open-questions.md).

Note the distinction from the client-facing **5x minimum ROI** promise in [Service offerings](service-offerings.md) — that is the return *the client* realizes. The 3X is *our* internal efficiency. Don't conflate them.

---

## Where the value actually compounds

The project business gets us in the door. **The Continuous AI Realization Service is the multiplier.**

- Project revenue is the landing motion; recurring revenue is the model
- Sold at **$10K / $20K / $25K monthly**, with the explicit goal that clients land on **Advantage at $25K**
- Sold as **1-year and 3-year subscriptions**, discounted toward the longer term, billed monthly
- Requires a **different team** behind it — the back-end business, owned separately from delivery

This is where firm valuation comes from. A book of project work is worth a multiple of earnings; a book of recurring contracts is worth considerably more.

**Open:** exit terms mid-subscription are undecided.

### Lorin's stated goal: 10 clients who depend on us

**[2026-09-09](../meetings/2026-09-09-website-and-engagement-framework.md):** *"My goal for us is 10 clients at over $100,000 a year contract. I want 1.2 million in gross recurring revenue."* He's explicit that this is a different goal from *"I want to get to $3 million"* in project revenue: *"a very different goal to say that we want 10 clients that depend on us."*

The arithmetic lines up with the service tiers. **10 clients on Essential (~$10K/month) is $1.2M a year.** Moving the same 10 up to Advantage ($25K/month) makes it $3M. This is the most concrete commercial target in the vault, and a candidate input to the **priorities reset** ([open-questions](../decisions/open-questions.md)).

What makes them stay, in Jesse's words: *"You're basically building a company operating system that is partly deterministic and partly AI."* Each proven workflow plugs into the next, and the models keep improving. *"It's limitless."* Lorin's caution: we're not an IT help desk. The infrastructure behind the recurring service still has to be defined.

---

## Reuse is the margin

Templates and frameworks are not just delivery accelerants — they are **the mechanism by which the margin target is reachable at all.** Every artifact built bespoke is margin spent once; every artifact built reusable is margin earned repeatedly.

This is why the IP stance in [IP and assets](ip-and-assets.md) is an economic position, not a legal preference.

---

## Our own overhead

**Target: about $300–500 a month to run the firm's internal stack** (2026-08-21). That's a Claude Team plan on cheap seats, GitHub (~$4/user), Supabase (~$40), a CRM at small-team pricing, free Looker Studio, n8n, and Cloudflare hosting (~$30). Detail in [Tech and partners](tech-and-partners.md). It isn't a margin lever at this scale, but it's part of the story: we run lean on the same approach we sell.

**Services math, the way Lorin needs it** (2026-08-13): offering → **activities → deliverables → hours × expertise**. That's the level of effort per accelerator × segment × size that Marc owes, kept simple enough to price from.

---

## The honest caveat

None of this is expected on day one. The early engagements are explicitly allowed to **break even or lose money** while the use cases and reusable assets get built.

The failure mode being guarded against is the one that doesn't announce itself: **a model clients love that loses money on every delivery.** Getting the unit economics right early is what prevents scaling into that.

---

## Live unknowns

- **Average engagement value.** $250K? $500K? Not yet calculated — and it determines whether the $2.5M pod is realistic.
- **The 3X definition.** See above.
- **Cost of the offshore blend.** PX5 Talent Network rates are directionally known (Canada ~30% below US), not modeled.
- **What the free XS actually costs us** to deliver.

---

**Related:** [Delivery model](delivery-model.md) · [Service offerings](service-offerings.md) · [IP and assets](ip-and-assets.md) · [Engagement architecture](engagement-architecture.md) · [Company overview](company-overview.md)
