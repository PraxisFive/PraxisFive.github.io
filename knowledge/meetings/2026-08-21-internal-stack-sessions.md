# 2026-08-21 — The Internal Operating Stack, and the Data Layer

**Type:** Two internal sessions on the same day (not client-facing)
**Participants:** Session A: Lorin Coles, Marc, Jesse, Xander. Session B: Lorin, Jesse, Xander.

**Processed into:** [Tech and partners](../company/tech-and-partners.md) · [Economic model](../company/economic-model.md) · [Team](../company/team.md) · [decision-log 2026-08-21](../decisions/decision-log.md) · [open-questions](../decisions/open-questions.md)

> ⚠️ **Source caveats.**
> - **Speaker labels.** Session A: A = Jesse · B = Xander · C = Lorin · D = Marc. Session B: A = Jesse · B = Xander · C = Lorin.
> - **Recording order:** it's unclear which session came first. Session B cites "what Marc suggested" on the Claude plan and repeats the ~$500/month total, so Session A was probably earlier.
> - **Garbled names:** Jesse's model-tier names are transcription artefacts ("Luna Max", "Sol High"). The data tools "Piper" and "Catch" are unidentifiable, so both are omitted.

---

## Session A: the stack with Marc

### Jesse's seven components of a company operating system

Jesse had these written out. *"Those are the seven things … required to have an operating system for a company."*

| # | Component | Choice | Status |
|---|-----------|--------|--------|
| 1 | **System of record** | **GitHub** | *"GitHub's fine for that."* |
| 2 | **System of relationship (CRM)** | **Attio** (proposed) | *"We can decide later."* Cheap and AI-first, with no year-long commitment. One of Jesse's portcos has adopted it. |
| 3 | **Workspace** | **Google Workspace** | **Decided.** Marc: Microsoft 365 was the only thing in his tech-stack doc that shouldn't be there. Lorin: *"That was the change that we made."* |
| 4 | **Agent runtime** (drafts, monitors, executes under contract) | Model-agnostic | Starting on a Claude Team plan. See below. |
| 5 | **Automation glue** (background triggers) | **n8n** | Marc: *"one of the better ones for workflow management … open source, but you can scale it."* |
| 6 | **Measurement** (baselines, outcome evidence) | Spreadsheets + client systems for now | |
| 7 | **Identity, access & secrets** | Google + GitHub | |

Jesse: all of it is free or close to free. *"Our overhead is like 500 bucks. Crazy."*

### Model spend: start cheap

- **Decision (Marc, agreed by Jesse):** *"Let's start with a cheap team plan on Claude. And if it doesn't work, we can make some adjustments."* The standard seat is **$25**, the premium seat **$125**. Seat allowances can be capped per person, and overage *"goes quick."* Marc: Team-plan data is kept private and isn't used for public model training. Anthropic's is the best team plan, Gemini's is good but tied to NotebookLM, and OpenAI is "a distant third."
- **Marc's cost insight:** *"It's the harness that costs you in the end, not the model"*, meaning how the harness chunks tokens into the transformer and KV cache.
- **Jesse's orchestration pattern** (an AI-native-operations example): a coordinator session hands builds to a worker session and sends the output to a higher-tier session for audit (go/no-go). Anything reworked more than twice escalates to the top tier, which oversees four or five builds at a time and can run overnight. He had been hitting usage limits in three days. Now he can't use a week's allowance, *"and there's no degradation in quality."* Delegation needs **separate sessions**, because within one session the model won't delegate. He next plans to route his Codex seat through OpenCode for more mileage.
- **Xander:** *"We're definitely overpaying for Claude right now"*, at two $100/month seats.

### Client-facing tech follows the client

