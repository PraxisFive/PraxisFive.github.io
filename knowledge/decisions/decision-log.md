# Decision Log

> Entries from 2026-08-05 onward. Earlier records stay in the internal knowledge base.

---

## 2026-09-09 — Revenue-side lane, LLC, shared repo, website on Cloudflare

**Session:** In-person working session
**Participants:** Lorin Coles, Marc, Jesse, Xander
**Source:** [processed transcript](../meetings/2026-09-09-website-and-engagement-framework.md) · *logged 2026-09-25 from the transcript*

### Decision

**1. We lead on the revenue side, not cost and productivity.** Lorin: *"I don't want to be a cost or productivity dealer … We want to be on the revenue generation side of the problem."* Operational-efficiency projects (invoice matching, claims routing) are out of lane for now. Jesse asked for this to be explicit: *"what we do and what we don't do right now."* Captured in [Positioning](../company/praxis-five-positioning.md) and [Service offerings](../company/service-offerings.md).

**2. PraxisFive will be an LLC.** Lorin's answer when Marc set up the GitHub org.

**3. A shared, private team GitHub org exists** (set up by Marc, with all four invited). It holds the website code. The context files go in once they've been cleaned of client material.

**4. Website: Cloudflare hosting, and Daniel's brand site as the visual base**, in the Praxis Plum theme. Everyone agreed. Lorin: *"I don't think we have to argue over this."*

**5. Rollout stance: experts below the surface, not gamified citizen-building.** Jesse argued against both licence sprays and gamified workflow-building. Lorin had proposed gamifying, and conceded: *"That's a really good point."* Treat this as the working position rather than a formal vote.

### Why
Jesse's challenge from the start of the session was that AI consultancies are getting a bad rap and the site needs a sharp, honest story. A sharp story needs a sharp scope. The entity, the repo and the hosting are the practical preconditions for going live.

### Next action
- **Marc:** a generic end-to-end framework for the ~6-week engagement, with a gate and a decision at each step
- **Jesse:** the feature-release case study; the assessment tool, built from Lorin's question bank
- **Lorin:** the question bank (generic plus per persona); website copy with Jesse
- **Xander:** clean the context files and share them to the team repo; get the transcript auto-upload working
- **Lorin / Xander:** PraxisFive email for Marc and Jesse

---

## 2026-08-21 — The internal operating stack

**Sessions:** Two sessions on the same day, one with Marc
**Participants:** Lorin Coles, Marc, Jesse, Xander
**Source:** [processed transcripts](../meetings/2026-08-21-internal-stack-sessions.md) · *logged 2026-09-25 from the transcripts*

### Decision

**1. Google Workspace internally. Microsoft 365 is out of the internal stack.** Marc: M365 was the only item in his stack doc that shouldn't be there. It stays a *client-side* necessity ([Tech and partners](../company/tech-and-partners.md)).

**2. GitHub is the system of record, with a repo per client** for decisions, design, workflows, onboarding and call notes.

**3. Start on a cheap Claude Team plan** ($25 seats) and move up only where usage demands it. Marc: *"Keep it simple to start with."*

**4. n8n is the automation glue.** Supabase and Looker Studio form the lean data and visualization layer. The data-layer rule of thumb (files + DuckDB → Supabase → warehouse, by scale) is in [Tech and partners](../company/tech-and-partners.md).

**5. Target internal overhead: about $300–500 a month** all in.

**6. Client-facing tech follows the client's realm.** A mainstream tier and a supported tier; anything anomalous priced separately so the client funds it. A Microsoft-house client gets Azure and Entra ID.

### Not decided
- **CRM: Attio** was proposed by Jesse (*"we can decide later"*). It **conflicts with an earlier (June 2026) decision that made HubSpot the CRM of record**. See open questions.

### Why
The firm needs its own operating system before it can credibly sell one. Keeping it cheap, modular and agnostic makes it a live demo of the approach (*"a model for how you could be doing things"*) rather than overhead.

---

## 2026-08-13/14 — GTM leads; how offerings get built; not a VAR

