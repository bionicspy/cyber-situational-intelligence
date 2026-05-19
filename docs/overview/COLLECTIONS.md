# Signal Collections

## Purpose of This Document

This document defines the **signal collections** used by the situational intelligence platform.

Signal collections are **first‑class conceptual constructs**.  
They are not feeds, data sources, or pipelines.

Each collection is defined by a **question it helps answer**, the **types of signals that inform that question**, and **why those signals matter** for situational awareness and decision‑making.

This document answers:

> **What questions does the system know how to ask about the world?**

Detailed persona usage of collections is defined separately in:

> 📄 **./PERSONAS.md**

The system‑level intent and horizon model are defined in:

> 📄 **./OVERVIEW.md**

---

## What a Collection Is (and Is Not)

A signal collection is:

- a **question‑driven lens on reality**
- a way to group signals by *decision relevance*
- an aid to correlation, explanation, and gap analysis

A collection is **not**:

- a topic taxonomy
- a feed list
- a severity category
- an implementation layer

The same signal may appear in multiple collections if it answers different questions in different contexts.

Overlap is **intentional and beneficial**.

---

## Signal Roles (Applied Across All Collections)

Signals within collections play different **roles** in situational understanding.

These roles influence:
- how signals are weighted,
- how they decay,
- and how they are explained to different personas.

### Core Signal Roles

- **Early**  
  Weak, anticipatory indicators  
  (e.g., emerging narratives, early tooling leaks, workforce stress)

- **Confirmatory**  
  Evidence that validates or refutes earlier signals  
  (e.g., exploitation confirmation, breach disclosure)

- **Analytical**  
  Signals that explain *why* something is happening  
  (e.g., economic incentives, campaign analysis)

- **Narrative**  
  Signals that shape perception and response velocity  
  (e.g., media framing, regulatory commentary)

Different personas value roles differently; collections provide the structure to reason about this consistently.

---

## Collection A — Threat Activity & Capability

**Question**  
What adversaries can do and are actively doing right now?

**Signals**
- Active exploitation reports
- Malware families and tooling
- Command‑and‑control infrastructure
- Campaign tracking and TTP evolution
- Offensive tool releases and updates

**Why it matters**
- Establishes immediate operational pressure
- Anchors near‑field situational awareness
- Provides ground truth on attacker capability and intent
- Feeds tactical and operational response decisions

---

## Collection B — Vulnerability & Exposure

**Question**  
What can be broken, under what conditions, and how broadly?

**Signals**
- CVEs and vulnerability records
- Configuration and default‑exposure patterns
- Weaponization indicators (PoCs, scanners)
- Dependency and supply‑chain exposure
- Platform‑specific exposure (cloud, SaaS, identity)

**Why it matters**
- Defines theoretical attack surface
- Explains *where damage is possible*, not whether it has occurred
- Serves as raw material for urgency derivation when paired with other collections
- Surfaces systemic exposure beyond individual products

---

## Collection C — Incident & Breach Reality

**Question**  
What is actually failing in the real world?

**Signals**
- Confirmed breach disclosures
- Credible investigative reporting
- Ransomware victim portals
- Leak indexing (metadata only)
- Post‑incident root cause and dwell‑time analysis

**Why it matters**
- Reveals organizational and control failure
- Shows attacker ROI and targeting preferences
- Leads regulatory, reputational, and executive concern
- Ground‑truths theoretical risk with observed outcomes

---

## Collection D — Regulatory, Legal & Policy Change

**Question**  
What consequences or obligations are about to apply?

**Signals**
- New cyber laws and amendments
- Disclosure and reporting requirements
- Regulatory guidance and consultations
- Enforcement actions and penalties
- Cross‑border data transfer policy

**Why it matters**
- Regulatory change alters risk faster than exploits
- Drives notification, disclosure, and response timelines
- Shapes executive and board‑level priorities
- Determines downstream impact of technical incidents

---

## Collection E — Geopolitical & Strategic Context

**Question**  
Why is pressure changing, and who is likely to be targeted?

**Signals**
- State conflict escalation
- Sanctions and diplomatic actions
- Election cycles and instability
- Energy, telecom, and infrastructure stress
- National cyber posture shifts

