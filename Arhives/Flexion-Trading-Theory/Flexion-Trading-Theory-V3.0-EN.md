# 1. Introduction and Objectives

Flexion Trading Theory (FTT) V3.0 defines a complete structural model of market dynamics based solely on observable price data P(t).  
The theory introduces a geometric interpretation of market motion through flexion derivatives, structural orientation, event triggers, and adaptive decision filters.

The objective of FTT is to describe trading signals as **structural transitions** in the shape of price evolution, not as reactions to volatility, patterns, or classical technical indicators.

FTT formalizes:
- the primary flexion derivatives ΔP, C = Δ²P, and ΔS = Δ³P,
- structural orientation K(t),
- the event system (FEW, FXB),
- adaptive structural windows W,
- the complete decision function that maps observable data to trading actions.

FTT V3.0 establishes a canonical mathematical foundation for the Flexion Trading Runtime Engine (FTRE).  
All practical implementations must strictly follow the definitions provided in this theory.

---

# 2. Observable Quantities

FTT V3.0 operates strictly on **observable market data**, without hidden variables or external sources.  
At each timestamp t the only input is the price P(t).  
All structural quantities are computed internally from P(t) over a finite window.

### 2.1 Price Series
- P(t) — the last traded price at time t.  
The theory does not assume continuity, smoothness, or distributional form; P(t) is treated as a discrete-time observable.

### 2.2 Time Basis
- t ∈ ℤ⁺ — monotonically increasing event index representing market ticks.  
Actual wall-clock timestamps may vary, but FTT uses event order, not real time, for structural derivatives.

### 2.3 Internal Observable Window
FTT requires a finite rolling window W(t) of the price series:
- {P(t−k)} for k = 0 … W(t)

This window is:
- adaptive,
- determined from structural smoothness conditions (Section 6),
- never fixed permanently.

### 2.4 No Additional Inputs
FTT uses **no indicators**, no volume, no OHLC bars, no moving averages, no volatility estimates from outside the theory.

Everything required for trading signals is derived directly from P(t) and its discrete variations.

This ensures:
- full theoretical purity,
- determinism,
- independence from broker-specific data,
- perfect reproducibility in FTRE.

---

# 3. Primary Flexion Derivatives

Flexion Trading Theory describes market structure through discrete geometric derivatives of price.  
These derivatives measure curvature, structural bending, and inflection within the price trajectory.

All derivatives below are defined on the adaptive window W(t) introduced in Section 6.

---

## 3.1 First Flexion Derivative: ΔP(t)
ΔP(t) captures the **instantaneous directional change** of price:

ΔP(t) = P(t) − P(t−1)

Properties:
- sign(ΔP) defines local upward/downward motion,
- magnitude |ΔP| reflects local impulse intensity,
- ΔP is the base for higher-order structural derivatives.

---

## 3.2 Second Flexion Derivative: C(t) = Δ²P(t)
C(t) represents **curvature** — the bending of price trajectory:

C(t) = ΔP(t) − ΔP(t−1)

Interpretation:
- C(t) > 0 → structure bends upward (convex),
- C(t) < 0 → structure bends downward (concave),
- C(t) = 0 → locally straight structural motion.

This is the primary driver of orientation K(t).

---

## 3.3 Third Flexion Derivative: ΔS(t) = Δ³P(t)
ΔS(t) captures **structural torsion** — the moment where curvature changes direction:

ΔS(t) = C(t) − C(t−1)

Interpretation:
- peaks of ΔS signal structural turning points,
- zero-crossings mark shifts between bending regimes,
- maxima/minima of ΔS(t) define FXB exit events.

ΔS is the **core volatility-independent structural indicator**.

---

## 3.4 Numerical Stability
All Flexion derivatives use minimal discrete operators:

- no smoothing,
- no interpolation,
- no external filters.

Stability is achieved only through:
- adaptive window W(t),
- structural filters (Section 6),
- event logic (Section 5).

Thus derivatives remain physically meaningful even under noisy tick conditions.

