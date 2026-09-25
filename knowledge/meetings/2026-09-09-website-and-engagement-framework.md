# 2026-09-09 — Website, Client Data Access, and the End-to-End Engagement

**Type:** Internal working session (not client-facing), in person, whiteboard plus screen
**Participants:** Lorin Coles, Marc, Jesse, Xander
**Processed into:** [Engagement architecture](../company/engagement-architecture.md) · [Delivery model](../company/delivery-model.md) · [Positioning](../company/praxis-five-positioning.md) · [Brand](../company/brand.md) · [Economic model](../company/economic-model.md) · [Ideal client profile](../company/ideal-client-profile.md) · [Team](../company/team.md) · [decision-log 2026-09-09](../decisions/decision-log.md)

> ⚠️ **Source caveats.**
> - **Speaker labels:** A = Marc · B = Xander · C = Lorin · D = Jesse. The labels swap in places, so the content is the better guide to who is speaking.
> - **Transcription artefacts:** "Practice five" is PraxisFive, "Cloud Player" is Cloudflare, "Main Point" is Maine Pointe.
> - **Off-topic:** about a third of the recording is personal small talk. It is not summarised.

---

## 1 · Client data access patterns

Marc and Xander worked through how clients get data into and out of client tooling:

- **Headless pull:** issue an API key with an expiry and use bearer tokens, so the client pulls data without an interactive session. Webhooks are push, not pull, and would need the client's own auth.
- **Interactive use:** SSO, or a time-limited signed URL (*"use this URL within the next 30 minutes"*).

---

## 2 · Shared repo and the transcript pipeline

- **Marc set up a private GitHub org and repo** for the four of them and invited everyone (*"It's public, but it's only private to us … for now"*). It holds the website code.
- **Xander will move the context files into it:** AI operating model, brand, buyer personas, company overview, delivery model, economic model, engagement architecture, ICP. First he updates them and **strips client material**. Jesse's caution: *"There's so much stuff, it can't all go on the site."* The master deck was built for internal use.
- **Xander: "We need to get the transcript auto-upload thing working ASAP … I don't want to lose any information."** Marc records sessions through Obsidian's recorder and uses a skill he built for transcripts.
- **Entity:** Marc asked because the GitHub org setup requires it. Lorin: **PraxisFive will be an LLC.**
- **Email:** Marc and Jesse are currently on personal addresses. Lorin: *"We'll make it happen."* They are to get PraxisFive addresses.

---

## 3 · The website

- **Hosting: Cloudflare.** Marc: the most reliable option, with stable year-to-year pricing where cheap hosts creep 30–40% higher. Jesse: about **$30/month**, with good bot protection. WordPress was dismissed as having security holes.
- **Visual base: Daniel's brand site.** It has light/dark modes and plum/blue theme switches. Everyone preferred the **Praxis Plum** theme (*"We own that color"*) and Marc prefers dark mode. Lorin: *"I don't think we have to argue over this. This is perfect."* The earlier green/yellow direction is disliked.
- **The gap is copy, not design.** Jesse: *"I need your help with the messaging really badly."* A colour change is "a five-minute change." Jesse found Daniel's brand material "a little esoteric." Lorin clarified that the "roots" metaphors were Daniel's own business, not PraxisFive's.
- **Site structure, as Lorin listed it:** who we serve (buyers) · value · the offering · how we do it (assessment → blueprint → execution tracks) · stories · who we are.
- **What visitors should see (Xander and Jesse):** a formalized but abstracted view of what we do. For example, a timeline arrow with key value points, or an end-to-end graphic with **progressive disclosure** that you hover over to open each step. It could be told as one story: from *"this has been broken for five years"* all the way to self-updating website and LinkedIn, with the human in the loop marked at each step.
- **Xander's field feedback on the deck:** people *"get a little confused once they actually see the offerings. It's very non-explicit … the mega flows."* They want tangible offerings.

---

## 4 · Positioning: "it ain't working"

Jesse opened this: *"AI consultancies and agencies are starting to get a bad rap … we need to hit that head on."* The room built the point of view together:

