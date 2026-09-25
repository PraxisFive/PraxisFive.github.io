# 2026-08-14 — GTM Mega Flow Working Session

**Type:** Internal working session (not client-facing), whiteboard
**Participants:** Lorin Coles, Jesse, Marc, Xander, Daniel (guest contributor)
**Processed into:** [AI Integrated Operating Model](../company/ai-operating-model.md) · [Service offerings](../company/service-offerings.md) · [Buyer personas](../company/buyer-personas.md) · [Tech and partners](../company/tech-and-partners.md) · [Team](../company/team.md) · [Decision log](../decisions/decision-log.md)

> ⚠️ **Source caveats.**
> - **Speaker labels:** A = Jesse · B = Daniel · C = Lorin · D = Xander · E = Marc. The labels are mostly stable, but check the content before quoting anyone.
> - **Transcription artefacts:** "Coles" stands in for "comes" throughout, "Lauren"/"Laura" is Lorin, "Mark" is Marc, and "Practice 5" is PraxisFive.

---

## What this session was

Lorin's goal: take **one** mega flow, GTM Activation & Execution, all the way from framework to a buyable offering. That gives the team a template it can repeat for the other four.

> *"Imagine that I had a book … I've got 20 use cases that we know drive real ROI for clients and we have examples of what we did."*

He wants clients to stop hearing "we're a consulting firm, let's set up a discovery meeting." He wants them to hear a point of view, a specific problem, and proof. *"They're tired of the consultant who takes the watch off their arm and then tells them what time it is."*

---

## The framing Lorin set

**AI is disrupting professional services itself.** Management consulting is knowledge work built on a time-and-materials model, and it is "100% being disrupted." PraxisFive is "pioneering a new way to work": iterate, get parts wrong over the next three to five months, and wait for the fit to "lock."

**The five mega flows, as he described them** (his working names, which differ from the canonical ones):
1. Integrated strategy & operational planning. Strategy, budgets and targets, cascaded to each group and reviewed quarterly with the board. *"Such a manual process … even the best of the best don't do it well."*
2. Innovation. Products, solutions and offerings, where product connects to marketing and sales.
3. Ecosystem orchestration & integration
4. GTM activation & execution. He considered renaming "execution" to "realization," then leaned back to execution. **No rename.**
5. Enabling infrastructure. The IT side, with its own buyers.

**Initial focus: GTM.** Jesse: *"Go to market is probably the lowest hanging fruit because everybody needs more revenue … cost savings is less sexy than more revenue."*

---

## The GTM framework

- **Shape: the bow tie** (Lorin credits Winning by Design, whose name for this is "revenue architecture"). The funnel runs wide into the transaction, narrows, and then widens again after it. *"It doesn't end at the transaction … we're moving to an outcome-based environment."* The vault currently calls this shape an **hourglass**. See open questions.
- **Top, middle and bottom of funnel, plus post-sale** (customer success, onboarding, services, partners who fulfil). *"This whole thing ties to one word … revenue."*
- **Velocity with precision.** Precision comes from using data up front on ICP, buying groups and target accounts. The alternative is lurching from one fix to the next: "the problem is SEO … no, it's AI optimization … no, it's the value prop."
- **Push and pull.** Different markets call for different motions. Coca-Cola is the example of a strong push-pull system: bottlers push the product, branding pulls it.
- **The assessment finds where the bottleneck really is.** *"They may think the problem is here, but the problem was actually here."*
- **Alliances baked in, not bolted on.** *"We're integrating alliances and ecosystems from day one."*
- **Revenue must be repeatable, predictable and durable.** That is how PE and CROs think about revenue, via ARR, the multiple and enterprise value. *"No one cares about sales."*
- **Bonus problem: DNA and wiring.** A transactional culture can't run an outcome-based motion. Marc added a book title: *what got you here won't get you there.*

**The buyer is the CRO or Chief Commercial Officer, because they own all the routes to market.** Not the chief sales officer or the CMO.

Xander asked whether bottom-of-funnel processes are built in isolation from the top. Lorin called it "the question of the day." Marketing owns the top in one system module and sales owns the rest in another, and the tools arrived through separate acquisitions. **PraxisFive is cross-functional by design, and that is the point of difference.**

---

## The GTM problem list (draft, about 10)

Lorin asked Jesse to name problems "at the right level." Lorin counted them aloud as they went, but the count is hard to follow in the transcript. Treat this as the audible draft. **Lorin took the action to restate and refine it.**

| # | Problem | Raised by | Note |
|---|---------|-----------|------|
| 1 | Optimizing against the wrong target | Jesse | |
| 2 | Incentivizing the wrong behavior | Jesse | Compensation models. *"Comp plans are always the wrong behavior."* |
| 3 | No integrated, end-to-end sales and marketing motion | Jesse | |
| 4 | Not integrated with product | Jesse | **Use case: new product feature release.** This is Jesse's workflow. See [Team](../company/team.md). |
| 5 | No single source of truth | Jesse | |
| 6 | No flywheel: the bottom of the funnel doesn't talk to the top | Jesse | |
| 7 | Sales and marketing don't understand each other's metrics | Jesse | *"Passing in the night."* Lorin notes firms have sold on this story alone. |
| 8 | Weak signals of customer dissatisfaction, so churn is caught too late | Lorin / Xander | Customer success split into its own org; NPS as a weak proxy |
| 9 | **Propensity signals for renewals and retention** | Marc | Marc built a predictive-analytics flow for exactly this at Cisco |
| (10) | Low conversion into real qualified pipeline; stalled decisions ("fear of messing up") | Lorin | Raised earlier, before the list was built. Unclear whether it counted. |