**Sessions:** Lorin with Marc (2026-08-13); GTM working session (2026-08-14)
**Participants:** Lorin Coles, Marc, Jesse, Xander; Daniel as guest on the 14th
**Source:** [08-13](../meetings/2026-08-13-offering-packaging-with-marc.md) · [08-14](../meetings/2026-08-14-gtm-mega-flow-working-session.md) · *logged 2026-09-25 from the transcripts*

### Decision

**1. We're not a VAR, and not in the configuration business.** We lead the transformation and sit between the client and their VAR. Strategic IT services are in scope. *(Lorin and Marc, 08-13)*

**2. GTM Activation & Execution is the lead mega flow.** Lorin and Jesse lead it. Lorin also wants to personally lead Strategic & Operational Planning.

**3. Offerings are built by one recipe per mega flow:** framework → about 10 problems ("flows") → at least one proven use case each → S / M / L packages → a value sheet or video. The hierarchy is **mega flow → flow → use case**. GTM is built first ([AI Integrated Operating Model](../company/ai-operating-model.md), [Service offerings](../company/service-offerings.md)).

**4. The GTM buyer is the CRO / Chief Commercial Officer**, because they own every route to market ([Buyer personas](../company/buyer-personas.md)).

**5. AI FinOps / token economics is the first strategic IT service to build** (Marc owns it). *"Let's own the ROI. Let's own this conversation."*

### Why
Field feedback said the mega flows read as abstract. Buyers want tangible offerings. A single repeatable recipe turns the operating model into a catalogue of problems and proven use cases, without breaking the "three accelerators only" rule from 2026-08-05.

### Refines
- [Tech and partners](../company/tech-and-partners.md) "deliberately not chased: GTM tools." We don't *partner with* GTM point tools. We do *use* them, and swap them freely.

### Next action
Lorin restates the draft GTM problem list and sketches assessment → blueprint → execution for GTM. Marc delivers a simplified (≤7-layer) architecture view and fits FinOps to the mega flows.

---

## 2026-08-13 — Brand: the official colour palette is adopted

**Source:** PraxisFive brand guide (colour system)
**Captured in:** [Brand](../company/brand.md)

### Decision

**1. Four primaries with defined roles.** Praxis Plum `#793268` is the signature. Electric Blue `#4267FF` carries energy and technology — CTAs, links, forward motion. Deep Titanium `#24262D` carries authority — text, headers, structure. Ice `#F2F6FA` carries clarity — backgrounds.

**2. Five accents, used sparingly.** Lilac `#B283F1` · Cyan `#00C2D9` · Teal `#20D0B6` · Violet `#6B4CFF` · Magenta `#E23E8C`. Data visualisation and emphasis only — they exist to keep the plum signature distinctive, not to compete with it.

**3. Six neutrals.** Ink `#0E1117` · Charcoal `#24262D` · Slate `#4B5263` · Stone `#E6E9EF` · Cloud `#F2F6FA` · White.

**4. Two gradients** — Praxis Plum → Electric Blue, and Praxis Plum → Deep Titanium.

**5. Tints for backgrounds, shades for text.** Plum runs 90/75/50/25/10 in both directions.

**6. The wordmark is Praxis + Five in two colours** — Praxis in white or Deep Titanium, Five in Electric Blue, with a small letter-spaced descriptor beneath.

### Why
This is the first real *visual* guidance the firm has had. It closes the workstream that the 2026-08-07 brand document left open, and it does so with a genuinely distinctive signature — plum is rare in professional services, which is the point.

### One deliberate departure
Praxis Plum at full strength is too dark to read as **text on Deep Titanium** — roughly 1.6:1. Both decks therefore carry a second token for accent text on dark surfaces: the **plum 50% tint `#BC98B4`**, which reads at about 6.8:1. Full-strength plum remains correct for fills, for rules and bars, and for text on Ice. This is an accessibility accommodation within the palette, not a change to it.

