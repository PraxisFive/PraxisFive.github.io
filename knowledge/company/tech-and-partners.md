# Tech Stack and Partner Strategy

What PraxisFive runs on, what it deploys into clients, and which platform partnerships it pursues. **Marc owns this** — "tech as a strategy" was his to produce as at 2026-08-05.

> Established in the [2026-08-05 session 2 working session](../meetings/2026-08-05-session-2-target-market-and-accelerators.md). **Extended 2026-08-21 and 2026-09-09** with the internal operating stack, the data-layer rule of thumb, and the not-a-VAR boundary ([2026-08-21 sessions](../meetings/2026-08-21-internal-stack-sessions.md) · [2026-08-13](../meetings/2026-08-13-offering-packaging-with-marc.md) · [2026-08-14](../meetings/2026-08-14-gtm-mega-flow-working-session.md)). Marc's working tech-stack document lives on the team Google Drive. This file records the decisions, not the full doc.

---

## How we run internally: seven components

**Set 2026-08-21.** Jesse's framing of what a company operating system needs. The target is to run the whole firm for **about $300–500 a month**. The internal stack also doubles as a **proving ground**: a live model of how a client could run. That's pillar 1 of AI-native ([Positioning](praxis-five-positioning.md)).

| # | Component | Choice | Status |
|---|-----------|--------|--------|
| 1 | **System of record** | **GitHub.** Private team org set up 2026-09-09. **Every client gets a repo**: decisions, design, GTM workflows, onboarding, ingested call notes. | Decided |
| 2 | **System of relationship (CRM)** | **Attio**: AI-first, cheap, no annual commitment | ⚠️ **Proposed, not decided**, and conflicts with the 2026-06-25 HubSpot decision. See [open-questions](../decisions/open-questions.md). |
| 3 | **Workspace** | **Google Workspace** | **Decided.** Microsoft 365 was dropped from the *internal* stack. It stays a client-side necessity (below). |
| 4 | **Agent runtime** | Model-agnostic. **Start on a Claude Team plan** at the $25 seat, move up only where usage demands it. | Decided: start cheap, adjust |
| 5 | **Automation glue** | **n8n**: open source and scalable | Decided |
| 6 | **Measurement** | Spreadsheets and client systems for now. **Looker Studio** (free) for visualization. **Supabase** (~$40/month) where a hosted database is needed. | Working |
| 7 | **Identity, access & secrets** | Google + GitHub | Working |

**Also in use:** **Slack** as the team channel (adopted August 2026). **Cloudflare** for the website (~$30/month). See [Brand](brand.md).

**Model spend discipline.** Marc: *"It's the harness that costs you in the end, not the model."* Jesse's pattern cuts usage sharply with no loss of quality: a coordinator session routes work to cheaper worker sessions, a stronger model audits, and anything reworked twice escalates. **Delegation needs separate sessions.**

---

## The boundary: we're not a VAR

**Agreed 2026-08-13 (Lorin and Marc).** Lorin worried that Marc's architecture document put the firm *"in the configuration business … worrying about memory,"* and into fights with CIOs who already have vendors.

- **We don't resell or configure infrastructure.** Marc: *"You don't want to be in the VAR business."*
- **We occupy the space between the client and their VAR** (SHI was the example). We turn the client's existing technical capability into an execution method and help them get the most from the budget.
- **We lead the transformation, not the build-out.** Lorin: *"We're owning the transformation."*
- **Strategic IT services are in.** AI FinOps / token economics is the first ([Service offerings](service-offerings.md)).

Still open: Lorin's broader question, **are we a managed-services business or do clients take solutions in-house?** The not-a-VAR line answers part of it. Where the agents we build end up running is the rest. See below and [open-questions](../decisions/open-questions.md).

---

## Client-facing tech follows the client

Marc's rules (2026-08-21):

- **Stay in the client's realm.** A Microsoft-house client gets Azure and Entra ID, because *"they won't be uncomfortable with the proposed technology."*
- **A mainstream tier and a supported tier.** Anything outside both is **priced separately so the client funds it**. Don't pay for idle resources.
- **Mind AWS egress.** AWS *"comes off cheap,"* but data-heavy clients pay to move data out.
- **Identity:** Entra ID or Okta. Both have free developer instances.
- **Agent orchestration exists on all three clouds.** Use whichever one the client runs.
- **Onboarding tooling:** Ansible (AWX is open source) and Terraform. *"Keep it simple"*, and pick tools once the first analysis shows what's needed.
- **Data platforms in play:** Databricks (a free tier is workable), Azure Synapse / Fabric, Informatica.

