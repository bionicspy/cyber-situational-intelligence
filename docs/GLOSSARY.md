# Glossary of Terms

This glossary defines the core terms used throughout the Situational Intelligence Platform documentation.

Terms are defined deliberately and narrowly.  
If two terms appear similar, the distinction is intentional.

---

## A

### Alert
A discrete notification intended to trigger immediate action.

**Important:**  
Alerts are **not** a primary output of this platform.  
Situational intelligence focuses on **situations**, not alerts.

---

### Assumption
A provisional belief held due to absence of contradictory evidence.

Characteristics:
- Explicit
- Time‑bound
- Revisitable
- Subject to decay

Assumptions are tracked, not hidden.

---

## C

### Collection (Signal Collection)
A **question‑driven grouping of signals** that help answer a specific class of question about reality.

Examples:
- Threat Activity & Capability
- Incident & Breach Reality
- Regulatory & Policy Change

Collections are not feed lists or topic taxonomies.

---

### Contradiction
The coexistence of signals that disagree in interpretation or implication.

Contradiction is:
- Preserved
- Surfaced
- Explained

Contradiction is treated as **information**, not as an error.

---

## D

### Data Model
The conceptual structure defining entities, signals, situations, and interpretations.

The model is:
- implementation‑agnostic
- time‑aware
- uncertainty‑preserving

See: `MODEL.md`

---

### Decay
The reduction in relevance or confidence of evidence over time.

Decay:
- is explicit
- differs by signal role
- applies to assumptions and interpretations
- does not erase history

---

## E

### Entity
A stable concept that exists independently of observation.

Examples:
- Vulnerability
- Product
- Organization
- Regulation

Entities:
- do not decay
- do not carry urgency
- are not opinions

---

### Evidence
One or more signals used to support an interpretation.

Evidence may be:
- partial
- contradictory
- incomplete

Evidence does not equal truth.

---

## F

### Far Field
The long‑term horizon (months to years) where structural, systemic, and strategic forces dominate.

Examples:
- geopolitical shifts
- architectural trust erosion
- regulatory trajectory

---

## G

### Governance
The set of constraints, rules, and disciplines that prevent the system from becoming authoritative, biased, or opaque.

Governance ensures:
- trust is explicit
- uncertainty is visible
- reasoning is auditable

See: `GOVERNANCE.md`

---

## H

### Horizon
The temporal context used to interpret relevance.

Defined horizons:
- Near Field
- Mid Field
- Far Field

Horizon is explicit, not inferred.

---

## I

### Identity Resolution
The process of linking multiple signals to the same underlying entity without interpretation or prioritization.

Identity resolution preserves disagreement.

---

### Ingestion
The process of collecting signals into the platform without filtering, interpretation, or judgment.

Ingestion is conservative by design.

See: `INGESTION.md`

---

### Interpretation
An explanation of what a situation means given evidence, time, and uncertainty.

Interpretation:
- explains, not decides
- is revisable
- is persona‑agnostic at its core

---

## M

### Mid Field
The medium‑term horizon (weeks to months) where patterns, trends, and momentum emerge.

Examples:
- campaign evolution
- enforcement likelihood
- organizational stress

---

### Model
See **Data Model**.

---

## N

### Near Field
The short‑term horizon (minutes to days) focused on immediate activity and failure.

Examples:
- exploitation in progress
- confirmed incidents
- operational urgency

---

## P

### Persona
A decision context defined by:
- role
- responsibility
- dominant horizon
- tolerance for uncertainty

Personas affect **framing**, not facts.

See: `PERSONAS.md`

---

### Persona Projection
The process of reframing interpretations to match a persona’s decision needs and horizon.

Persona projection:
- does not change evidence
- does not change truth
- changes emphasis and explanation only

---

## R

### Relevance
The importance of a situation or signal to a specific persona and horizon.

Relevance is:
- contextual
- time‑bound
- persona‑dependent

Relevance is never absolute.

---

## S

### Signal
A time‑stamped, source‑attributed observation or assertion about the world.

Signals:
- may be wrong
- may conflict
- decay over time
- gain meaning through context

---

### Signal Role
The functional role a signal plays in understanding a situation.

Defined roles:
- Early
- Confirmatory
- Analytical
- Narrative

Role affects explanation and decay, not truth.

---

### Situation
A clustered, provisional understanding of an underlying reality derived from multiple signals.

Situations:
- span collections
- evolve over time
- may be wrong
- exist before prioritization

A situation is **not** an alert or an incident.

---

## T

### Temporal Semantics
The application of time‑aware meaning, including:
- decay
- momentum
- horizon alignment

Temporal semantics ensure that time changes interpretation.

---

## U

### Uncertainty
Acknowledged lack of complete knowledge.

Uncertainty is:
- explicit
- preserved
- explained
- never hidden for convenience

---

## W

### Weak Signal
A low‑confidence, early, or indirect indicator that may gain importance over time.

Weak signals:
- are preserved
- are not discarded as noise
- often become decisive in retrospect

---

## Final Notes

- If a term is not defined here, it should not be used casually.
- If two terms appear similar, consult this glossary before merging them.
- Changes to terminology must be reviewed for architectural and governance impact.

> **Situational intelligence depends on disciplined language.  
Ambiguous terms produce ambiguous decisions.**