**Why it matters**
- Predicts targeting before attacks occur
- Explains changes in adversary motivation
- Informs strategic risk and scenario planning
- Provides far‑field context for mid‑field signals

---

## Collection F — Ecosystem & Supply‑Chain Fragility

**Question**  
Where could systemic failure emerge even without an attacker?

**Signals**
- Critical vendor outages
- Managed service provider compromises
- Open‑source maintainer stress
- License and governance changes
- Cloud region dependencies and constraints

**Why it matters**
- Non‑malicious failure often creates attack opportunity
- Predicts wide blast‑radius events
- Explains broad exploitation of mundane weaknesses
- Supports resilience and dependency planning

---

## Collection G — Narrative, Trust & Information Warfare

**Question**  
How is perception being shaped, distorted, or amplified?

**Signals**
- Disinformation and influence campaigns
- Incident framing and blame narratives
- False or exaggerated breach claims
- Panic amplification across platforms
- Trust erosion patterns

**Why it matters**
- Perception drives executive and regulatory response speed
- Shapes market and public reaction independent of facts
- Escalates or de‑escalates crises
- Explains pressure beyond technical severity

---

## Collection H — Technology Inflection & Adoption Drift

**Question**  
Where is the next attack surface forming?

**Signals**
- Architectural shifts (identity‑first, passwordless)
- AI capability and deployment changes
- Platform default evolution
- Developer ecosystem trends
- Security tooling consolidation

**Why it matters**
- New paradigms become vulnerable before defenses exist
- Low‑volume, high‑leverage signals
- Enables far‑field anticipation
- Informs long‑term architectural decisions

---

## Collection I — Human & Organizational Factors

**Question**  
Where are people weakening the system before technology fails?

**Signals**
- Security workforce shortages or layoffs
- Burnout indicators in SOC and IR teams
- Leadership turnover in IT and security
- Insider risk trend reporting
- Shadow admin and credential misuse patterns

**Why it matters**
- Many breaches correlate with overload and attrition
- Predicts detection failure and long dwell times
- Explains repeated control breakdowns
- Connects technical events to organizational reality

---

## Collection J — Economics & Criminal Market Dynamics

**Question**  
Is cybercrime becoming cheaper, faster, or more profitable?

**Signals**
- Ransom payment and negotiation statistics
- Malware‑as‑a‑service pricing
- Initial access broker activity
- Leak market demand patterns
- Crypto enforcement and seizure actions

**Why it matters**
- Economics shape attacker behavior
- Price drops predict volume spikes
- Enforcement pressure predicts technique pivots
- Explains scale and persistence of attacks

---

## Collection K — Defensive Capability Maturity & Drift

**Question**  
Are defenders getting stronger or weaker as a system?

**Signals**
- SOC tooling consolidation trends
- Detection‑engineering maturity assessments
- Zero trust implementation failures and successes
- Identity governance drift
- Alert fatigue and overload indicators

**Why it matters**
- Attackers adapt to defensive patterns
- Widespread misconfiguration becomes systemic vulnerability
- Explains why generic attacks keep succeeding
- Provides insight beyond single incidents

---

## Collection L — Measurement, Assurance & Trust Signals

**Question**  
Who can be trusted when they say “secure”?

**Signals**
- Audit failures and restatements
- Certification disconnect narratives
- False security claims exposure
- Pen‑testing blind spot reports
- Assurance framework evolution

**Why it matters**
- Many breaches occur in “certified” environments
- Reveals control theatre and over‑confidence
- Critical for executive and regulatory trust calibration
- Informs governance and assurance decisions

---

## Collection M — Emergent, Non‑Traditional Attack Surfaces

**Question**  
What is not treated as cyber yet — but will be?

**Signals**
- Physical–digital convergence (badging, cameras, HVAC)
- Digital identity use beyond IT
- AI training data poisoning
- Model supply‑chain integrity
- OT / IT and sensor network convergence

**Why it matters**
- Crises emerge here before norms exist
- Regulation and defense always lag
- Early visibility provides strategic advantage
- Defines the far‑field radar mission

---

## Summary

Signal collections define the **question space** of the platform.

They ensure that:
- signals are contextualized, not accumulated,
- overlap improves understanding,
- gaps are visible as unanswered questions,
- and AI reasoning aligns with human decisions.

Collections do not replace expertise.  
They provide the structure that makes expertise scale.