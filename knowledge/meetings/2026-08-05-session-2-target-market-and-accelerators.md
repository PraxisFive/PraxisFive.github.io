# 2026-08-05 (session 2) — Target Market, Accelerators, and the Tech Stack

**Type:** Internal working session (not client-facing)
**Participants:** Lorin Coles, Marc; Xander joins briefly (transcribed as "Sandra"); Jesse referenced but not present
**Artifacts:** Six whiteboard photos (two board states) + partial transcript
**Follows:** [session 1 — operating model](2026-08-05-operating-model-working-session.md)

> ⚠️ **Source caveat.** Transcript truncated at ~50K characters and **speaker labels swap repeatedly** — Speakers 1 and 2 trade places several times mid-conversation. Attribution below is inferred from content: **Lorin** owns pricing, alliances, Brian Hankin, "my comfort zone is enterprise"; **Marc** carries the Cisco / Teradata / AppDynamics / UCS / Webex operating history and the anti-free position.

---

## The headline: the target market moved up-market again

Lorin: *"I initially really only wanted to focus here… however, two reasons why I've evolved."*

1. **Brian Hankin has been playing in enterprise**, and so has Lorin.
2. **Enterprise is Lorin's actual comfort zone** — *"So I might as well sell to them."*

### The three segments as now drawn

| # | Segment | Band | Label |
|---|---------|------|-------|
| 1 | PE / VC / family-office **portfolio companies** | **$100–400M** | Growth |
| 2 | **Mid-market** | **$1–3B** | Breakouts |
| 3 | **Enterprise** | **$3B+** | Innovators |

Enterprise profile written on the board: **$3B+ · tech-forward · digital · B2B · complex selling**. Industries across all three: Enterprise B2B · software · AI · manufacturing · tech · consumer goods.

**Marc's counter-argument — cost to serve inverts.** At the enterprise tier you tell the sales story *once* but implement it *ten times*; specialists are deep and capable. At the lower tier one person holds seven jobs, so handholding, and therefore cost, goes up. Lorin's rebuttal: dealing with one person doing seven jobs is simpler than coordinating seven specialists. Neither resolved it — but it's a real cost-to-serve question per tier.

> ⚠️ **This is the third different set of revenue bands in the vault.** See the revenue-band item in [open-questions](../decisions/open-questions.md) — it is now the most consequential open item.

---

## Accelerators — the spine, renamed and packaged

Marc's construct, adopted: **an "accelerator" is a packaged module that plugs into the base service offering at each t-shirt size.**

**Three accelerators, deliberately only three:**

1. **Analysis** — the baseline. *"I don't want to get too hung up if it's a baseline, a diagnostic, an assessment, a benchmark."*
2. **Roadmap / Blueprint**
3. **Execution**

**Only Execution varies by size.** Analysis and Roadmap are constant across XS→XL.

**Why only three** — Lorin's AppDynamics lesson: they shipped a large catalogue, salespeople couldn't explain it, and buyers treated the spec sheets like a menu, cherry-picking parts of each. *"It got really convoluted. Keep it simple."*

### Execution tracks — timings now specified

| Track | Duration | Status |
|-------|----------|--------|
| Quick Strikes | Sprint | **Always delivered** |
| Quick Wins | Sprint | **Always delivered** |
| Critical Priorities | One sprint | **Always delivered** |
| Strategic Plays | ~3 months | Optional / special |
| Transformational Bets | **6 months+** | Optional / special |

**A sprint = up to four weeks**, milestone-gated — *"you can decide to not go forward, but if you prove it, you go to the next one."*

> This **supersedes** the horizons captured in session 1 (hours/days → month-plus) and answers the open question flagged there: "a month and beyond" was indeed too short for a Transformational Bet.

---

## Economics — margin target raised

- **70% gross margin**
- **50% net profit**
- $350 average bill rate confirmed
- Prices confirmed unchanged: XS free · S $75K · M $150K · L $250–350K · XL custom

Marc: *"I looked it up last night… I was more or less right."* The remaining ~20 points cover cost of acquisition, commissions, and overhead.

> ⚠️ **This tightens session 1 materially.** Session 1 set ~50% gross margin (a $75K engagement costing ≤$35K) and 30% firm EBITDA. 70% GM implies a $75K engagement costs **≤$22.5K**, and 50% net profit is exceptionally high for a services business. One phrase — *"if it's 70, 35 is what we got to get"* — is ambiguous and may mean something different again.

---

## Packaged services — the pre-engagement ladder

Outcome-based, fixed-scope entry products, sized by complexity (**novice → intermediate → advanced**):

| Package | Duration |
|---------|----------|
| **First Step** | 2 days (~16 hours) — workshop, whiteboarding |
| **Jump Start / Fast Path** | ~1 month |
| **Right Start** | 90 days |

**The Cisco cautionary tale.** "Expert as a Service" died because it had no defined outcomes — *"it was a money pit."* The fix was outcome-based packaging: novice-tier items were easy, fast, high-volume; complexity escalated the tier and the price.

**Marc is against "free."** *"I'm not a fan of doing anything free… it's really optional."* His preferred frame is **try-and-buy** — the car-dealership "puppy dog close": let them take it for the weekend, because it's hard to give the puppy back. **Always paper it with a $0 statement of work** to protect scope.

Lorin's version of free is narrower: *"We're going to go do something and deliver something in a short period of time, we're just not charging you"* — pick one problem, prove the value, then the next problem is paid.

---

## Deliverables — no more PowerPoint

The single clearest product statement of the session:

> *"I can't just deliver a PowerPoint. We have to deliver a digital something. They have to get something — a digital thumbprint."*