**Offering construction, agreed by the room:** explain the space → name about 10 problems → give at least one sample use case per problem (up to five) → package S / M / L → attach a value sheet or video. *"It's that simple, isn't it?"*

**Hierarchy:** mega flow → flow → use case. Lorin: *"I'll call these flows."*

---

## Jesse's GTM engineering stack

Lorin asked what matters to a business person "solely focused on go to market." Jesse walked through his working chain:

**listen** (pick up signals) → **capture** → **normalize** → **enrich** (e.g., Apollo, Ocean.io: who is the buying committee behind an anonymous company visit) → **store** (Supabase) → **score** → **brain** (the LLM, routed across models) → **sequencer** (n8n) → **omnichannel distribution** (Instantly for email, HeyReach for LinkedIn) → **design/build tool** (Lovable, Figma, Replit) → **CRM** (source of truth for deal flow). He added SEO and AI visibility, community (Slack/Discord), paid media, and **call recording** (Ergo, which fills in CRM fields after a meeting and even creates the deal).

- **Cost proof point:** the whole engine runs monthly for *"the cost of four clicks"* on a "network penetration testing" Google ad. That click cost has gone from about **$40 to $150 in a year**. That is the business case against paid media.
- **Modularity is the principle.** No year-long contracts, no lock-in, swap tools per use case. *"What a manufacturer is going to need is going to be different than a CPG or an e-comm company."*
- **Security is where we differentiate.** These tools connect to a client's nervous system (CRM, database). Done carelessly, they put the client's data and reputation at risk. Marc: this is why enterprises refused OpenClaw.

**Lorin's reaction:** this is a *workflow*, not an architecture. It "looks and feels no different than any other days of new software," and he expects consolidation. He named the pattern a **closed-loop listening engine**: listening is only valuable if it ends in prioritization and action. Jesse's addition: *"there's a business outcome tied to this."*

Lorin then asked whether a consistent method exists for decomposing any workflow ("is there a five-step process?"). Jesse's practice is to have the client document the five things they do repeatedly, map each step on a Miro board, and list the decision points under each box. Lorin: *"This is business process reengineering all over again."* **Still open: a named PraxisFive workflow-decomposition method.**

---

## Technology: simplify it for business buyers

Lorin's frustration: *"That's what pisses off business people."* Every week brings new names (Lovable, OpenClaw, open-weight models, Harvey, Sierra) and he can't tell what matters.

- **Rejected:** a vendor "AI stack iceberg" diagram. Marc thinks it was "piped into AI" without being thought through. Its layer 0 put the deployment layer (the cloud hosts) at the top, and the choice of hyperscalers was odd.
- **Wanted:** at most seven layers, on the OSI analogy. *"Hardware, software, services, network. That's it."* Lorin wants to add **data** and probably **security**. **Marc owns a simplified version.**
- **Daniel's metaphor:** a tree and its root system. Data feeds the roots, and fruit grows from what you feed it. Lorin disliked a single tree but warmed to a **forest**, where trees communicate through their roots ("it's agentic in a way"). He also floated singularity and harmony. Nothing adopted.

---

## Marc: the FinOps / token-economics offering

- **Pitch:** run the three accelerators against a client's AI spend. **Analysis:** what is actually being spent and where the hidden costs are. **Blueprint:** where chatbots, LLMs or agentic components belong. **Execution:** put controls in.
- **The control gap:** clients can see overspend, but have no way to throttle, pause or kill-switch it. *"That doesn't exist yet."* Marc is doing technical builds for someone building this, using LiteLLM or RouteLLM (he estimates about 80% of the industry uses a variant) and NVIDIA Dynamo / Run:ai for GPU-level kill switches. It can ship as SaaS or on-prem.
- **Targets:** financial services first (for example, a bank with 10,000+ analysts). *"I know several companies that are literally well out of their realm with their AI spending."*
- **Lorin:** *"Let's own the ROI. Let's own this conversation."* On benchmarks, Xander suggested tying them to existing industry benchmarks.

---

## Market signals mentioned

- **Anthropic and OpenAI both launched formal partner programs** in the past few months, reportedly about $100M and $150M. They are tiered and pay-to-play, which Lorin calls an old-school channel model. IBM reached OpenAI's top ("elite") tier by committing to train about 3,000 people. Lorin, as an alliances veteran, reads this as a significant shift.
- **Buyers want hybrid delivery:** an external team that keeps them ahead, partnered with an internal team that deploys. *"No one does it better than Accenture."*
- *"Winning by Design are the most brilliant thought leaders on revenue architecture."* They are a comparator the firm must be aware of.

---

## Actions

| Owner | Action |
|-------|--------|
| **Lorin** | Restate the ~10 GTM problems. Draft example use cases for each. Sketch the assessment → blueprint → execution track for GTM at high level. |
| **Marc** | Simplified architecture view (≤7 layers) and more context on the FinOps use case, kept high level. |
| **All** | Next working session. Marc proposed Monday or Tuesday; Jesse prefers Monday. |

---

**Related:** [AI Integrated Operating Model](../company/ai-operating-model.md) · [Service offerings](../company/service-offerings.md) · [Tech and partners](../company/tech-and-partners.md) · [Buyer personas](../company/buyer-personas.md) · [Team](../company/team.md) · [2026-08-13 session](2026-08-13-offering-packaging-with-marc.md)