### Supersedes
- The 2026-08-07 entry's item 7 ("a visual identity exists" — navy/blue ramp). Lorin confirmed on 2026-08-07 that the brand document's navy and blue were **arbitrary**, an artefact of how the document was built. That position is now moot.
- The interim magenta `#CE3A7F` house style used in the decks.
- The Berry Plum `#82345F` exploration, run 2026-08-13 against a 10-option colour board.

### Resolves
- *Visual identity — colour.* Type and the logo system remain open.

### Applied to
`00_context/brand.md`, `05_assets/decks/praxis-five-master.js` → `PraxisFive-Operating-Master.pptx` (v3.0, 59 slides), `05_assets/decks/praxis-five-atlas.js` → `PraxisFive-Framework-Atlas.pptx` (v3.0, 39 slides).

### Opens
- Does *AI-native* survive in the lockup descriptor? The guide reads "OUTCOME REALIZATION FIRM"; the vault says "AI-native Outcome Realization firm."
- A fourth positioning line appeared on the guide that matches none of the three canonical lengths.

---

## 2026-08-07 — Brand: the name is PraxisFive, and it has an identity

**Source:** "PraxisFive Name and Brand" (brand story deck, internal & external use)
**Captured in:** [Brand](../company/brand.md)

### Decision

**1. The name is one word — PraxisFive.** Applied across the knowledge base, the skills, and both deck generators. Dated historical records — transcripts and prior log entries — keep the old spelling because they are accurate to when they were written.

**2. The lead tagline is "Ideas. Execution. Outcomes."** Four supporting variants exist for specific moments: *From Intelligence to Impact* (short-form) · *Where AI Becomes Outcomes* (category-defining) · *Turning AI Into Measurable Business Value* (proposals) · *From Strategy to Sustained Value* (continuity).

**3. The name carries the model, not decoration.** *Praxis* — the Greek concept of turning knowledge into disciplined action. *Five* — three distinct meanings: five operating domains, five kinds of value, five journey levels. "It isn't symbolism — it's the shared operating language between us and every client."

**4. The five domains are renamed to shorter canonical forms.** Strategic & Operational Planning · Innovation & Product Development · Ecosystem Orchestration & Governance · GTM Activation & Execution · Infrastructure Enablement & Readiness. Flow 1 drops *Integrated*, flow 2 shortens substantially, flow 4 shortens to *GTM*, flow 5 drops *Collective*.

**5. New framework — five kinds of value.** Every engagement should create all five, each enabling the next: Better Decisions → Better Execution → Better Adoption → Better Performance → Better Outcomes.

**6. New framework — the organizational AI journey.** Emerging → Developing → Proficient → Differentiated → Exponential, engaged through Assess → Partner → Elevate. Each level is a magnitude rather than a step.

**7. A visual identity exists.** Navy and blue palette built around a five-step ramp from `102542` to `3B6FE8`, heavy condensed display headings, blue rules and statement bands.

### Why
This is the first real brand guidance the firm has had, and it is unusually load-bearing: the name encodes the operating model rather than sitting on top of it. Adopting the shorter domain names also removes drift that had accumulated across three working sessions.

### Resolves
- *Mega flow 5 canonical name* — Infrastructure Enablement & Readiness, no "Collective".
- *PraxisFive brand assets* — identity now exists.
- *Firm descriptor, three variants* — "AI-native Outcome Realization firm" confirmed; the other two retired.

### Settled same day (Lorin, 2026-08-07)

**The journey scale.** Emerging → Developing → Proficient → Differentiated → Exponential is **canonical**. Initiate → Accelerate → Optimize → Scale → Transform is retired. Offering size now sizes against levels, and the read is per-domain rather than a single score. Applied across engagement-architecture, service-offerings, positioning, CLAUDE.md, and both decks.

**The colours are arbitrary.** The navy and blue in the brand document are **not a brand decision** — they are whatever the document happened to be built in. They carry no authority, must not be quoted as brand colours, and nothing should be re-skinned to match them. **The visual identity remains genuinely open** and is now the outstanding brand workstream. The decks' magenta house style is equally provisional and claims nothing.