**Clients get AI agents as part of the deliverable.** Praxis Five can host them, or help deploy on-prem. Agents sit inside the client's infrastructure where they have to, and the hosted side is secure enough for the rest — Marc cites Snowflake, Databricks, and Workday as the pattern.

---

## Tech stack and partner strategy

Marc to own "tech as a strategy" and produce the stack.

| Layer | Choice |
|-------|--------|
| Infrastructure / host | **AWS** — *"most mainstream… straightforward to work with as a partner"* |
| Workspace | **Google** |
| Data | **Databricks** on AWS (Spark / SQL) |
| Scale | **NVIDIA** |
| Client-side must-have | **Microsoft 365 / Teams / Copilot** |

**Partners to pursue:** AWS · Google · Microsoft Azure · Anthropic · Databricks · Snowflake · NVIDIA · **Oracle** (Lorin has a close contact; strong in healthcare and increasingly mainstream cloud).

**Why Microsoft is non-negotiable:** *"It's not just they need Excel. It's the way they use Teams and Copilot… they transcribe every meeting in Teams. Just transcription is critical for us."*

Marc's Cisco/Webex experience: their transcription model was poor and needed manual correction, but he built categorisation on top — tagging for GDPR/HIPAA/PII and redacting content from anyone without clearance. That capability is directly reusable.

Tooling aside: Marc prefers **draw.io** (free, large API, he has a scraper app that pushes into it); Lorin uses **Lucidchart**.

---

## Delivery model refinements

- Core trio confirmed: **Engagement Manager (Lorin) · Domain Expert (Jesse) · Tech Lead / Analyst (Marc)**
- **New — a workflow role in the centre.** Lorin floated a "Xander role" bridging the three: industrial engineering plus data background, workflow-focused. Explicitly *not* short-term — a role that could join the delivery team over time.
- **Specialist Pool:** developers (coding) · engineers (capacity / architecture) · UX · Data (logical and physical) · Security
- **Talent Pool (1099):** domain · industry · cross-functional · deep tech · AI · scale
- **Technical project manager** — remote, no travel and expenses, purely level-of-effort. Marc's proposed hire for scoping and the free/try-and-buy tier.
- **Continuous Value Realization = observability**, sitting outside the delivery model.

**Marc's deliverable to build:** a definition of each accelerator, plus level of effort **per customer segment × per t-shirt size**.

---

## Marc's six numbered workstreams

Written on the board as an ordered list:

1. **Solution / Reference / Tech Architecture** — one base foundational model, adapted into **three variants**, one per customer segment
2. **Solution Offering Matrix** — XS→XL, scope of work, $350 rate
3. **GTM / Sales Model** — *"think Pre-Sales FDE"* (forward-deployed engineer)
4. **Delivery / Continuous Value Realization Service**
5. **What tech do we need / license**
6. **Become a partner** — the platform list above

---

## Two frameworks drawn but not yet in the vault

### The rollout maturity ladder — degree of agent-AI automation

| Stage | State | Value |
|-------|-------|-------|
| 1 | Digital worker adds value | **5x** |
| 2 | Batched agent value | **10x** |
| 3 | Autonomous value | **20x+** |

### iVIS — interactive Value Identification Session
An existing Praxis Five method Xander hadn't seen. Run a session with the client, **map value against the risk of getting that value**, and use the resulting 2×2 to identify and sequence projects. Quadrants sketched: game-changer, average, low-hanging fruit, and a high-risk corner. Feeds POC → Pilot → Program. Onboarding sketched at ~16 weeks, with 4-week and 12-week variants.

---

## Standards and reference frameworks name-checked

MECE · OSI 7 layers · ISO · IEEE · Underwriters Laboratories · Malcolm Baldrige · CMMI · Six Sigma Black Belt · Agile · Pragmatic Marketing (trained methodology) · Bain · Value Engineering / ecosystems.io (Chad Quinn). Chain written top-right: **Transformation → 5 mega flows → use case → sub-use case.**

---

## Companies to study

| Company | Read |
|---------|------|
| **Nimble Gravity** | AI and digital engineering consultancy. Found through PE. *"Killing it… they've figured out their delivery model."* Use cases rated strong. *"Like Palantir, but open."* Model from, don't copy. |
| **Workflows.io** | Jesse's find. GTM-only focus. *"Thinking too small"* — but the use-case presentation is good. |
| **Palantir** | The comparator. Karp admired. |
| Clay · Apollo · ClickUp | GTM AI tools. Lorin unconvinced they matter — *"I think that puts us on a wild goose chase."* |

---

## The alliance use case — the strategic prize

Lorin's clearest articulation of where the firm's own IP could break open a market:

Alliance and ecosystem work is inherently cross-functional — the alliance lead is never the dominant function, so data sits across sales, product, and marketing systems, or on someone's desktop. The chronic failure: **you build a plan, assign tasks, and nothing executes.** *"It just dies. And then you're on their ass going, hey, I need this back."*

> *"If we have agents that can go get this stuff and give it to us, we're going to change the entire Alliance partner channel ecosystem landscape."*

**Transcription is the unlock** — every meeting is now transcribed, so the standup itself becomes the data source. *"Just give me the access to that standup so I can feed my system"* — captured, categorised, and turned into accountability.

---

## Positioning language used

- *"We're an outcome-based realization firm"* — note the phrasing drifts again (vault: **outcome realization firm**)
- *"We're AI, but not everything is AI… we're doing AI foundational work, but we're not covering the gamut of what AI does. It's too big."*
- Shared accountability named as the model to drive

---

**Related:** [Ideal client profile](../company/ideal-client-profile.md) · [Economic model](../company/economic-model.md) · [Engagement architecture](../company/engagement-architecture.md) · [Service offerings](../company/service-offerings.md) · [Delivery model](../company/delivery-model.md) · [Tech and partners](../company/tech-and-partners.md)
