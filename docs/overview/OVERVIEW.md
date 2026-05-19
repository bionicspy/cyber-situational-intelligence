# Situational Intelligence Platform — Big Picture

## Why This System Exists

This system is not being built to aggregate feeds, replace existing security tools, or accelerate alerting.

It is being built to provide **situational awareness** across **strategic, operational, and tactical horizons** — with AI performing the heavy lifting required to extract meaning, identify patterns, and tailor relevance to different **decision personas**.

Most security tooling answers:
> “What just happened?”

This system answers:
> **“What matters now, why it matters, and where this is heading — for whom.”**

That final clause is critical.  
Relevance without a decision context is noise.

---

## A Mental Model: Radar, Not a Feed Reader

Think of this system as a **radar**, not a feed reader or dashboard.

A feed shows:
- events in time order
- raw volume
- unweighted severity
- duplicated narratives

A radar shows:
- **distance** (how soon something will matter)
- **direction** (where pressure is moving)
- **velocity** (how fast relevance is increasing)
- **clustering** (related signals forming a situation)

The system is designed to provide **depth perception**, not scrolling awareness.

---

## Near, Mid, and Far Field Awareness

The system intentionally operates across **three horizons** simultaneously.

### Near Field — Immediate Reality (Now → Days)

**What is actively happening or failing**

Examples:
- Exploits in the wild
- Active campaigns
- IOCs and infrastructure
- KEV‑class events
- Confirmed incidents

This horizon supports **operational and tactical personas**:
- SOC
- Incident response
- Crisis leadership

---

### Mid Field — Emerging Conditions (Weeks → Months)

**What is forming, shifting, or accelerating**

Examples:
- Campaign evolution
- Repeated failure patterns
- Regulatory movement
- Sector‑specific targeting shifts
- Exploitation maturity vs exposure

This horizon supports **managerial and governance personas**:
- Product owners
- Security leadership
- Risk and compliance

---

### Far Field — Strategic Direction (Months → Years)

**What will shape risk before it is visible operationally**

Examples:
- Geopolitical shifts
- Technology inflection points
- Ecosystem and supply‑chain fragility
- Narrative momentum
- Structural control erosion

This horizon supports **strategic personas**:
- Executives and boards
- Architecture and engineering leadership
- Strategy and emerging technology roles

Most tools never reach this horizon.  
Most consequential decisions live here.

---

## Personas Are First‑Class

This platform is **persona‑driven by design**.

Signals are not valuable in isolation — they only matter relative to:
- **who is deciding**
- **what decision is being made**
- **over what time horizon**
- **with what tolerance for uncertainty**

The same situation:
- looks urgent to a SOC analyst,
- scoped to applicability for a product owner,
- structural to an architect,
- and reputational to an executive.

This is not a failure of clarity — it is the nature of reality.

### Persona Deep Dive

This document stays at the **big‑picture level**.

A full persona definition — including:
- decision questions,
- horizon emphasis,
- collection relevance,
- and explanation style

is documented separately in:

> 📄 **[`PERSONAS.md`](./PERSONAS.md)**

---

## Signal Collections (Question‑First Model)

The system organizes signals into **orthogonal collections**, each defined by a **question it helps answer**, not by a topic it covers.

This ensures:
- every signal has a purpose,
- multiple collections can describe the same situation,
- overlap improves corroboration rather than confusion,
- AI reasoning aligns to decisions, not ingestion.

Each collection answers *part* of a persona’s question — never the whole story.

??????????

## Signal Collections as First‑Class Concepts

The platform organizes signals into **formal collections**, each defined by a
**decision‑shaping question** it helps answer.

Collections are not data sources or feeds.
They are **orthogonal lenses on reality**, such as:

- adversary activity and capability
- technical exposure and vulnerability
- real‑world incidents and breaches
- regulatory and legal consequences
- geopolitical and economic pressure
- human, organizational, and ecosystem fragility

A single situation may draw from **multiple collections simultaneously**.

Collections do not compete — they **corroborate, constrain, and contextualize**
each other.

Each collection is defined in detail in:

> 📄 **./COLLECTIONS.md**

---

## Signal Roles (Cross‑Cutting Concept)

Signals are not treated equally.

Each signal plays one or more **roles** in situational understanding, regardless of collection.

### Core Signal Roles

- **Early**  
  Weak, anticipatory indicators that something may emerge  
  (e.g., narrative shifts, tooling leaks, workforce stress)

- **Confirmatory**  
  Evidence that validates or refutes earlier signals  
  (e.g., exploitation confirmation, breach disclosure)

- **Analytical**  
  Interpretive signals that explain *why* something is happening  
  (e.g., economic incentives, campaign analysis)

- **Narrative**  
  Signals that shape perception and response velocity  
  (e.g., media framing, regulatory commentary)

Different personas value different signal roles:
- SOCs prioritize confirmatory signals
- Leadership values analytical and confirmatory signals
- Strategy personas rely heavily on early and analytical signals

Signal role influences **weight, decay, and presentation** — not just presence.

---

## Deduplication Philosophy

Deduplication is **semantic**, not syntactic.

The system does not eliminate duplicates because they look similar.  
It determines whether multiple signals describe the **same underlying reality**.

Key principles:
- Preserve disagreement
- Treat contradictions as signals
- Avoid false consensus
- Cluster by **situation**, not by event

For many personas, contradiction is more informative than agreement.

---

## Cross‑Cutting Dimensions (Applied Everywhere)

Every signal, regardless of collection, is interpreted through the same dimensions:

### Time Horizon
- Immediate → Emerging → Structural  
Optimization for “now” alone guarantees strategic blindness.

### Intent vs Outcome
- Intent: espionage, disruption, profit
- Outcome: breach, outage, disclosure

### Agency & Control
- Individual
- Organizational
- Systemic

### Signal Strength
- Weak signals
- Correlated signals
- Authoritative signals

AI is most valuable where humans dismiss weak signals too early.

### Reversibility
- Patchable
- Policy‑locked
- Reputation‑damaging

This dimension matters most to executive and governance personas.

---

## Why This Is Different from Existing Tools

Most tools observe:
> **Actions → Outcomes**

This platform observes:
```
CAUSES ─► CONDITIONS ─► ACTIONS ─► OUTCOMES ─► CONSEQUENCES
│           │            │           │            │
Tech       Human/org     Threats     Breaches     Regulation
Econ       Policy        Campaigns   Disruption   Trust
Geo        Ecosystem                  Data loss    Cost
```
Existing tools optimize **execution**.  
This system optimizes **orientation**.

It does not replace scanners, SIEM, SOAR, or EDR.  
It sits **above and across them**, providing context, direction, and prioritization.

---

## Final Synthesis

When fully realized, the platform provides:

- A shared situational picture across personas
- Horizon‑aware understanding of change
- Early visibility into pressure, not just failure
- Explicit handling of uncertainty and trust
- Explanations aligned to human decision‑making

Most systems tell you **what happened**.  
This system tells you:

> **Where you are, who should care, and what direction matters next.**

That difference is the entire point.