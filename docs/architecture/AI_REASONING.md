# AI Reasoning & Interpretation

## Purpose of This Document

This document describes **how artificial intelligence is used** within the Situational Intelligence Platform.

It explains:
- what kinds of reasoning AI performs,
- where that reasoning fits in the overall architecture,
- how uncertainty and contradiction are handled,
- and what AI is *explicitly not allowed to do*.

This document does **not** describe:
- specific models or vendors,
- training pipelines,
- prompt engineering,
- or infrastructure implementation.

Those choices are intentionally deferred.

---

## Core Principle

> **AI exists to explain reality, not to replace judgment.**

The platform uses AI to:
- reduce cognitive load,
- expose patterns humans miss,
- and articulate meaning across large, heterogeneous signal sets.

It does **not** use AI to:
- decide priority,
- automate response,
- or declare truth.

---

## Where AI Operates in the Architecture

AI reasoning occurs primarily in two architectural layers:

1. **Interpretation & Explanation Layer**
2. **Persona Projection Support (non‑authoritative)**

AI never operates in:
- Signal Intake
- Normalization & Identity
- Situation Formation
- Governance or control logic

This strict placement prevents early bias and silent decision‑making.

---

## Types of Reasoning Performed

The AI performs **interpretive reasoning**, not predictive or prescriptive reasoning.

### 1. Pattern & Context Identification

AI helps identify:
- relationships across signals and collections,
- recurring motifs and failure patterns,
- correlations that are difficult to see manually.

This reasoning:
- spans technical and non‑technical domains,
- respects provenance,
- and preserves disagreement.

---

### 2. Signal Role Attribution

Signals play different roles in understanding a situation.

AI assists in identifying:
- **Early signals** — weak, anticipatory indicators
- **Confirmatory signals** — evidence validating or refuting hypotheses
- **Analytical signals** — explaining causality or structure
- **Narrative signals** — shaping perception and reaction velocity

Signal role informs **explanation emphasis**, never truth or priority.

---

### 3. Temporal Interpretation

AI reasons explicitly about **time**:

- distinguishing near, mid, and far horizons,
- identifying acceleration or fading relevance,
- explaining why something matters *now* versus *later*.

AI is prohibited from:
- collapsing horizons,
- assuming recency equals importance,
- or discarding older signals automatically.

---

### 4. Situation Explanation

AI assembles explanations that answer:

> *“Given everything observed, what does this situation appear to represent?”*

These explanations:
- integrate multiple collections,
- acknowledge gaps and uncertainty,
- highlight conflicting evidence where present,
- remain revisable as new signals arrive.

> **Explanations are hypotheses, not conclusions.**

---

## Handling Uncertainty and Contradiction

Uncertainty is not a failure state.  
It is an **explicit output**.

### Contradictory Evidence

When signals conflict, AI must:
- surface the contradiction,
- explain why disagreement exists,
- avoid forcing resolution.

Examples:
- vendor assurance vs breach evidence,
- exploit claims without confirmation,
- regulatory interpretation disputes.

Contradictions are treated as **signals themselves**.

---

### Confidence Expression

AI expresses confidence qualitatively, not numerically:

- explains why confidence is high, moderate, or low,
- identifies which assumptions drive uncertainty,
- indicates what evidence would reduce ambiguity.

False precision is avoided deliberately.

---

## Persona‑Aware Interpretation (Without Persona‑Specific Truth)

AI supports persona projection **without changing reality**.

This means:
- same underlying situation,
- same evidence,
- same explanation core,

but with:
- different emphasis,
- different framing,
- different horizon alignment.

> **Persona changes relevance, not facts.**

Detailed persona handling is defined in:
- 📄 `PERSONAS.md`

---

## What AI Is Explicitly Not Allowed to Do

To maintain trust and auditability, AI must never:

- assign severity or priority scores
- recommend specific actions
- auto‑escalate incidents
- suppress minority or dissenting views
- infer intent without supporting evidence
- present speculation as fact
- collapse uncertainty silently

If AI output cannot be explained to a human, it does not belong in the system.

---

## Explainability as a First‑Class Requirement

All AI outputs must be:

- traceable to underlying signals,
- explainable in plain language,
- reversible as new data arrives.

This ensures:
- auditors can understand reasoning,
- decision‑makers can challenge assumptions,
- and confidence can evolve transparently.

---

## Relationship to Other Documents

AI reasoning is bounded by:

- 📄 `MODEL.md` — what concepts may exist and relate
- 📄 `COLLECTIONS.md` — what questions are being answered
- 📄 `PERSONAS.md` — how meaning is framed for decisions
- 📄 `ARCHITECTURE_OVERVIEW.md` — where reasoning is permitted

Implementation details appear in:
- 📄 `AI_REASONING.md` → **this document**
- 📄 `GOVERNANCE.md` — oversight, audit, and controls

---

## Final AI Principle

> **AI is trusted here not because it is authoritative,  
> but because it is constrained.**

The system succeeds only if humans remain:
- aware,
- oriented,
- informed,
- and ultimately responsible.