What the document *does* establish visually is structure, and that survives any palette: the five-step ramp device (five, made structural rather than decorative), statement bands, numbered blocks, condensed display headings.

### Next action
Commission or decide the visual identity. Everything verbal is settled; colour, type, and logo are the gap.

---

## 2026-08-05 (session 2) — Target market moves up-market; accelerators; the tech stack

**Session:** Working session with Marc
**Participants:** Lorin Coles, Marc (Xander briefly)
**Source:** [session 2 transcript + boards](../meetings/2026-08-05-session-2-target-market-and-accelerators.md)

### Decision

**1. The target market moves up-market — three segments.** Portfolio companies (PE/VC/family office) **$100–400M** "Growth" · Mid-market **$1–3B** "Breakouts" · Enterprise **$3B+** "Innovators" (tech-forward, digital, B2B, complex selling). Driven by Brian Hankin already operating in enterprise and by enterprise being Lorin's own comfort zone. **Supersedes the $25M–$300M band.**

**2. The spine is packaged as three accelerators** — Analysis · Roadmap/Blueprint · Execution. Each plugs into the base offering per t-shirt size. **Only Execution varies by size.** Three and only three, deliberately — the AppDynamics lesson that a large catalogue becomes an unsellable menu.

**3. Execution track durations set.** A sprint is up to four weeks, milestone-gated. Quick Strikes, Quick Wins, and Critical Priorities are **always delivered**; Strategic Plays (~3 months) and Transformational Bets (6 months+) are optional layers. Supersedes the hours/days → month-plus set from session 1.

**4. Margin targets raised to 70% gross margin / 50% net profit.** Blended rate $350/hr and the XS–XL prices unchanged.

**5. Packaged services ladder adopted** — First Step (2 days / ~16 hrs) · Jump Start or Fast Path (~1 month) · Right Start (90 days). Outcome-based and fixed-scope, tiered novice → intermediate → advanced. Built on the Cisco "Expert as a Service" failure: open-ended expert hours with no defined outcome became a money pit.

**6. "Free" is reframed as try-and-buy**, always papered with a **$0 statement of work**. One problem, real deliverable, short window, no charge — then paid.

**7. Deliverables must be digital, and include AI agents.** *"I can't just deliver a PowerPoint."* Agents run on-prem where they must and hosted where they can; Praxis Five can host or help deploy.

**8. Tech stack set.** AWS for infrastructure · Google for workspace · Databricks on AWS for data · NVIDIA for scale · Microsoft 365/Teams/Copilot as a client-side necessity. Partner list to pursue: AWS · Google · Microsoft · Anthropic · Databricks · Snowflake · NVIDIA · Oracle. Marc owns "tech as a strategy."

**9. Six numbered workstreams assigned to Marc:** solution/reference architecture (three variants, one per segment) · solution offering matrix · GTM & sales model ("think pre-sales FDE") · delivery and continuous value realization · tech and licensing · partner status.

### Why
Session 1 settled how the firm is staffed and what it costs. This session settled **who it is for and what it actually hands over.** The up-market move is a deliberate bet on the founder's existing network and comfort zone rather than on an abstract mid-market thesis — reachability over theoretical fit, consistent with warm intros being the binding channel constraint.

### Conflicts created — read before acting
- **Revenue bands.** Three sets now exist across one week: $25M–$300M (ICP) · $20–200M / $100M–$1B (canvas) · $100–400M / $1–3B / $3B+ (this session). The pricing does not obviously survive the move up-market.
- **Margins.** ~50% gross / 30% EBITDA (session 1) vs 70% gross / 50% net (session 2). Both cannot be operative.
- **Focus industries.** This session named "Enterprise B2B, software, AI, manufacturing, tech, consumer goods" in passing. The documented six are Enterprise B2B Software · AI · Services · FMCG · Packaging · Materials. Manufacturing and tech are new; Services, Packaging, and Materials went unmentioned.

