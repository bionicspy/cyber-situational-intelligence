# Personas & Decision Mapping

## Purpose of This Document

This document defines the **human side of the situational intelligence system**.

While other documents describe:
- what signals are collected,
- how they are clustered into situations,
- and how intelligence is derived,

this document answers a different question:

> **Who is this intelligence for, what decisions does it support, and over what time horizon?**

The goal is not to enumerate roles for access control or dashboards.  
The goal is to anchor the system in **real decision‑making contexts across time**.

---

## Why Personas Matter in a Situational Intelligence System

Most security platforms treat users as:
- consumers of alerts, or
- viewers of dashboards.

This system treats users as **decision‑makers operating at different horizons**:

- **Near field** — immediate operational reality  
- **Mid field** — emerging patterns and momentum  
- **Far field** — structural direction and long‑term exposure  

The same situation must look different to:
- a SOC analyst handling an incident **now**,
- a product owner assessing applicability over **weeks**,
- a security architect reconsidering design over **months or years**,
- an executive weighing regulatory and reputational exposure over **strategic timelines**.

If these perspectives are not explicit, systems drift toward:
- one‑size‑fits‑all severity,
- alert overload,
- misaligned prioritization,
- loss of strategic signal.

Personas ensure that **the same truth is interpreted differently, intentionally, and with respect to time**.

---

## What a Persona Is (and Is Not)

A persona in this system is:

- a **decision context**
- a **dominant time horizon (near / mid / far)**
- a **set of questions that must be answered**
- a **tolerance for uncertainty and ambiguity**

A persona is **not**:
- a job title
- a named individual
- a dashboard layout
- a static role

Multiple people may operate within the same persona at different times.  
A single person may occupy **multiple personas depending on situation and horizon**.

---

## How Personas Relate to Collections and Horizons

Collections describe **what questions the system can answer**.

Personas describe:
- **which questions matter**
- **at which horizon**
- **with what urgency and confidence threshold**

Personas do not subscribe to feeds.  
They subscribe to **answers to questions across time horizons**.

---

## SOC / Detection Teams

**Primary Question**  
> *What requires immediate attention right now?*

**Relevant Collections**
- Collection A — Threat Activity & Capability  
  - Surfaces active exploitation, tooling, and attacker behavior
- Collection B — Vulnerability & Exposure  
  - Shows where immediate exposure could align with attacks
- Collection C — Incident & Breach Reality  
  - Confirms whether similar failures are already occurring
- Collection K — Defensive Capability Maturity & Drift  
  - Explains noisy alerts, blind spots, and detection breakdowns

### Time Horizon Framing

**Near Field (Minutes–Days)**  
- Is exploitation active?
- Do I need to act immediately?

**Mid Field (Days–Weeks)**  
- Are alerts part of a campaign or recurring failure?

**Far Field**  
- Low relevance; context only.

**Decision Support Provided**
- Alert prioritization
- Faster escalation clarity
- Reduced alert fatigue

---

## Incident Response & Threat Intelligence

**Primary Question**  
> *What pattern are these events forming, and how is adversary behavior changing?*

**Relevant Collections**
- Collection A — Threat Activity & Capability  
  - Reveals TTPs, tooling, and infrastructure
- Collection C — Incident & Breach Reality  
  - Grounds analysis in confirmed outcomes
- Collection J — Economics & Criminal Market Dynamics  
  - Explains attacker motivation, scale, and persistence

### Time Horizon Framing

**Near Field**  
- Is this credible malicious activity?

**Mid Field**  
- Are coordinated campaigns emerging or shifting?

**Far Field**  
- How is attacker strategy evolving?

**Decision Support Provided**
- Campaign identification
- Attribution support
- Behavior forecasting

---

## Product & Platform Owners

**Primary Question**  
> *Does this apply to what I own, and how urgently should I act?*

**Relevant Collections**
- Collection B — Vulnerability & Exposure  
  - Defines theoretical product exposure
- Collection C — Incident & Breach Reality  
  - Shows whether similar products are failing
- Collection F — Ecosystem & Supply‑Chain Fragility  
  - Highlights dependency and blast‑radius risk
- Collection H — Technology Inflection & Adoption Drift  
  - Reveals emerging exposure due to architectural change

### Time Horizon Framing

**Near Field**  
- Is my product impacted right now?

**Mid Field**  
- Are peers or dependencies failing?

**Far Field**  
- Is my architecture drifting into risk?

**Decision Support Provided**
- Product‑specific urgency
- Remediation scoping
- Design trade‑off clarity

---

## Security Architecture

**Primary Question**  
> *Why do these classes of attacks keep working everywhere?*

**Relevant Collections**
- Collection B — Vulnerability & Exposure  
  - Reveals recurring structural weaknesses
