# Open Questions

Unresolved decisions and forks worth tracking. Move to `decision-log.md` once resolved.

---

## From the Aug 11 – Sep 9 working sessions (opened 2026-09-25)

> Surfaced while processing the Aug–Sep 2026 working sessions. Sources are in Meetings.

### 🔴 CRM: Attio or HubSpot?
An earlier (June 2026) decision made **HubSpot** the CRM and system of record. On 2026-08-21 Jesse proposed **Attio** for the internal stack (AI-first, cheap, no annual commitment). Lorin is enthusiastic (*"I'm so excited about Attio"*), and one of Jesse's portcos has moved to it. Nobody has revisited the HubSpot decision. **Decide before any pipeline or outreach automation is built,** because any pipeline automation syncs into whichever one wins.

### 🟠 Sandbox → staging → production
Lorin, 2026-08-13 and again 2026-08-21: *"How we go from a sandbox environment to production in this AI world … it's this to here that we've been unclear about."* **Marc owes a recommendation.** It governs how anything we build (agents, the assessment tool, client tooling) moves into a client's hands.

### 🟠 Where do the solutions we build live?
Lorin, 2026-08-13: *"Am I becoming a managed-services business for my clients, or am I building solutions they bring in-house?"* Settled: **not a VAR, not configuration** (decision 2026-08-13). Still open: who hosts and runs the agents after an engagement, and how that ties into the Continuous AI Realization Service's back end.

### 🟠 The simplified reference architecture
Lorin wants **at most seven layers** a business buyer can read (hardware · software · services · network, plus data and security). He rejected the vendor "iceberg" diagram. **Marc owns it** as workstream 1. See [Tech and partners](../company/tech-and-partners.md).

### 🟠 Finish the GTM offering, then repeat it four times
The GTM problem list is a **draft** of about 10 items. **Lorin owns the restatement**, plus use cases and an assessment → blueprint → execution sketch. The same recipe then has to run for the other four mega flows. See [AI Integrated Operating Model](../company/ai-operating-model.md).

### 🟠 The assessment question bank, and a workflow-decomposition method
Jesse's assessment tool is **waiting on Lorin's questions**: a generic set plus one per persona, in waterfall order. Separately, Lorin asked whether a **consistent method exists to decompose any workflow** (*"is there a five-step process?"*). Nothing is named yet. See [Engagement architecture](../company/engagement-architecture.md).

### 🟡 Hourglass or bow tie?
The vault calls the GTM shape an **hourglass**. Lorin drew a **bow tie** on 2026-08-14 and credited Winning by Design, who own that term. Pick one word to use externally and say how we differ from Winning by Design (we go further past the transaction).

### 🟡 Client-facing vocabulary for the pod
Two vocabularies now describe the same thing: the **Client Pod** (Engagement Manager · Technical Analyst · Strategist) and the **fusion** (Executive · Expert · Engineer), which Lorin floated on 2026-09-09. Decide which one goes on the website. See [Delivery model](../company/delivery-model.md).

### 🟡 Website: publish pricing? When does stealth end?
Jesse wants a **"how we work & pricing"** section. Lorin wants to stay **in stealth**. Publishing the XS–XL prices is a positioning decision in itself. It also collides with the unresolved revenue-band question above. See [Brand](../company/brand.md).