---

# 4. Structural Orientation K(t)

Structural orientation K(t) defines the **dominant direction of structural motion** in the price trajectory.  
It is derived solely from the curvature derivative C(t) and reflects the persistent geometric bias of the market.

---

## 4.1 Definition

K(t) is defined as the **sign of the cumulative curvature trend** over the adaptive window W(t):

K(t) = sign( Σ C(t−k) ),  for k = 0…W(t)

Thus:

- K(t) = +1 → persistently upward structural orientation  
- K(t) = −1 → persistently downward structural orientation  
- K(t) = 0 → no dominant orientation (neutral structure)

---

## 4.2 Interpretation

### Upward orientation (K = +1)
- curvature C(t) tends to be positive,
- price structure bends upward,
- upward flexion events (FEW_UP) are structurally valid.

### Downward orientation (K = −1)
- curvature C(t) tends to be negative,
- price structure bends downward,
- downward flexion events (FEW_DN) are structurally valid.

### Neutral orientation (K = 0)
- structural symmetry,
- mixed curvature,
- the market is in a transitional or noisy phase.

In the neutral regime, **all FEW signals are suppressed**.

---

## 4.3 Orientation as a Stability Requirement

K(t) acts as a **directional filter** for FEW events:

- FEW is permitted only if its direction matches K(t).
- Opposite-direction events are ignored as noise.
- K(t) prevents overtrading in oscillatory micro-movements.

This ensures that trades align with **structural direction**, not tick noise.

---

## 4.4 Relation to ΔS(t)

ΔS(t) defines the moment of structural reversal.  
K(t) defines the **persistent direction**.

Together they ensure:
- FEW = entry into dominant structural bending,
- FXB = exit at torsion extremum.

Both depend only on P(t) and are fully deterministic.

---

# 5. Structural Events

Structural events are the core decision triggers of FTT.  
All events arise exclusively from the behavior of C(t) and ΔS(t), without indicators or smoothing.  
There are only two event types:

- **FEW — Flexion Entry Window**
- **FXB — Flexion Break (Exit)**

---

## 5.1 FEW — Flexion Entry Window

FEW marks the moment when the structure **enters a new bending regime** consistent with the dominant orientation K(t).

### 5.1.1 Formal definition

A FEW event occurs at time t if:

1. **C(t) crosses zero in the direction of K(t)**  
   sign(C(t)) = K(t)

2. **Curvature increases in the direction of K(t)**  
   C(t) > C(t−1)  when K=+1  
   C(t) < C(t−1)  when K=−1

3. **Orientation filter active**  
   K(t) ≠ 0

Thus:

- FEW_UP  → K=+1 and curvature bending upward  
- FEW_DN  → K=−1 and curvature bending downward

### 5.1.2 Interpretation

FEW represents the **start of a structurally valid impulse**.  
Not a price breakout, not a pattern — a real geometric transition of curvature.

FEW is always an **entry** event.

---

## 5.2 FXB — Flexion Break (Exit)

FXB marks the **structural torsion maximum**, where the curvature regime becomes unstable.

### 5.2.1 Formal definition

A FXB event occurs at time t if:

1. **ΔS(t) is a local extremum (peak or trough)**  
   ΔS(t−1) < ΔS(t) > ΔS(t+1)   (peak)  
   ΔS(t−1) > ΔS(t) < ΔS(t+1)   (trough)

2. **Magnitude stability**  
   |ΔS(t)| > |ΔS(t−1)| and |ΔS(t)| > |ΔS(t+1)|

FXB does NOT depend on K(t) — structural instability is symmetric.

### 5.2.2 Interpretation

FXB is the precise moment where the curvature loses coherence and the previous bending regime collapses.

Thus:
- every FEW must eventually be followed by an FXB,
- FXB always implies **exit**,
- FXB has no directional bias.

---

## 5.3 Structural Cycle FEW → FXB

The complete structural trading cycle is:

1. **FEW** — enter the impulse  
2. **K(t)** — hold while oriented  
3. **FXB** — exit at structural break

This cycle is deterministic and derived entirely from flexion geometry.

No volatility analysis, patterns, or indicators are needed.

---

# 6. Flexion Windows and Filters

FTT V3.0 uses an adaptive structural window W(t) to ensure stable computation of flexion derivatives and event logic.  
The window is not constant; it follows the geometry of price motion.

Additionally, secondary structural filters (M, μ, Θ) provide numerical stability while preserving full theoretical purity.

---

## 6.1 Adaptive Structural Window W(t)

The window W(t) determines how many past points are used when evaluating:

- orientation K(t),
- flexion derivatives ΔP, C, ΔS,
- stability conditions.

### 6.1.1 Definition

W(t) is defined as the **minimum window that stabilizes curvature sign**:

W(t) = min k  such that  
sign( Σ C(t−i), i=0…k ) = sign( Σ C(t−i), i=0…k+1 )

Interpretation:
- when the structure is stable → W(t) small (3–7 ticks),
- when structure fluctuates → W(t) expands automatically.

This gives robust orientation without smoothing or lag.

---

## 6.2 Structural Magnitude Filter μ(t)

μ(t) represents **local impulse strength**:

μ(t) = |ΔP(t)|

Usage:
- filter extremely small movements,
- suppress FEW during micro-noise.

Condition:
FEW allowed only if μ(t) > μ_min(W(t))

where μ_min is a threshold growing with W(t).  
Large window → require stronger impulse → no microtrades.

---

## 6.3 Curvature Stability Filter M(t)

M(t) is the **rolling magnitude of curvature**:

M(t) = avg( |C(t−i)|, i=0…W(t) )

Usage:
- rejects FEW when curvature is inconsistent,
- ensures entry only when bending is coherent across the window.

Condition:
FEW allowed only if |C(t)| > α · M(t)

with α typically in [1.2 – 2.0].

---

## 6.4 Temporal Coherence Filter Θ(t)

Θ(t) is the local structural timescale that measures the coherence of torsion dynamics within the adaptive window W(t). It is defined as:

\[
\Theta(t) = \frac{W(t)}{|ΔS(t)| + \varepsilon}
\]

where ε is the minimal discrete torsion granularity imposed by the price grid. This correction prevents division by zero without altering the structural meaning of ΔS(t). The parameter ε is not a tunable constant and does not introduce smoothing; it represents the smallest nonzero possible change in torsion due to discrete price increments.

Interpretation:
- small Θ(t) → strong, coherent structural motion
- large Θ(t) → torsion degenerates into noise

Condition:
FEW is suppressed when Θ(t) exceeds the temporal coherence limit Θ_max. This ensures entries occur only during structurally meaningful torsion-driven impulses.

---

## 6.5 Summary of Filters

A FEW event is valid only if all structural conditions are met:

1. orientation alignment (K filter)  
2. curvature direction (C filter)  
3. curvature stability (M filter)  
4. impulse magnitude (μ filter)  
5. temporal coherence (Θ filter)

These filters do NOT change the theory — they enforce it numerically while preserving structural purity.

---

# 7. Flexion Trading Structural Cycle (FTSC)

The Flexion Trading Structural Cycle (FTSC) is the complete lifecycle of a trade as defined purely by structural geometry.  
Every trade must follow this cycle exactly; no steps may be skipped, repeated, or reordered.

The cycle consists of three deterministic stages:

1. **Structural Initiation**  
2. **Structural Propagation**  
3. **Structural Collapse**

Each stage maps directly to observable flexion derivatives and event conditions.

---

## 7.1 Stage 1: Structural Initiation (FEW)

This stage begins when the market transitions into a coherent bending regime.

Conditions:
- sign(C(t)) = K(t)
- curvature increasing in the direction of K(t)
- all filters μ, M, Θ satisfied
- K(t) ≠ 0

Event:
- FEW_UP  → Start of upward bending  
- FEW_DN  → Start of downward bending  