### Governing AI access inside a client

Our alternative to *"a thousand Copilot licences"* (2026-09-09):

- **Role-based access**, partitioned by function (e.g., from directory groups), so marketing sees marketing and account teams see their accounts.
- **Token allowances per role**, enforced through an **AI gateway** (LiteLLM, RouteLLM, TensorRT-LLM). Model choice can also vary by role.
- **Frame the risk as blast radius.** How much damage can one account's access do?
- **Experts build below the surface.** Employees keep doing their jobs and handle the exceptions. They aren't asked to build their own workflows. See [Positioning](praxis-five-positioning.md).

---

## The data layer: when do you actually need a database?

**Rule of thumb** (2026-08-21):

| Scale | Answer |
|-------|--------|
| Hundreds to tens of thousands of records, one team, periodic questions | **No database.** Normalize into files (JSON / Parquet) and query them in place with **DuckDB** plus an agent. The agent does the counting in SQL and the reading in text. |
| Dashboards that must update live | A scheduled sync or webhook into a small **Supabase / Postgres** database |
| Many concurrent users, millions of rows | A real database or warehouse |

- **Streaming (Kafka / Confluent) moves data. It doesn't store it.** It feeds a store; it doesn't replace one.
- **"If the schema is wrong, no amount of infrastructure fixes it."** Data model before tools. The medallion pattern (bronze → silver → gold) is the default shape once a warehouse is justified.
- **Executives won't query a database,** so there's always a visualization layer (Looker Studio, Power BI, Databox, or a custom front end).

---

## The simplified reference architecture: wanted

Lorin, 2026-08-14: *"That's what pisses off business people."* A new vendor name every week, and vendor "AI stack" diagrams nobody can read. He wants **at most seven layers**, on the OSI analogy, anchored on **hardware · software · services · network**, adding **data** and probably **security**. **Marc owns it.** It's his workstream 1 (solution / reference architecture) at the right altitude.

Principles agreed along the way:
- **Modularity, no lock-in.** Not to a model, not to a vendor, not to a year-long contract (Jesse, and Lorin in *"violent agreement"*).
- **Business buyers don't want to see how the sausage is made.** Lead with the outcome. Keep the stack diagram for the technical buyer.

---

## The platform and client-side choices (2026-08-05)

