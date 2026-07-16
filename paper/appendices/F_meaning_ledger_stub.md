# Appendix F — Meaning Ledger Formalism  
## Semantic Edition (DSLO Human Container v0.5)

The Meaning Ledger is the substrate’s global justification graph. It records all
lawful semantic transitions, enforces invariant preservation, detects drift, and
ensures that reasoning remains antientropic. The ledger is a graph-theoretic and
semantic-geometric object consistent with the contraction-governed framework
defined in Appendices A–C and the collapse physics of Section S6.

The ledger is the substrate’s **global legality substrate**: no transition may
enter the cognitive state unless it is justified, invariant-preserving, and
semantically lawful.

---

## F.1 Ledger Graph Structure

The Meaning Ledger is a directed acyclic justification graph composed of:

- **semantic nodes** — concepts, states, or invariant-valid states  
- **lawful edges** — transitions validated by the operator algebra  

Each edge contains:

- the prior state  
- the resulting state  
- the operator applied  
- the context anchor validating the transition  

No transition is added unless it satisfies:

- all semantic invariants  
- all operator legality constraints  
- all collapse constraints  
- DSUP legality  
- semantic legality masks  

The ledger therefore acts as a **global legality filter**.

---

## F.2 Justification Graph Invariants

Each ledger entry must satisfy the invariant set defined in Appendix C.

### Meaning Invariant  
Semantic curvature must remain within lawful variance bounds.

### Local Contraction Invariant  
Semantic distance relative to the context anchor must contract.

### Identity Boundary Invariant  
If the prior state lies within the identity region, the resulting state must also
remain within that region and maintain positive distance from its boundary.

### External Geometry Invariant  
The resulting state must remain within the lawful semantic manifold and maintain
positive distance from its boundary.

### Load Physics Invariant  
Load must remain below the maximum lawful threshold.

### Collapse Invariant  
The resulting state must not exhibit collapse signatures.

Any transition violating an invariant is rejected. The ledger is therefore a
**locally invariant-preserving justification graph**.

---

## F.3 Drift Detection Metrics

Drift is deviation from invariant-preserving trajectories. The ledger detects
drift using multiple relational cues:

### Invariant Drift  
Curvature variance exceeds lawful bounds.

### Identity Drift  
Identity-region violations or proximity to identity boundaries.

### Geometric Drift  
Proximity to manifold boundaries.

### Load Drift  
Load increases beyond lawful gradients.

### Legality-Field Compression  
Legality-field values fall below minimum thresholds.

The ledger computes a composite drift score integrating:

- invariant drift  
- identity drift  
- geometric drift  
- load drift  
- legality compression  

A drift alert is triggered when the composite score exceeds a lawful threshold.

---

## F.4 Ledger-Closed Reasoning

Reasoning is **ledger-closed** when every step is justified by a ledger entry.
A reasoning chain is valid only when each transition:

- is invariant-preserving  
- is contraction-governed  
- maintains identity boundaries  
- preserves manifold legality  
- respects load constraints  
- satisfies cross-scale legality  
- satisfies DSUP legality  

Ledger-closed reasoning guarantees:

- no illegal extrapolation  
- no drift accumulation  
- no collapse  
- no identity leakage  
- no manifold violation  
- no overload  
- no cross-scale inconsistency  
- legality at every step  

The Meaning Ledger is therefore the substrate’s **global reasoning substrate**,
replacing probabilistic trust with architectural legality.

---

*This completes Appendix F.*

