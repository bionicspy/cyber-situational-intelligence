# Data Model Overview

## Purpose of This Document

This document defines the **conceptual data model** of the Situational Intelligence Platform.

It specifies:
- the core modeling primitives used to represent reality,
- how signals, identities, evidence, and situations relate,
- how time and uncertainty are handled explicitly,
- and the invariants that keep interpretation and decision‑making separate.

This document intentionally avoids:
- physical schemas,
- database‑specific constructs,
- storage formats,
- or implementation details.

Those choices are deferred until **after** the model is stable.

---

## Modeling Philosophy

The model is built around a simple but strict principle:

> **Reality is represented as stable identities observed through evolving evidence, clustered into situations, interpreted over time.**

Key consequences of this philosophy:

- Identities are stable
- Evidence is time‑bound
- Situations are provisional
- Interpretation is layered
- Decisions are external

---

## Core Modeling Primitives

The model consists of four primary constructs:

1. **Entity**
2. **Signal / Observation**
3. **Situation**
4. **Interpretation**

Each serves a distinct purpose and must not be collapsed.

---

## 1. Entity

**Definition**  
An **Entity** represents a stable concept in the world.

Entities answer the question:
> *“What exists independently of our observation?”*

### Characteristics

- Stable over time
- Unique within its domain
- May participate in multiple situations
- Does not decay
- Does not imply urgency or importance

### Examples

- Vulnerability (e.g., a CVE)
- Weakness (e.g., a CWE)
- Product or platform
- Organization
- Adversary group (conceptual, not authoritative)
- Regulation or policy artifact

### Invariants

- An entity’s identity does not change because evidence changes
- Multiple entities may be related, but none inherit urgency
- Entities are not opinions

> **Entities anchor meaning; they do not provide it.**

---

## 2. Signal / Observation

**Definition**  
A **Signal** (or Observation) represents a time‑stamped statement about the world.

Signals answer the question:
> *“What was observed or asserted, by whom, and when?”*

### Characteristics

- Always time‑bound
- Always attributable to a source
- May conflict with other signals
- May be incomplete or uncertain
- Decays in relevance over time

### Examples

- “This exploit is active in the wild”
- “Organization X disclosed a breach”
- “A proof‑of‑concept was published”
- “A regulator proposed new reporting requirements”
- “A ransomware group claimed responsibility”

### Invariants

- Signals are never silently corrected
- Contradictory signals coexist
- Signals do not determine truth on their own
- Signals gain meaning through aggregation and context

> **Signals are evidence, not facts.**

---

## 3. Situation

**Definition**  
A **Situation** represents a **clustered hypothesis** about an underlying reality, derived from multiple signals.

Situations answer the question:
> *“What seems to be happening when all signals are considered together?”*

### Characteristics

- Composed of multiple signals
- Spans one or more collections
- May involve many entities
- Explicitly provisional
- Evolves as new signals arrive

### Examples

- “A mass‑exploitation campaign targeting a specific platform”
- “Emerging regulatory pressure around disclosure timelines”
- “Systemic failure pattern in a vendor ecosystem”
- “Trust erosion driven by repeated security claims failures”

### Invariants

- Situations exist before prioritization
- Situations can be wrong
- Situations can overlap
- Situations are not decisions

> **A situation is a working understanding, not a conclusion.**

---

## 4. Interpretation

**Definition**  
An **Interpretation** is an explanation of what a situation means, given time, uncertainty, and context.

Interpretations answer:
> *“Why does this situation matter, and how should it be understood?”*

### Characteristics

- Persona‑agnostic at the core
- Can be projected differently per persona
- Horizon‑aware (near / mid / far)
- Explicit about uncertainty and confidence

### Invariants

- Interpretation never prescribes actions
- Interpretation preserves disagreement
- Interpretation is explainable and reversible

> **Interpretation informs judgment; it does not replace it.**

---

## Time as a First‑Class Dimension

Time is not metadata.  
Time **changes meaning**.

### Temporal Properties

- Every signal has a timestamp
- Relevance decays differently per signal role
- Momentum (increasing / decreasing relevance) is tracked
- Horizon (near / mid / far) is explicit, not inferred

> **Old certainty is worse than fresh uncertainty.**

---

## Signal Roles in the Model

Signals play different roles within situations:

- **Early** — weak, anticipatory indicators
- **Confirmatory** — evidence that validates or refutes
- **Analytical** — explains causal structure
- **Narrative** — shapes perception and response velocity

Signal role influences:
- weighting,
- decay behavior,
- explanatory emphasis.

Signal role does **not** imply correctness.

---

## Uncertainty and Contradiction

Contradiction is **first‑class** in the model.

The system:
- never collapses conflicting signals prematurely,
- never hides disagreement,
- never forces consensus.

Uncertainty is expressed as:
- confidence bands
- competing interpretations
- conditional explanations

> **Disagreement is information.**

---

## What the Model Explicitly Refuses to Do

The model does **not**:

- assign severity scores
- decide urgency
- rank actors or entities
- automate response decisions
- collapse reality into truth labels

Those are **downstream human responsibilities**.

---

## Relationship to Other Documents

This model underpins:

- 📄 `ARCHITECTURE_OVERVIEW.md` — structural responsibilities
- 📄 `COLLECTIONS.md` — question‑driven organization of signals
- 📄 `PERSONAS.md` — decision context and horizon framing

Implementation details are defined separately:

- 📄 `INGESTION.md`
- 📄 `AI_REASONING.md`
- 📄 `DEPLOYMENT.md`
- 📄 `GOVERNANCE.md`

---

## Final Modeling Principle

> **If a data element cannot be explained as an entity, a signal, a situation, or an interpretation, it does not belong in the system.**

This constraint is intentional.

It keeps the model:
- comprehensible,
- extensible,
- auditable,
- and aligned with human decision‑making.