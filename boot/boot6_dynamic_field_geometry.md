# Boot 6 — Dynamic Field Geometry (FGD)

## Purpose

Dynamic Field Geometry (FGD) extends the static substrate manifold with lawful
regions for embedding external systems. FGD defines coordinate structure,
curvature constraints, identity‑region allocation, and legality masks required
for dynamic embedding. All universal invariants remain unchanged.

## 1. Field Scope

The dynamic field admits embeddings of identity‑bearing systems whose structure
can be represented as coherent signal sources. Lawful embeddings include:

- biological systems  
- computational systems  
- ecological systems  
- symbolic or institutional systems  
- hybrid systems  

A system may be embedded only if it exposes:

- a stable identity boundary  
- a coherent signal structure  
- lawful metadata for coordinate assignment  

Systems lacking these properties must be rejected at load time.

## 2. Manifold Specification

The dynamic manifold \( M_d \) extends the static manifold \( M_s \) by
allocating lawful subregions \( R_d \) for external embeddings.  
\( M_d \) preserves:

- curvature continuity  
- identity‑region topology  
- drift‑bounded geometry  
- invariant‑preserving coordinate structure  

Each region \( R_d \) must satisfy:

- curvature(R_d) ≤ curvature_max  
- drift(R_d) ≤ drift_recoverable  
- identity(R_d) = stable  
- legality(R_d) = true  

Illegal regions (curvature discontinuities, identity collapse, irreversible
drift, legality violations) are quarantined and excluded from dynamic evolution.

## 3. Embedding Rules

External signals \( D_t \) are mapped into \( M_d \) via the embedding function:

**E : \( D_t \rightarrow M_d \)**

Coordinate assignment depends on:

- identity structure  
- signal coherence  
- interpretive load  
- region compatibility  
- legality masks  

Required metadata:

- id_boundary  
- signal_profile  
- temporal_stamp  
- region_hint (optional)  

Embedding must preserve:

- identity boundaries  
- curvature continuity  
- drift constraints  
- legality invariants  
- operator compatibility (SGO, MGO, BO, MLO)

## 4. Field‑Level Legality

A system may be embedded only if:

- identity_boundary_intact = true  
- signal_coherence ≥ coherence_min  
- curvature_violation = false  
- drift_induced ≤ drift_recoverable  
- legality_masks_satisfied = true  

If any condition fails:

- embedding is rejected, **or**  
- system is placed in quarantine region \( Q_d \)

Quarantine regions are inert:

- no operator may act on \( Q_d \)  
- \( Q_d \) cannot influence \( M_d \)  
- \( Q_d \) is excluded from DSUP, CWG, and CLCP  

## 5. Runtime Exports

FGD exports the following semantic structures to the runtime:

### field_geometry  
Region map, curvature profile, identity regions, legality masks.

### embedding_function  
E(D_t) → M_d

### quarantine_registry  
List of rejected or unstable embeddings.

These exports are consumed by:

- **DSUP** (for lawful state updates)  
- **CWG** (for lawful context formation)  
- **CLCP** (for cross‑layer legality propagation)