### 🟡 Internal tooling drift
- The knowledge base's tool registry lists Outlook and Teams as Lorin's tools. The team now runs **Google Workspace + Slack**. Which is canonical for the firm's own email and calendar?
- **Meeting capture:** Fireflies (current) vs **Ergo** (Jesse's pick; it fills CRM fields after a call). Xander (2026-09-09): transcript auto-upload is needed **"ASAP."**
- Lorin is looking for an **AI-native financial system**, possibly replacing QuickBooks.

### 🟡 Referenced work that isn't in the vault
Collect these, or link to them: Marc's **tech-stack** and **FinOps** documents (team Google Drive); Lorin's **"seven AI risks"**; Marc's **"seven human things"**; Jesse's **GTM engineering stack** write-up; the **"no process, no agent"** article; Daniel's brand site code, which holds the typeface name.

---

## PraxisFive — live items (opened 2026-08-03)

### 🔴 Reset current priorities
The prior Q2 2026 priorities — 3 diagnostic pilots, website credibility, 30–50 account outreach by end of August — predate the rebrand and are stale on both brand and scope. **Nothing downstream can be sequenced until these are reset.** Highest-leverage open item.

**Evidence for the reset: what the team actually worked on, Aug 11 – Sep 9** (from the processed transcripts):
1. **The website.** Build underway (Jesse), hosting chosen, visual base agreed. **Copy is the blocker.**
2. **GTM offering package.** Framework, about 10 problems, use cases, S/M/L (Lorin to restate).
3. **The assessment tool.** Jesse has a prototype and is waiting on Lorin's question bank.
4. **The end-to-end ~6-week engagement framework** (Marc drafting).
5. **The feature-release case study** (Jesse), the first real proof story.
6. **The internal stack**, set on 2026-08-21.

Lorin also stated a **commercial North Star: 10 clients at >$100K/year ≈ $1.2M gross recurring revenue** ([Economic model](../company/economic-model.md)). It's a natural anchor for the reset. **Still needs Lorin to set the priorities himself.**

### 🔴 Assessment dimensions per mega flow
The diagnostic isn't buildable until each of the five mega flows has scored dimensions. An earlier framework's 170+ dimensions covered 8 post-contract orgs — that maps to parts of flows 4 and 5 only. Decide what carries and what gets built new.

### 🔴 Average engagement value — the missing input
**Not yet calculated,** and flagged by Lorin himself: *"I haven't done the math."* Is a typical engagement $250K or $500K? This determines whether the $1.5–2.5M book of business per pod is achievable, because one $2.5M project and fifty $50K projects are completely different staffing problems. **Nearly every other number in [economic-model](../company/economic-model.md) is downstream of this one.** *(Raised 2026-08-05.)*

### 🔴 Revenue bands — three conflicting sets in one week
| Source | Bands |
|---|---|
| Documented ICP | $25M–$300M |
| Working canvas | Growth Engine $20–200M · Middle Market $100M–$1B |
| **Session 2 (latest)** | **Portfolio $100–400M · Mid-market $1–3B · Enterprise $3B+** |

Session 2 is the most recent and the most reasoned — Lorin moved up-market deliberately (Brian Hankin's presence in enterprise, plus his own comfort zone). But **the pricing has not moved with it.** A $75K–$350K engagement is a rounding error to a $3B enterprise and reaches a completely different buyer through completely different procurement. Either the prices rise, or the segments narrow, or the offer changes shape.

**Resolve before the lead re-score runs** — it bakes whichever band is chosen into all 367 accounts. *(Raised 2026-08-05; escalated same day.)*

### 🔴 Margin targets — two incompatible sets
Session 1: **~50% gross margin, 30% firm EBITDA** (a $75K engagement costs ≤$35K). Session 2: **70% gross margin, 50% net profit** (the same engagement costs ≤$22.5K). Both were set on the same day. 50% net profit is exceptionally high for a services business; the phrase *"if it's 70, 35 is what we got to get"* suggests the definition may not be settled even within session 2. **Neither figure should be used to price or to model the pod until one wins.** *(Raised 2026-08-05.)*

### 🟠 Focus industries — the list drifted
Session 2 named "Enterprise B2B, software, AI, manufacturing, tech, consumer goods" in passing. The documented six are **Enterprise B2B Software · AI · Services · FMCG · Packaging · Materials**. Manufacturing and tech are new entrants; Services, Packaging, and Materials weren't mentioned. Confirm whether this is a real change or loose talk — it drives the account list. *(Raised 2026-08-05.)*

### 🟠 Cost to serve by segment — unresolved argument
Marc: enterprise means telling the sales story once but implementing ten times, with seven specialists to coordinate; the growth tier means one person doing seven jobs and far more handholding, so **cost to serve rises as you go down-market**. Lorin: one generalist is simpler to deal with than seven specialists. Neither won. This is exactly what Marc's level-of-effort-per-segment model needs to answer. *(Raised 2026-08-05.)*

### ~~🟡 Firm descriptor — three variants in circulation~~
**RESOLVED (2026-08-07):** The brand document is unambiguous — **"PraxisFive is an AI-native Outcome Realization firm."** The Value Realization and Client Realization variants are retired.

### 🟠 Offering-size definitions
Prices are set (XS free / S $75K / M ~$150K / L $250–350K / XL custom). Still undefined: duration bands, how many mega flows are worked in depth per size, deliverable inventory per size, and what specifically constitutes the free XS — **including what the free XS costs us to deliver.**

### 🟠 Continuous AI Realization Service — level definitions
What's included at Essential (~$10K/mo) vs Plus ($20K/mo) vs PraxisFive Advantage ($25K/mo). The $5K gap between Plus and Advantage is narrow and needs a clear differentiating story. Also: minimum term, and whether a prior engagement is a prerequisite. **Mid-subscription exit terms explicitly undecided** — *"they can get out at any time... I haven't thought through that enough."* (2026-08-05.)

### 🟠 Define the "3X"
PraxisFive plans against a **3X** model against MBB's 10–14X — but 3X of what was never stated, and a "5 to 1" was floated in the same exchange. Revenue-to-cost? Revenue-per-head? Materially changes [economic-model](../company/economic-model.md). *(Raised 2026-08-05.)*

### ~~🟡 Execution track horizons — one tension~~
**RESOLVED (2026-08-05, session 2; closed here 2026-09-25):** durations were revised: sprints of up to four weeks for the first three tracks, **~3 months** for Strategic Plays, **6 months+** for Transformational Bets. That removes the "a month and beyond is too short" tension. See [engagement-architecture](../company/engagement-architecture.md).

### 🟡 Offshore talent — Expert Pool or PX5 Talent Network?
Jesse holds that strong offshore engineering talent (his own team is largely non-US) sits in the **PX5 Talent Network**; Lorin pushed back on excluding them from the core team. A blend was floated, nothing settled. Affects the certification standard and the cost model in [delivery-model](../company/delivery-model.md). *(Raised 2026-08-05.)*

### ~~🔴 Two five-level maturity scales — pick one~~
**RESOLVED (Lorin, 2026-08-07):** The brand document's scale wins — **Emerging → Developing → Proficient → Differentiated → Exponential**. Initiate → Accelerate → Optimize → Scale → Transform is retired. Applied across [engagement-architecture](../company/engagement-architecture.md), [service-offerings](../company/service-offerings.md), positioning, CLAUDE.md, and both decks. Offering size now sizes against levels, not stages.

### ~~🟡 Mega flow 5 — canonical name~~
**RESOLVED (2026-08-07):** The brand document settles it — **Infrastructure Enablement & Readiness**, no "Collective". All five domain names were tightened at the same time; see [brand](../company/brand.md).

### 🟡 Dominant mega flow by industry
Which flow tends to be dominant in each of the six focus industries? Likely differs sharply between Enterprise B2B Software and Materials. Shapes outreach and the account hypothesis.

### 🟡 Revenue band across non-software industries
The $25M–$300M working band was calibrated on B2B SaaS. FMCG, Packaging, and Materials have different revenue-per-employee and margin structures. See [assumptions](assumptions.md).

### ~~🔴 Visual identity — colour~~
**RESOLVED (2026-08-13):** The official brand guide landed with a full palette — **Praxis Plum `#793268`** signature, **Electric Blue `#4267FF`** energy, **Deep Titanium `#24262D`** authority, **Ice `#F2F6FA`** clarity, plus five accents, six neutrals, two gradients, and a plum tint/shade ramp. Applied to both decks. The Berry Plum exploration and the earlier magenta house style are retired. See [brand](../company/brand.md).

### 🟠 Visual identity — type and logo system
Colour is settled; the rest of the identity isn't.

- **Typefaces are not specified** anywhere in the guide. The decks run Georgia / Calibri as a working pairing — legible and neutral, but not a decision.
- **Logo system** has a wordmark (Praxis in white/titanium + Five in Electric Blue, descriptor beneath) but no clear-space, minimum-size, mono, or reversed variants.

### 🟡 Descriptor — does "AI-native" survive the lockup?
The brand guide's wordmark descriptor reads **"OUTCOME REALIZATION FIRM."** The vault, the positioning, and the canonical narrative all say **"AI-native Outcome Realization firm."** Dropping *AI-native* from the mark may be deliberate compression — or drift. Decide, because it's the line that goes under the logo everywhere. *(Raised 2026-08-13.)*

### 🟡 A fourth positioning line appeared
The guide carries *"We help organizations realize the full value of AI and technology — turning potential into measurable outcomes that drive growth."* It doesn't match the one-liner, the elevator, or the full narrative in [brand](../company/brand.md). Fold it into the three lengths or retire it. *(Raised 2026-08-13.)*

### 🟡 "PX5" — is it a real abbreviation?
The decks and [delivery-model](../company/delivery-model.md) carry **PX5 Talent Network**, but *PX5* appears nowhere else in the vault and nowhere in the brand guide. Either it's an approved short form and belongs in the brand doc, or the network needs a different name. *(Raised 2026-08-13.)*

---
