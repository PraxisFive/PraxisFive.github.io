# Delivery Model

How PraxisFive staffs and delivers an engagement. The unit of delivery is the **pod**, and a pod is measured in **FTE, not headcount**.

> Established in the [2026-08-05 operating model working session](../meetings/2026-08-05-operating-model-working-session.md). Economics of the pod live in [Economic model](economic-model.md).

---

## The three tiers

| Tier | Composition | Role |
|------|-------------|------|
| **Client Pod** | Employee-weighted core | The engagement team. Client-facing, continuous, owns the outcome. |
| **Expert Pool** | Mixed employee / 1099, **certified** | Deep specialists we know and trust. Pulled in as the engagement needs them. |
| **PX5 Talent Network** | All 1099, as-needed | Elastic capacity. Offshore-weighted. |

**Certification is the gate.** Everyone in the Expert Pool carries a PraxisFive certification — the standard is higher than the PX5 Talent Network's, because these people front the client. The working rule: *if we use a 1099 here, they have to look and behave like an employee.*

**PX5 Talent Network geography.** South America, Eastern Europe, and Canada are the target markets — talent quality is equivalent, cost is materially lower (Canada roughly 30% less, with the time-zone advantage). Whether the strongest offshore engineering talent belongs in the PX5 Talent Network or gets promoted into the Expert Pool is **unresolved** — see [open-questions](../decisions/open-questions.md).

---

## The Client Pod — three roles

The session started from a traditional consulting roster (strategist, project manager, consultant, analyst, SME, architect, data, design, DevOps) and deliberately collapsed it. What survived:

### 1. Engagement Manager
**The engagement manager and the project manager are the same person.** Not a coordination layer — the client interface, the human in the loop, and the decision-maker on sequencing.

This is a different breed from the traditional PM. Technical enough to move credibly between dev, marketing, and sales inside the client. Strong organization and communication. AI-native by habit. The old failure mode — a project manager who moved work between silos without understanding it — is exactly what AI removes.

**Hiring spec:**

| Attribute | Target |
|-----------|--------|
| Source | Agencies, where strong account managers are underpaid |
| Market rate | $40–60K at source; **~$80K** landed, with an AI-native premium |
| Degree | No CS degree required |
| Non-negotiable | **EQ** — how they handle interaction and conflict, and their problem-solving resolution skills |
| Thinking style | **Probabilistic, not deterministic** — give them a theoretical scenario and they can reason to a plausible outcome |
| AI posture | Uses AI every day as a matter of habit. Not chasing an AI certification. |

> The certification-chasers price themselves up and signal the wrong thing. We want native fluency, then take them up a level because they've joined an AI-native firm.

### 2. Technical Analyst
Understands technology and architecture without being an engineer. The translation layer between the business problem and the agentic framework underneath it. Reads as an IT/architecture background — the useful profile is a solid engineering or systems education, not a top-tier CS pedigree.

### 3. Strategist / Domain Expert
Carries the functional and industry depth, and pulls in additional expertise from the Expert Pool or PX5 Talent Network as the engagement demands. Cross-functional by design — the vantage point is deliberately not single-function.

**Plus admin support**, and a live possibility that the **Engagement Manager and Strategist collapse into one role** for the right person — "the engagement strategy project manager."

### 4. A workflow role in the centre — forming

Floated 2026-08-05 (session 2): a fourth role bridging the other three, focused on **workflow** — an industrial engineering plus data background. Explicitly **not a short-term hire**; a role that could join the delivery team over time as volume justifies it.

**Reaffirmed 2026-09-09**, with Xander named in the seat for now: *"You in the center … because you're redesigning work."* The rationale is the firm's own thesis. If AI value comes from redesigning work (see [Positioning](praxis-five-positioning.md)), someone on the pod has to be expert in how the work actually flows.

### The technical project manager

Marc's proposed hire for scoping and the try-and-buy tier. **Fully remote, no travel and expenses** — purely a level-of-effort resource. Understands the technology well enough to scope, not to build.

---

## The fusion framing: Executive · Expert · Engineer

**Lorin, [2026-09-09](../meetings/2026-09-09-website-and-engagement-framework.md).** A play on the **forward-deployed engineer (FDE)** model that the large firms and hyperscalers are now rolling out. PraxisFive keeps the E and triples it:

| Capability | Brings in | Maps to |
|------------|-----------|---------|
| **Executive** | Leadership and executive insight | Engagement Manager / Strategist |
| **Expert** | Functional and domain depth, from the Expert Pool | Strategist / Domain Expert |
| **Engineer** | Developers, data, technology, from the Specialist Pool | Technical Analyst + Specialist Pool |
| *Centre: workflow* | Industrial engineering: how the work actually flows | The forming fourth role above |

*"It's not about three people, it's about a unit of delivery."* The fusion is **how we describe the pod** (it has outward-facing potential, as the answer to "why not just hire an FDE shop?"). The Client Pod roles above are **how we staff it**. Same thing, two vocabularies. Settle which one goes client-facing before the website copy is written.

### A requirement that surfaced: the boardroom-credible technologist

Jesse, 2026-08-21: *"You gotta have somebody who can walk into a boardroom … and go toe to toe with whoever the CIO or the CISO is and give them confidence."* Every pitch needs the Engineer capability **in the room**, not just on the bench. Today that is one person. See [open-questions](../decisions/open-questions.md).

---

## What sits behind the pods

**Specialist Pool** *(the Expert Pool, as drawn on the 2026-08-05 board)*
- Developers — coding
- Engineers — capacity and architecture
- UX
- Data — logical and physical
- Security

> Terminology to settle: Jesse distinguishes "developers" from "engineers"; Marc reads engineers as closer to architects. Same distinction, different words. Worth fixing before it reaches a client.

**Talent Pool — 1099**
- Domain and industry depth
- Cross-functional
- Deep tech · AI · scale

**Continuous Value Realization = observability**, and it sits *outside* the delivery pods rather than inside them.

---

## FTE, not headcount

A pod is not four people. A pod is a **level of effort**, assembled from fractions.

- One **FTE** = one full-time level of effort
- One **mandate** = a defined block of hours
- A pod might be 1.5 or 2.5 FTE — 20% of one person plus a slice of another

This is what makes the model elastic: the same three roles scale up and down inside an engagement without hiring or firing anyone.

---

## The flywheel

Three functions, tightly integrated — described in session as a helix rather than a pipeline:

```
Selling  ⇄  CX / Client Delivery  ⇄  Continuation Services
   ↑                                          │
   └──────────── insight loops back ──────────┘
```

- Delivery insight changes **how we sell**
- Selling insight changes **how we deliver**
- The continuous service surfaces **new opportunities that become new sprints**

They are managed separately because **the economics are separate** — but they are not independent. Things break, new things ship, and the loop is how the firm stays current in a market that moves this fast.

---

## What this looks like today

Four people mapping onto the model, not a hiring plan. Backgrounds are in [Team](team.md).

| Person | Role | Fusion |
|--------|------|--------|
| **Lorin** | Engagement Manager | Executive |
| **Marc** | Technical Analyst; owns CX, observability, the continuous-services back end, and AI FinOps | Engineer |
| **Jesse** | Expert: AI, marketing, GTM engineering | Expert |
| **Xander** | Workflow and data in the centre; builds the firm's data and deliverable tooling. Available until about February 2027. | Centre |

---

**Related:** [Team](team.md) · [Economic model](economic-model.md) · [Engagement architecture](engagement-architecture.md) · [IP and assets](ip-and-assets.md) · [Service offerings](service-offerings.md) · [AI Integrated Operating Model](ai-operating-model.md)
