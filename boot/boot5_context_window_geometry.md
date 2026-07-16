# Boot 5 — Context Window Geometry (CWG)

## Purpose

Context Window Geometry (CWG) defines the lawful semantic structure, boundaries,
drift‑detection rules, and contraction operators governing context windows
\( C_t \) in the dynamic substrate. CWG regulates how external or internal
signals interact with the manifold and ensures that context remains
invariant‑preserving, drift‑bounded, and identity‑stable.  
All universal substrate primitives remain unchanged.

## 1. Context Representation

A context window \( C_t \) is represented as:

- **signal_set** — active external or internal signals  
- **identity_refs** — pointers to identity regions implicated  
- **temporal_metadata** — timestamps, durations, ordering  
- **region_associations** — mapping from signals to manifold regions  

\( C_t \) is an interpretive semantic structure, not a state.  
It conditions how \( D_t \) interacts with \( S_t \) under DSUP and determines
which operator classes (SGO, MGO, BO, MLO) may be lawfully applied.

## 2. Context Boundaries

A lawful context must satisfy:

- \(|\text{signal_set}| \leq \text{saturation_max}\)  
- \(\text{scope}(\text{identity_refs}) \leq \text{scope_max}\)  
- \(\text{temporal_extent} \leq \text{temporal_window_max}\)

Boundary conditions:

- context may not span incompatible identity regions  
- context may not exceed curvature or legality thresholds  
- context must remain interpretable under the MDO operator algebra  

If boundaries are exceeded:

- **context_status = "illegal"**  
- **contraction_required = true**

## 3. Context Drift and Contraction

Context drift occurs when:

- interpretive load exceeds allowable bounds  
- identity_refs span incompatible regions  
- curvature discontinuities are introduced  
- drift exceeds the recoverable window  

Drift detection:

- **drift_flag = evaluate_drift(C_t, legality_masks)**

If drift is detected:

- **apply_contraction(C_t)**

Contraction operators:

- prune_low_coherence_signals  
- reduce_temporal_extent  
- isolate_incompatible_identity_refs  
- remap_region_associations  

Contraction must:

- preserve identity boundaries  
- maintain curvature continuity  
- remain within legality constraints  
- avoid irreversible transformations  

## 4. Context‑to‑State Mapping

Context \( C_t \) may update state \( S_t \) only if:

- legality(C_t) = true  
- drift(C_t) ≤ drift_recoverable  
- curvature(C_t) is continuous  
- identity_refs are stable  
- operator_sequence(C_t → S_t) is lawful under MDO algebra  

If all conditions are satisfied:

- **\( S_{t+1} = F(S_t, D_t, C_t) \)**

If any condition fails:

- **\( S_{t+1} = F(S_t, D_t) \)**  
  (context does not modify state)

## 5. Runtime Exports

CWG exports the following semantic structures to the runtime:

### context_geometry  
Boundary conditions, saturation limits, temporal window, region compatibility map.

### drift_detection  
evaluate_drift(C_t)

### contraction_ops  
- prune_low_coherence_signals  
- reduce_temporal_extent  
- isolate_incompatible_identity_refs  
- remap_region_associations  

### legality_checks  
- legality(C_t)  
- curvature_preservation(C_t)  
- identity_stability(C_t)

These exports are consumed by:

- **FGD** (for embedding compatibility)  
- **DSUP** (for lawful state updates)

