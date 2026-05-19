# Signal Ingestion

## Purpose of This Document

This document defines how signals enter the Situational Intelligence Platform.

It explains:
- what ingestion is responsible for,
- what guarantees ingestion provides,
- what ingestion must *never* do,
- and why ingestion is intentionally conservative.

This document does **not** describe:
- specific feed integrations,
- crawl schedules,
- message formats,
- or transport technologies.

Those are implementation concerns that must conform to the rules here, not define them.

---

## Core Ingestion Principle

> **Ingestion observes reality; it does not interpret it.**

Signal ingestion exists to ensure the platform has **maximum, unbiased visibility** into the environment before any meaning is imposed.

If interpretation happens too early, the system becomes:
- brittle,
- biased,
- and unable to reassess past assumptions.

---

## What Is a Signal?

A **signal** is any externally or internally sourced observation, assertion, or report about the world that may contribute to situational understanding.

Signals are:
- time‑bound,
- source‑attributed,
- context‑specific,
- and potentially incomplete or wrong.

Signals are *inputs*, not truths.

---

## Responsibilities of the Ingestion Layer

The ingestion layer is responsible for:

### 1. Broad Signal Capture

- Accepting diverse signal types from technical, organizational, regulatory, economic, and narrative domains
- Preferring completeness over cleanliness
- Avoiding premature assumptions about relevance

> **If a signal seems unimportant today, it may matter later.**

---

### 2. Provenance Preservation

For every ingested signal, the system must preserve:
- original source
- publication or observation time
- collection time
- delivery channel
- any stated confidence, caveats, or disclaimers

Signals must always be traceable back to their origin.

---

### 3. Temporal Accuracy

- Timestamps must reflect *when the signal was true*, not just when it was ingested
- Known delays, retroactive updates, or corrections must be preserved
- Re‑ingestion must not overwrite historical context

Time is not metadata; it is semantic.

---

### 4. Acceptance of Duplication

The ingestion layer **expects** duplication.

Multiple reports of the same event are:
- evidence of salience,
- opportunities for corroboration,
- and sources of contradiction.

Duplication is resolved later — never here.

---

### 5. Acceptance of Contradiction

Conflicting signals are **first‑class inputs**, not errors.

Examples:
- one source claims active exploitation; another disputes it
- a vendor asserts non‑impact while a breach is reported
- early reporting contradicts later clarification

Ingestion never attempts to reconcile disagreements.

---

## What Ingestion Explicitly Does *Not* Do

To preserve system integrity, ingestion must never:

- Assign severity or priority
- Decide “what matters”
- Filter signals by perceived importance
- Suppress sources due to trust assumptions
- Normalize meaning (only structure, if required)
- Deduplicate events
- Correlate signals across sources
- Infer intent, outcome, or applicability
- Apply persona or horizon logic

> **Any logic that changes meaning belongs downstream.**

---

## Types of Signals Accepted

Signal ingestion is domain‑agnostic by design.

Examples include, but are not limited to:

- Vulnerability disclosures and advisories
- Exploitation and threat activity reports
- Incident and breach reporting
- Regulatory, legal, and policy publications
- Sanctions, geopolitics, and state activity
- Supply‑chain outages and ecosystem stress
- Economics and criminal market indicators
- Media reporting and narrative framing
- Human and organizational stress signals

The ingestion layer does not require signals to be “security‑labeled” to be accepted.

---

## Signal Integrity Invariants

The following invariants apply to all ingestion paths:

- **Nothing is dropped silently**
- **Nothing is corrected without trace**
- **Nothing is enriched with opinion**
- **Nothing is prioritized**
- **Nothing is interpreted**

These invariants are more important than throughput or efficiency.

---

## Relationship to Upstream Sources

Ingestion treats all sources as:

- potentially incomplete
- potentially biased
- potentially delayed
- potentially wrong

This applies equally to:
- authoritative bodies,
- vendors,
- ISACs,
- media outlets,
- or community reporting.

Trust and confidence are applied **later**, never at intake.

---

## Relationship to Downstream Layers

Ingested signals flow directly into:

- 📄 **Normalization & Identity Layer**  
  (for structural comparability without interpretation)

They have no direct interaction with:
- situations
- temporal semantics
- persona handling
- interpretation or explanation

This separation is strict by design.

---

## Failure Modes Ingestion Must Avoid

Historically, signal ingestion fails when it:

- filters too aggressively to reduce “noise”
- enforces early taxonomy
- optimizes for current relevance
- encodes trust assumptions implicitly
- collapses duplicates prematurely

Each of these destroys long‑term situational awareness.

---

## Why This Matters

The majority of strategic failures occur not because:
- signals were unavailable,
- or experts were incompetent,

but because:
- weak signals were filtered out,
- contradictions were smoothed over,
- or relevance was judged too early.

By keeping ingestion simple and conservative, the platform preserves the ability to **reinterpret the past when the future arrives**.

---

## Relationship to Other Documents

This document defines ingestion responsibilities in support of:

- 📄 **ARCHITECTURE_OVERVIEW.md** — layer boundaries
- 📄 **MODEL.md** — signal vs entity vs situation semantics
- 📄 **COLLECTIONS.md** — downstream question grouping
- 📄 **AI_REASONING.md** — interpretation rules

Implementation details appear in:
- 📄 **DEPLOYMENT.md**
- 📄 **GOVERNANCE.md**

---

## Final Ingestion Principle

> **It is always safer to ingest too much and decide later  
> than to decide early and lose the ability to understand.**

Everything downstream depends on this discipline.