The trade is **opened** at FEW.

This marks the entry into a new structural impulse.

---

## 7.2 Stage 2: Structural Propagation (Holding Phase)

During this phase the structure moves coherently in the direction defined by K(t).  
The trade remains open under the following invariants:

1. K(t) must remain constant in sign  
2. C(t) must not reverse relative to K(t)  
3. No FXB extremum must occur  
4. Filters must remain satisfied:
   - |C(t)| > α·M(t)
   - μ(t) above threshold
   - Θ(t) within limit

Interpretation:
- structure is stable,
- bending direction persists,
- no torsion instability detected.

During propagation, **no new trades** are allowed.

---

## 7.3 Stage 3: Structural Collapse (FXB)

Collapse occurs when torsion ΔS(t) reaches a local extremum:  
a peak or trough indicating structural instability.

Conditions:
- ΔS(t−1) < ΔS(t) > ΔS(t+1), or  
- ΔS(t−1) > ΔS(t) < ΔS(t+1)

Event:
- FXB (exit)

FXB always marks the **end** of the structural impulse.

Exit is mandatory:
- FEW → hold → FXB  
- no exceptions, no delays, no re-entry inside a cycle.

---

## 7.4 Complete Cycle Summary

A structurally valid trade always follows:

1. **FEW** — entry at new structural bending  
2. **K(t)** — propagation while bending persists  
3. **FXB** — exit at torsion extremum

Constraints:
- exactly one FEW per cycle  
- exactly one FXB per cycle  
- no FEW allowed before a collapse  
- no FXB allowed before an entry  

The FTSC defines trading as a direct mapping of geometric structure, not price movement.

---

# 8. Formal Decision Function (FTT_API)

FTT_API is the canonical decision function that maps
observable market data P(t) to structural trading actions.
The function is deterministic and fully defined by the theory;
no heuristic rules or empirical tuning are allowed.

FTT_API produces exactly three possible outputs:

- FEW_UP   — open long position
- FEW_DN   — open short position
- FXB      — close any open position
- NONE     — no action

---

## 8.1 Input Domain

The function receives only the observable sequence:

P(t), P(t−1), … , P(t−W(t))

No additional information is permitted.

From P(t), the engine computes:

- ΔP(t)
- C(t)       = Δ²P(t)
- ΔS(t)      = Δ³P(t)
- K(t)
- W(t)
- M(t), μ(t), Θ(t)

All of these are internal structural variables.  
They are *not* inputs — they are **computed** inside the API.

---

## 8.2 Decision Logic

The decision function is defined as:

FTT_API(P(t)) =
FEW_UP if FEW conditions satisfied with K(t)=+1
FEW_DN if FEW conditions satisfied with K(t)=−1
FXB if FXB extremum detected
NONE otherwise


This mapping is total and deterministic.

Order of evaluation:

1. **FXB check**  
   If ΔS(t) is a local extremum → return FXB  
   (FXB has absolute priority)

2. **FEW check**  
   If all FEW rules satisfied:
   - orientation alignment: sign(C(t)) = K(t)
   - curvature strengthening in direction of K(t)
   - all filters μ, M, Θ satisfied
   - K(t) ≠ 0  
   Then:
      - return FEW_UP if K=+1  
      - return FEW_DN if K=−1  

3. **Else** return NONE

---

## 8.3 Determinism and Purity

FTT_API satisfies:

- **Determinism**: identical P(t) → identical output  
- **Locality**: decisions depend only on finite window  
- **Purity**: no stochastic components, no smoothing, no probabilistic thresholds  
- **Completeness**: every structural state maps to exactly one output  

No discretionary overrides or timer-based rules are allowed.

---

## 8.4 State Transition Rules

The decision function defines the structural trading state machine:

State S(t) ∈ {FLAT, LONG, SHORT}

Transition rules:

- S = FLAT  
    - FEW_UP → LONG  
    - FEW_DN → SHORT  
    - FXB → FLAT (ignored)  
    - NONE → FLAT