| Layer | Choice | Why |
|-------|--------|-----|
| **Infrastructure / host** | **AWS** | The most mainstream, and straightforward to work with as a partner. *"They're a pain, but working with them as a partner is straightforward."* |
| **Workspace** | **Google** | Workspace suite for the firm's own operations. **Confirmed 2026-08-21.** Microsoft 365 is out of the internal stack. |
| **Data** | **Databricks on AWS** | Spark / SQL. Also runs on Azure — portable if a client's tenancy demands it. |
| **Scale / compute** | **NVIDIA** | For workloads that need it. |
| **Client-side integration** | **Microsoft 365 · Teams · Copilot** | Non-negotiable. See below. |
| **Diagramming** | draw.io (free, large API — Marc has a scraper that pushes into it) · Lucidchart (Lorin's) | Unresolved, low stakes. |

**Cost discipline.** Cloud subscriptions were flagged as a live risk: *"you're subscribed to AWS, and the next thing your bill is $10,000."* Becoming a partner is partly a cost strategy, not only a go-to-market one.

---

## Why Microsoft is non-negotiable

Not a preference — a delivery dependency.

> *"It's not just that they need Excel. It's the way they use Teams and the way they use Copilot. They transcribe every meeting in Teams. Just transcription alone is critical for us."*

Every meeting being transcribed means **the meeting itself becomes the data source**. PraxisFive has to be able to connect to Teams and Microsoft 365 to get that input, because that is where the client's own signal now lives.

**Existing capability to reuse.** Marc built exactly this on Cisco's Webex: the native transcription was poor and needed correction, but he layered categorisation on top — tagging content for GDPR, HIPAA, and PII, then automatically redacting or withholding it from anyone without clearance. That pattern is directly portable and is a credible differentiator when handling client transcripts.

---

## Partners to pursue

| Partner | Note |
|---------|------|
| **AWS** | Primary infrastructure partnership |
| **Google** | Workspace and cloud |
| **Microsoft / Azure** | Client-side necessity |
| **Anthropic** | Model provider |
| **Databricks** | Data platform |
| **Snowflake** | Data platform |
| **NVIDIA** | Compute |
| **Oracle** | Lorin has a close contact. Strong in healthcare; Oracle Cloud increasingly mainstream. |

This is workstream 6 of Marc's six. Lorin is opening doors through his network.

---

## Where agents run

Agents are part of what the client keeps — see [Service offerings](service-offerings.md). Deployment follows the pattern the data platforms already established:

- The agentic layer sits **inside the client's infrastructure** where it must (on-prem, in-tenancy)
- The remainder is **secure enough to host** on our side
- Snowflake, Databricks, and Workday are the reference implementations for this split

PraxisFive can host, or help the client bring it on-site. Lorin flagged the hosting operation itself as something he doesn't yet know how to run — an open capability gap.

---

## Deliberately not chased

**Go-to-market AI tools — Clay, Apollo, ClickUp.** Lorin's read: *"I think that puts us on a wild goose chase."* The infrastructure partnerships matter; the GTM point tools don't, at least not yet.

> **Nuance added 2026-08-14.** Jesse's working GTM engine *uses* several of these tools: Apollo and Ocean.io for enrichment, Instantly and HeyReach for outreach, n8n for sequencing, Supabase for storage, and Ergo for call capture. Both positions hold. **We don't partner with GTM point tools, and we do use them, swapping them freely per client.** Lorin expects them to consolidate: *"Why would you buy from 12 vendors when you could buy from one?"* The asset is the workflow, not the tool list.

---

## Companies to model from

| Company | What to take |
|---------|--------------|
| **Nimble Gravity** | AI and digital engineering consultancy, found through PE. *"They've figured out their delivery model."* Use cases rated strong. *"Like Palantir, but open."* **Model from, don't copy** — and don't try to be them. |
| **Workflows.io** | Jesse's find. Go-to-market only, *"thinking too small"* — but the use-case presentation is worth studying. |
| **Palantir** | The comparator for what this category looks like at scale. |
| **Maine Pointe** | A supply-chain consultancy with a strong reputation. It describes itself as AI-native: *"we didn't add AI to our firm, we built our firm around it."* Outcome-based from day one. Its maturity model's level 5 is called **"Unlocked."** Closest in spirit to our own claim, so review it against our Emerging → Exponential scale. *(Lorin, 2026-09-09)* |
| **Winning by Design** | Revenue-architecture thought leaders who own the **bow tie** model. *"The most brilliant thought leaders on revenue architecture."* The comparator for the GTM framework. Know it well, and be explicit about where we go further (past the transaction). *(Lorin, 2026-08-14)* |

---

## Market signals worth tracking

As reported in session. **Not independently verified.** Check before quoting externally.

- **AI labs now run formal, tiered partner programs.** Anthropic launched first and OpenAI followed, reportedly about $100–150M each. They're pay-to-play with credential tiers, which Lorin calls an old-school channel model. IBM reached OpenAI's top tier by committing to train about 3,000 people. **This matters to us:** Anthropic is already on our partner list, and tier status may decide who gets access to their enterprise accounts. *(2026-08-14)*
- **Forward-deployed engineering is going mainstream** through hyperscaler and big-firm partnerships (a Google–Accenture announcement in the week of 2026-09-09). It's the context for our Executive · Expert · Engineer fusion ([Delivery model](delivery-model.md)).
- **"Headless CRM":** AI interfaces in front of the CRM of record, and meeting notes becoming a record in their own right. *(2026-08-11, 2026-08-21)*
- **Token economics / AI FinOps is becoming a category.** Budgets are being blown in weeks. That's the opening for our FinOps offering.
- **Regulated buyers need indemnification.** Banks won't adopt open-source or open-weight components without it, so enterprise-supported distributions matter (e.g., NVIDIA AI Enterprise). Marc also said US bank model-risk guidance (SR 11-7) has been replaced by newer guidance. **Unverified.** Confirm before using it with a financial-services buyer. *(2026-09-09)*
- **Daniel's local-AI ventures** (own-your-data infrastructure) are a potential partner. Marc to review. *(2026-08-11)*

---

**Related:** [Service offerings](service-offerings.md) · [Delivery model](delivery-model.md) · [Positioning](praxis-five-positioning.md) · [IP and assets](ip-and-assets.md) · [Team](team.md)