- Collection F — Ecosystem & Supply‑Chain Fragility  
  - Shows systemic dependency failure
- Collection H — Technology Inflection & Adoption Drift  
  - Highlights architectural churn
- Collection K — Defensive Capability Maturity & Drift  
  - Exposes repeated defensive misconfiguration
- Collection M — Emergent Attack Surfaces  
  - Shows domains without mature controls

### Time Horizon Framing

**Near Field**  
- What incidents reveal design flaws?

**Mid Field**  
- Which failure modes repeat system‑wide?

**Far Field**  
- What architectural changes are required?

**Decision Support Provided**
- Structural risk identification
- Control strategy redesign
- Long‑term architecture planning

---

## Security Leadership (CISO / VP Security)

**Primary Question**  
> *What matters most now, and where should attention be focused?*

**Relevant Collections**
- Collection C — Incident & Breach Reality  
  - Anchors urgency in real‑world failure
- Collection D — Regulatory & Policy Change  
  - Defines consequence and obligation
- Collection E — Geopolitical & Strategic Context  
  - Explains shifting threat pressure
- Collection K — Defensive Capability Maturity & Drift  
  - Shows where defenses are weakening
- Collection L — Measurement & Assurance  
  - Calibrates confidence in controls and claims

### Time Horizon Framing

**Near Field**  
- Is this materially urgent?

**Mid Field**  
- Where is risk accumulating?

**Far Field**  
- Is posture aligned with future pressure?

**Decision Support Provided**
- Clear prioritization narratives
- Resource allocation guidance
- Defensible risk communication

---

## Executives & Board

**Primary Question**  
> *What is the business impact and trajectory of this risk?*

**Relevant Collections**
- Collection C — Incident & Breach Reality  
  - Connects cyber events to cost and reputation
- Collection D — Regulatory & Policy Change  
  - Highlights disclosure and liability
- Collection E — Geopolitical & Strategic Context  
  - Frames macro‑level pressure
- Collection G — Narrative, Trust & Information Warfare  
  - Explains perception‑driven escalation

### Time Horizon Framing

**Near Field**  
- Is this a crisis?

**Mid Field**  
- Will this escalate commercially or legally?

**Far Field**  
- Is the risk profile changing permanently?

**Decision Support Provided**
- Governance oversight
- Risk tolerance calibration
- Strategic alignment

---

## Risk, Legal & Governance

**Primary Question**  
> *Where are we exposed to legal, regulatory, or trust failure—and how soon could that exposure materialize?*

**Relevant Collections**
- Collection C — Incident & Breach Reality  
  - Establishes precedent and enforcement triggers
- Collection D — Regulatory, Legal & Policy Change  
  - Defines obligations, deadlines, and enforcement direction
- Collection L — Measurement, Assurance & Trust  
  - Exposes assurance gaps and control theatre
- Collection G — Narrative, Trust & Information Warfare  
  - Forecasts escalation through perception and scrutiny

### Time Horizon Framing

**Near Field**  
- Are disclosure thresholds crossed?
- Is narrative outrunning facts?

**Mid Field**  
- Are assurances aging or contradicted?

**Far Field**  
- Are governance frameworks becoming insufficient?

**Decision Support Provided**
- Compliance posture awareness
- Early disclosure risk warnings
- Strategic governance management

---

## Strategy & Emerging Technology

**Primary Question**  
> *What is becoming important before it is obvious?*

**Relevant Collections**
- Collection E — Geopolitical & Strategic Context  
  - Shows macro‑pressure shifts
- Collection H — Technology Inflection & Adoption Drift  
  - Reveals new attack surfaces forming
- Collection I — Human & Organizational Factors  
  - Highlights latent organizational fragility
- Collection M — Emergent Attack Surfaces  
  - Identifies domains without mature defenses

### Time Horizon Framing

**Near Field**  
- Weak signals worth noting?

**Mid Field**  
- Which trends are solidifying?

**Far Field**  
- What defines the next attack surface?

**Decision Support Provided**
- Long‑term investment guidance
- Strategic positioning
- Anticipatory risk management

---

## Key Design Takeaway

Each persona:
- spans multiple horizons,
- values those horizons differently,
- and requires explanations tuned to time and responsibility.

Without explicit horizon awareness, systems regress into alerting.  
With it, the system becomes a **decision radar**.

---

## Summary

By weaving **time horizon** directly into persona definitions and **annotating collections with decision value**, the system ensures that:

- relevance is contextual, not absolute
- urgency is derived, not assumed
- decisions scale beyond firefighting
- strategic signals are preserved

The system’s value emerges not from *what it knows*,  
but from **who it helps decide, when, and why**.