- **Marc's tech-stack doc is on the Google Drive.** He proposes a **mainstream tier and a supported tier**. Anything anomalous gets priced separately so the client funds it. *"You're not spending money for resources sitting idle."*
- **Cloud notes:** Google is commonly preferred. Oracle is a player. **AWS "comes off cheap"** but charges to move data out, so data-heavy clients pay to leave.
- **Microsoft clients:** a Microsoft-house client gets Azure, with auth through **Entra ID**. Marc agreed: *"Stay in that realm … they won't be uncomfortable with the proposed technology."* **Okta** is the other common identity layer. Both have free developer instances.
- **Agent orchestration:** all three clouds offer it. Lorin met a local Azure specialist who covers companies of our size, and *"there's no reason we cannot use Microsoft for that, especially if there's some kind of a deal."*
- **Client onboarding tooling:** Ansible (AWX / Tower is open source) and Terraform. Marc's advice: *"We should keep it simple"* and pick tools once the first customer's analysis says what's needed.
- **Data tooling:** Informatica, Azure Synapse / Fabric, Databricks (usable on the free tier).
- **Security scanning** for leaked keys: tools exist, and one of Jesse's portcos is a cybersecurity company.

## Session B: data layer, costs, environments

### The lean internal cost line

| Item | Cost (as quoted) |
|------|------------------|
| Claude Team | $25/seat (standard) |
| GitHub | ~$4/user/month |
| Supabase | ~$40/month (Jesse pays ~$50 hosting six projects) |
| Looker Studio | free |
| Attio | ~$35/month for small teams, up to 10 seats (Jesse's read of the pricing page; he'd earlier said ~$79) |

**Total: about $300–500/month all in.** Lorin is also looking for an **AI-native financial system**, possibly to replace QuickBooks. Nothing decided.

### Every client gets a GitHub repo

Jesse: *"Every client gets a GitHub … a single source of truth."* It holds decisions, design, GTM workflows, onboarding, and ingested call notes, all partitioned. Anything built lives decentralized from our machines and stays **agnostic** to whatever the client runs. Our own stack doubles as a **proving ground**, a model of how the client could work.

### Three environments: the unanswered question

Lorin drew experiment/sandbox → **pre-production** (for example, Xander's builds) → **production**. *"It's this to here that I feel like we've been unclear about."* Deferred to Marc.

### Data: when do you actually need a database?

Lorin asked whether data streaming (Kafka / Confluent) removes the need to land data in a structured store. Jesse ran the question through an LLM on screen. Lorin: *"This answered everything."* The rule of thumb:

- **Streaming is about movement, not storage.** A stream with nowhere to land is a river you can't query.
- **Hundreds to tens of thousands of records, one team, periodic questions:** normalize into files (JSON / Parquet) and query them in place with **DuckDB** plus an agent. **No database.** The agent does both the counting (SQL) and the reading (what customers are actually angry about).
- **Live dashboards:** a scheduled sync or webhook into a small Supabase / Postgres database.
- **Many concurrent users and millions of rows:** a real database or warehouse.
- **"If the schema is wrong, no amount of infrastructure fixes it."** Data model before tools.
- Xander added the medallion pattern: bronze (raw) → silver (schema enforced) → gold (derived metrics).

**A quick-hit demo came out of it:** *"Watch us make a thousand of your tickets queryable in an afternoon, with no new software purchase."*

### Other ideas

- **Visualization is required.** Executives won't query Supabase, so use Looker Studio, Databox, Power BI, or a custom front end. When clients need to edit, the edit path matters. It could run back to the source.
- **Client data access is our job to fix.** Lorin: *"It's our job to say, if you want this kind of measurement, you're going to have to get this data, and we have to build a business case."*
- **Onboarding intake:** Jesse proposed a lightweight link, "here's all the stuff we need," that feeds ingestion.
- **Xander:** build a **library of ~1,000 business metrics** with semantic search on a cheap model (Haiku), so a client's name for a metric maps to the standard one. Useful for client scorecards.
- **Jesse:** design-quality skills (Impeccable, "tasty design") run in an **eval loop until the site passes**, to QA the website's front end.

---

**Related:** [Tech and partners](../company/tech-and-partners.md) · [Economic model](../company/economic-model.md) · [Team](../company/team.md) · [2026-08-13 session](2026-08-13-offering-packaging-with-marc.md)