### Next action
Model level of effort per accelerator **× per segment × per t-shirt size** — Marc's deliverable, and the thing that will show whether the up-market move survives contact with the pricing.

---

## 2026-08-05 — Operating model: pods, unit economics, IP retention

**Session:** Operating model working session (whiteboard)
**Participants:** Lorin Coles, Marc, Jesse, Xander
**Source:** [2026-08-05 transcript + whiteboard](../meetings/2026-08-05-operating-model-working-session.md)

### Decision

**1. The delivery unit is the pod, measured in FTE — not headcount.** Three tiers: **Client Pod** (employee-weighted core) · **Expert Pod** (certified, mixed 1099/employee) · **Talent Network** (all 1099, as-needed, offshore-weighted — South America, Eastern Europe, Canada).

**2. The Client Pod is three roles.** **Engagement Manager** (explicitly the *same person* as the project manager) · **Technical Analyst** · **Strategist/Domain Expert**, plus admin support. Collapsed down from a traditional eight-plus-role consulting roster. EM and Strategist may merge for the right person.

**3. EM/PM hiring spec set.** Sourced from agencies at $40–60K · landing **~$80K** with an AI-native premium · no CS degree required · filtered on **EQ and problem-solving**, and on **probabilistic rather than deterministic thinking** · AI-native by daily habit, not by certification.

**4. Economic targets set.** **30% EBITDA** at the firm · **~50% project gross margin** (a $75K engagement costs ≤$35K) · **$350/hour blended average** (down from a $500 working number; internal three-tier rate card) · **$1.5–2.5M book of business per pod** · 2–3 pods for a $5M firm. Explicitly goals, not current state — early engagements may break even or lose money while the asset library is built.

**5. Execution track horizons confirmed and compressed.** Quick Strikes *hours–days* · Quick Wins *days–weeks* · Critical Priorities *weeks (sprints)* · Strategic Plays *~a month* · Transformational Bets *a month and beyond*. Materially shorter than the prior working draft (days → weeks → quarters → multi-quarter → multi-year).

**6. M size repriced to ~$150K** (from the $125–250K band). XL restated as **Custom**, $350K+ indicative.

**7. IP retention is a standing contracting position.** Clients get derivative rights and can operationalize our models internally; **Praxis Five retains the right to reuse its own frameworks with other clients, including direct competitors**, absent an explicit named restriction. Named exclusions are a priced commercial term, not a default. Set at contract, not at renewal.

**8. Client work is built non-bespoke on purpose.** Use cases developed in client work are built to generalize into reusable assets.

**9. The spine is a tool chain, not three documents.** **Value Assessment → Roadmap → Execution Tracks**, integrated so each stage feeds the next.

**10. The Continuous AI Realization Service is the multiplier.** 1-year and 3-year subscriptions, billed monthly, discounted toward the longer term, with the explicit goal of landing clients on **Advantage at $25K/mo**. A separate team sits behind it.

### Why
The positioning and the offer were settled on 2026-08-03; none of the machinery underneath them was. Without a delivery unit there's no way to answer "can we staff this," without unit economics there's no way to know whether the prices work, and without an IP position the framework library — the actual asset — leaks out through standard derivative-rights clauses one engagement at a time.

The compression across execution tracks and the sales cycle is a deliberate expression of the AI-native thesis: baselining that took six weeks takes days, and discovery is largely pre-empted by arriving with a hypothesis already formed from the client's own data.

### Resolves
- Open question *"Execution track thresholds"* — horizons confirmed, with one tension flagged (Transformational Bets at "a month and beyond" reads short for operating-model-level change; may be a minimum rather than a typical).
- Open question *"Offering-size definitions"* — **partially.** M price fixed at ~$150K and pricing confirmed as effort-based. Duration bands, mega flows worked per size, deliverable inventory, and the free XS definition all remain open.

### Next action
Model the average engagement value — $250K vs $500K changes whether a $2.5M pod is achievable, and it's the missing input to nearly everything else in the economic model. Then define the 3X multiple, which was invoked but never defined.