- S = LONG  
    - FXB → FLAT  
    - FEW_UP/FEW_DN ignored  
    - NONE → LONG

- S = SHORT  
    - FXB → FLAT  
    - FEW_UP/FEW_DN ignored  
    - NONE → SHORT

This guarantees:
- exactly one open position per cycle  
- no overlapping trades  
- no recursive entries

---

## 8.5 API Output Encoding

FTT_API returns a compact structural code:

- 0 → NONE  
- 1 → FEW_UP  
- 2 → FEW_DN  
- 3 → FXB

This encoding corresponds directly to FTRE.

---

# 9. Mapping Theory → FTRE Runtime Engine

FTRE (Flexion Trading Runtime Engine) is the canonical implementation of the Flexion Trading Theory (FTT).  
Its purpose is to convert the theoretical constructs of Sections 1–8 into a deterministic, production-grade computational engine.

FTRE contains **no new logic**.  
It is a strict, mechanical translation of FTT into executable form.

---

## 9.1 Architectural Principles

FTRE must follow three invariants:

1. **Purity**  
   All structural quantities (ΔP, C, ΔS, K, W, M, μ, Θ) are computed only from P(t).  
   No external indicators, timers, smoothing, or probabilistic methods are allowed.

2. **Determinism**  
   Identical price sequences must always produce identical structural decisions.

3. **Canonical Mapping**  
   FTRE implements FTT_API exactly as defined in Section 8.

---

## 9.2 Internal Processing Pipeline

For every price update P(t), FTRE performs:

1. **Window Update**  
   - append P(t)  
   - adapt W(t) via curvature stability  
   - discard values outside W(t)

2. **Compute Derivatives**  
   - ΔP(t) = P(t) − P(t−1)  
   - C(t)  = ΔP(t) − ΔP(t−1)  
   - ΔS(t) = C(t) − C(t−1)

3. **Compute Orientation**  
   K(t) = sign( Σ C(t−i) for i=0…W(t) )

4. **Compute Filters**  
   - μ(t) = |ΔP(t)|  
   - M(t) = avg|C(t−i)|  
   - Θ(t) = W(t) / |ΔS(t)|

5. **Event Evaluation**  
   - FXB priority: check ΔS extremum  
   - FEW conditions: curvature alignment + filters  
   - else NONE

6. **State Transition**  
   Apply rules from Section 8.4.

7. **Return Structural Code**  
   (0, 1, 2, 3)

---

## 9.3 API Definition (Canonical Form)

FTRE exposes exactly one public method:

int FTRE_Evaluate(double price, int timestamp);


which returns:

- 0 = NONE  
- 1 = FEW_UP  
- 2 = FEW_DN  
- 3 = FXB

No additional outputs or auxiliary data are permitted in the API layer.  
Any diagnostic or debug information must be optional and separate.

---

## 9.4 Independence from Platform

FTRE must run:

- identically on every broker,  
- regardless of spread, liquidity, or execution speed,  
- without depending on MQL, C++, or OS-specific behavior.

Platform-specific code (EA, script, bot, connector) is a thin wrapper around FTRE.

The **theory lives in FTT**,  
the **logic lives in FTRE**,  
the **trading execution lives in the platform wrapper**.

---

## 9.5 Completeness of Mapping

Sections mapped directly:

- Section 3 → derivative engine  
- Section 4 → orientation engine  
- Section 5 → event engine  
- Section 6 → window + filters engine  
- Section 7 → structural state machine  
- Section 8 → canonical decision function  
- Section 9 → runtime implementation rules

FTRE contains no components outside this mapping.

---

## 9.6 FTRE as the Only Canonical Implementation

FTRE V1.0 becomes the **only valid executable reference** of the Flexion Trading Theory.  
Any deviation from FTT definitions invalidates the engine.

FTT defines *what* happens.  
FTRE defines *how* it happens.  
Trading platforms only execute *the result*.