- **Bolted on.** Tools added onto processes nobody examined, working from how the job is supposed to be done rather than how it's actually done.
- **Hidden cost.** Marc: token and data-access costs that nobody sees or audits. *"It's all being eyeballed."*
- **Poor rollout.** Lorin: *"Here's Copilot, go play with it"* with no structure behind it. The example discussed was a company that bought huge numbers of Copilot licences and got nothing back: *"a case study for how not to do AI."*
- **No return.** The figures cited were an MIT study and HBR articles, with "14% of CEOs" (Jesse) or "6%" (Lorin) reporting a return. **Needs sources before any of it is used.**
- **Adoption treated as the user's burden.** Jesse: people shouldn't have to learn a new way to do their job. The work should become *"a natural, organic layer underneath it,"* so they handle the three exceptions instead of a hundred repetitions.

**The headline:** *"Dude, it ain't working."* Marc: ***"We're the company that makes it work."*** Lorin: we have a proven way of making it work, and it goes back to **business process reengineering**. You have to redesign the work. Jesse: *"A 15-step process now is a four-step process."*

### Rollout debate: gamify it, or keep experts below the surface?

- **Lorin** would have **gamified** the rollout: people nominate use cases, the firm sets priorities, and bonuses reward high-impact new workflows.
- **Jesse** opposes both gamification and a licence for everyone. Employees should keep doing their jobs while *"the experts are working below the surface."* Citizen-built workflows are worse and pull people away from their work. Every employee can have an AI account, as long as it is partitioned by function.
- **Lorin conceded:** *"That's a really good point."*
- **Marc added the access model:** role-based access (for example, via Active Directory groups), **token allowances per role** enforced through an **AI gateway** (LiteLLM, RouteLLM, TensorRT-LLM), and a per-model choice. Jesse's frame for it was *"what's the blast radius?"*

---

## 5 · Scope: revenue side, not cost and productivity

Jesse gave an example: a logistics company whose 14-step invoice reconciliation takes three weeks and could take five days. Marc: work backwards from the outcome, gate by gate. **Lorin stopped it there:**

> *"I don't want to be a cost or productivity dealer … We want to be on the revenue generation side of the problem … growth and innovation."*

Xander's university claims-process project (claims moved out of email, resolution time down about 80%) got the same answer: *"That's the kind of project I don't want to do."* His supply-chain expert is available if that kind of opportunity comes up, but the lane is GTM, where he and Jesse are strongest.

**Jesse:** *"We should be clear about what we do and what we don't do right now."* If the assessment's top two boxes turn out to be invoice matching, *"that's not our lane right now."* Logged as a decision.

---

## 6 · The engagement: homework → hypothesis → waterfall questions

Marc asked Lorin to write down "my instincts when I first walk in the door" so the tooling can be built around them. What Lorin said:

1. **Homework before any conversation.** *"You can't say, I haven't met with them, so I don't know."*
2. **The 5Cs:** Company · Customer · Collaborators · Competitors · Climate (the market). Together they give the **"Big C" — Context.** This includes looking at competitors' sites. *"There's 105 Cs out there. This is my model."*
3. **Firmographics first:** size, how they make money, whether they are low-margin/high-volume or high-margin.
4. **Leave the homework with a hypothesis and a point of view.** *"I try really hard to say don't be biased. Even though I'm biased."*
5. **Waterfall questions, starting strategic.** Revenue goal, then revenue by segment, product and geography, then profit, margin, sales-team composition and channel mix. Anomalies come only after that. *"If the goal is the channel is 60% of revenue and it's 20%, why is the channel not performing?"* Questions differ by role.
6. **What you are hunting for:** a specific thing that gets their attention or earns a proposal. For example, a bottleneck or missed revenue that ties back to the 5Cs.

**The pre-engagement map Lorin drew.** The five areas sit across two lines. One axis runs **corporate ↔ field**, the other **get-to-market ↔ go-to-market**. **Ideas** sit on the left (*"everything that's possible, connecting out to the network"*) and **outcomes** on the right (*"the customer … and the outcomes they're trying to deliver"*). It mirrors "Ideas. Execution. Outcomes." Only the verbal description is in the vault, not a photo of the board.

**Three customer types, as Lorin described them:**
- **High-growth, PE-backed:** EBITDA drives the multiple and the multiple drives enterprise value. Heavy pressure. Jesse: about **36,000 PE-backed companies** are looking for an exit (unverified).
- **Mid-market:** steady, often family-owned, not growing fast. Looking for the next growth, but wary.
- **Innovative corporates:** reinventing themselves, and after *targeted* growth through TAM, SAM and share of wallet, which is what CROs manage.

**Lorin's commercial goal:** *"10 clients at over $100,000 a year contract. I want 1.2 million in gross recurring revenue."* He calls this "a very different goal" from $3M in project revenue. **The engagement promise:** value in **30 days**, and within six weeks *"something they haven't seen before."* The initial offering is $75K–120K.

### The fusion: Executive · Expert · Engineer

Lorin tied this to the **forward-deployed engineer (FDE)** wave, including Google's partnership announcement with Accenture that week. *"We were ahead of our time."* Play on the E: **Executive, Expert and Engineer, fused into one unit of delivery.**

- **Executive (Lorin):** brings in leadership and executive insight
- **Expert (Jesse):** brings in functional and domain experts, whether deep AI, supply chain or anything else
- **Engineer (Marc):** brings in developers, data and technology
- **In the centre, a workflow and industrial-engineering role (Xander):** *"Because you're redesigning work."* Xander noted that Georgia Tech's ISyE has added AI and operations-research-for-decisions concentrations. Lorin's comment: "systems" here means the business system, as in systems thinking.

*"It's not about three people, it's about a unit of delivery."*

### Continuity: why they stay

Jesse: *"You're basically building a company operating system that is partly deterministic and partly AI."* Small workflows go from 14 steps to 3, then plug into the next workflow, and so on. He walked through his feature-release chain: a change in dev status → notification → rollout across portfolio companies → an agent drafts the website update, blog and LinkedIn post → sales enablement reviews closed-lost deals for that feature. *"That one little thing … it's never ending."*

---

## 7 · Assessment tooling

- **Jesse has started a lightweight assessment tool.** It is interactive, works on mobile, and uses branching logic ("what's your biggest bottleneck … how much is it costing you") to put a dollar figure on each answer. *"You tell me the questions you want, and I'll build you the tool."*
- **Lorin's step one sits a level above Jesse's.** It starts with strategic goal alignment (revenue by segment, product and geography) before any specific bottleneck. He has generic questions plus question sets by persona.

---

## 8 · Comparator: Maine Pointe

Lorin raised Maine Pointe, a supply-chain consultancy with an excellent reputation. They describe themselves as AI-native: *"we didn't add AI to our firm, we built our firm around it."* They have been outcome-based from day one. Their maturity model's level 5 is called **"Unlocked."** Worth reviewing against our Emerging → Exponential scale.

---

## Actions

| Owner | Action |
|-------|--------|
| **Marc** | Draft a **generic end-to-end framework for the ~6-week engagement** from existing docs, with a gate and a decision at each step. Specific offerings, including FinOps, get retrofitted into it. |
| **Jesse** | Write up the **feature-release case study** as a real, showable example. Build the assessment tool from Lorin's questions. Rough out the website structure. |
| **Lorin** | Supply the question bank: generic plus per persona, in waterfall order. Help Jesse with website copy. |
| **Xander** | Update the context files, strip client material, share them to the team repo. Get the transcript auto-upload working. |
| **Lorin / Xander** | Set up PraxisFive email for Marc and Jesse |

---

**Related:** [Engagement architecture](../company/engagement-architecture.md) · [Delivery model](../company/delivery-model.md) · [Positioning](../company/praxis-five-positioning.md) · [Brand](../company/brand.md) · [2026-08-14 GTM session](2026-08-14-gtm-mega-flow-working-session.md)
