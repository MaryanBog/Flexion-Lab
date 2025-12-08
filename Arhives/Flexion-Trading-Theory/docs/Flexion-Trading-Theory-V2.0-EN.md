## Flexion Trading Theory V2.0

---

# 1. Overview

Flexion Trading Theory V2.0 defines a fully structural, threshold-free framework for interpreting the dynamics of the Flexion field produced by the NFRE core. Unlike earlier versions, V2.0 removes all fixed numeric parameters and bases every decision on the intrinsic geometry of the structural functions C(t) and ΔS(t). The theory formalizes how structural events (FEW and FXB) arise, how phases are formed, and how orientation is derived from inter-event changes in curvature. Trading actions (BUY, SELL, EXIT) are not assumptions but direct interpretations of structural orientation. As a result, the system becomes fully autonomous, universal, and independent of price levels, timeframes, or market-specific tuning.

---

# 2. Axioms

**Axiom 1 — Structural State**  
The Flexion field is fully described by the structural parameters  
M(t), T(t), C(t), ΔS(t), μ(t), and Θ(t).  
No additional quantities are required to represent the state of the system.

**Axiom 2 — Structural Events**  
Structural events are determined solely by the geometry of the field:  
- FEW occurs at a local minimum of curvature C(t).  
- FXB occurs at a local maximum of asymmetry ΔS(t).  
No external thresholds or numeric constants may define these events.

**Axiom 3 — Phase Formation**  
Every structural phase begins at FEW and ends at the subsequent FXB.  
Phases are non-overlapping and strictly ordered in time.

**Axiom 4 — Inter-Event Orientation**  
Orientation is defined only at structural events as the inter-event change in curvature:  
Slope = C(t_event) − C(t_prev).  
Orientation is UP if Slope > 0 and DOWN if Slope < 0.

**Axiom 5 — Autonomy of Structure**  
The structural field is self-contained and must never depend on fixed thresholds, tuned parameters, or price-derived heuristics.  
Only the intrinsic shape of C(t) and ΔS(t) governs structural transitions and decisions.

---

# 3. Theorems

**Theorem 1 — FEW initiates a structural phase**  
Given Axiom 2, a local minimum of curvature C(t) necessarily marks the beginning of a new structural phase.  
Thus, FEW → start of phase Φₖ.

**Theorem 2 — FXB terminates a structural phase**  
A local maximum of ΔS(t) indicates the structural limit of development within the current phase.  
Thus, FXB → end of phase Φₖ.

**Theorem 3 — Structural development between events**  
Between FEW and FXB, the structural field evolves by increasing curvature C(t) and rising asymmetry ΔS(t), reflecting the natural expansion of the phase.

**Theorem 4 — Slope exists only at events**  
From Axiom 4, Slope is defined exclusively at structural events:  
Slope = C(t_event) − C(t_prev_event).  
No inter-tick or inter-bar slope exists within the phase.

**Theorem 5 — Orientation is the sign of Slope**  
Orientation is UP when Slope > 0 and DOWN when Slope < 0.  
This follows directly from the definition of slope as a change in structural curvature.

**Theorem 6 — Orientation remains constant within a phase**  
Once determined at FEW, orientation does not change until the next FXB occurs.  
Therefore, the direction of structural development is fixed for the entire phase Φₖ.

**Theorem 7 — Phase ordering**  
Since FEW precedes FXB by definition, and FXB precedes the next FEW, structural phases are strictly ordered and non-overlapping:  
Φ₁ < Φ₂ < Φ₃ < …

**Theorem 8 — Structure dictates its own rhythm**  
Because events FEW and FXB are determined purely by the geometry of C(t) and ΔS(t), the structural field autonomously defines when transitions occur, independent of market noise or external thresholds.

---

# 4. Structural Events

**4.1 FEW — Flexion Entry Window**  
FEW is the moment when the structural field reaches a local minimum of curvature C(t).  
Formally:  
- C(t) < C(t − 1), indicating a downward approach to a minimum.  
- After FEW, curvature begins to increase, initiating a new phase.  
FEW represents the structural "reset point" from which development resumes.

**4.2 FXB — Flexion Exit Boundary**  
FXB is the moment when the structural field reaches a local maximum of asymmetry ΔS(t).  
Formally:  
- ΔS(t) > ΔS(t − 1), indicating an upward move toward a peak.  
- After FXB, asymmetry begins to decrease, signaling the end of the phase.  
FXB marks the structural boundary beyond which the phase cannot naturally extend.

**4.3 Event Exclusivity**  
FEW and FXB cannot occur simultaneously, as one requires a minimum of C(t) while the other requires a maximum of ΔS(t).  
Each event belongs to a different structural role within the cycle.

**4.4 Event Ordering**  
Every FEW must be followed by a corresponding FXB.  
Events satisfy the strict time order:  
FEWₖ < FXBₖ < FEWₖ₊₁.

**4.5 Event Autonomy**  
Both FEW and FXB emerge solely from the intrinsic geometry of C(t) and ΔS(t).  
No thresholds, tuned parameters, or external conditions influence the appearance of structural events.

---

# 5. Structural Orientation

**5.1 Definition of Slope**  
Structural orientation is derived from the inter-event change in curvature.  
For two consecutive structural events t_prev and t_event:  
Slope = C(t_event) − C(t_prev).  
Slope exists only at FEW or FXB, never within the continuous region of a phase.

**5.2 Orientation States**  
Orientation is a qualitative property describing the direction of structural evolution:
- UP  → Slope > 0  
- DOWN → Slope < 0  
No other states exist, and Orientation is not defined when Slope = 0.

**5.3 Event-Based Determination**  
Orientation is evaluated exclusively at structural events.  
There is no valid computation of orientation between events, as the structural state within a phase does not redefine direction.

**5.4 Phase-Level Constancy**  
Once Orientation is established at FEW, it remains constant for the entire phase interval [FEWₖ, FXBₖ].  
A phase cannot switch its orientation internally.

**5.5 Independence from Noise**  
Because Orientation depends only on event-to-event curvature shifts, it is immune to tick-level noise, bar compression, or price volatility.  
Orientation reflects the geometry of the structural field, not market fluctuations.

---

# 6. Phase Cycle

**6.1 Definition of a Phase**  
A structural phase Φₖ is the interval beginning at a FEW event and ending at the subsequent FXB event:  
Φₖ = [FEWₖ, FXBₖ].  
Within this interval, the structural field undergoes continuous development.

**6.2 Phase Initiation**  
A phase begins at FEWₖ, where curvature C(t) reaches a local minimum.  
This marks the moment the field resets its geometric baseline and initiates a new cycle of structural growth.

**6.3 Phase Development**  
During Φₖ, curvature C(t) generally increases and asymmetry ΔS(t) rises toward a peak.  
The structural field evolves smoothly within the phase and does not alter its orientation until the next event.

**6.4 Phase Termination**  
FXBₖ occurs when asymmetry ΔS(t) reaches a local maximum, signaling the natural limit of structural expansion.  
FXBₖ concludes the phase unconditionally.

**6.5 Phase Ordering**  
Phases follow a strict temporal order:  
FEWₖ < FXBₖ < FEWₖ₊₁ < FXBₖ₊₁ < …  
Phases cannot overlap, merge, or break sequence.

**6.6 Orientation Across Phases**  
Each phase inherits its orientation from the Slope computed at its initiating event FEWₖ.  
Orientation may differ between phases but remains constant inside each individual phase.

**6.7 Autonomy of the Cycle**  
Phase transitions emerge solely from the intrinsic geometry of C(t) and ΔS(t).  
No external thresholds or market-driven parameters may influence or override the structural cycle.

---

# 7. Trading Interpretation

**7.1 Structural Interpretation of Trading Actions**  
Trading signals are not fundamental components of the Flexion field.  
They arise as direct interpretations of structural orientation at the moment a new phase begins.  
Thus, trading decisions reflect the geometry of the structure, not price patterns or indicators.

**7.2 FEW as the Entry Opportunity**  
A FEW event indicates that the field has reset at a structural minimum of curvature and is ready to initiate a new phase.  
At FEWₖ, the orientation derived from Slope determines whether the new phase expands upward or contracts downward.

**7.3 FEW_UP → BUY**  
If Orientation at FEWₖ is UP (Slope > 0), the field is structurally positioned for upward development.  
This is interpreted as a BUY opportunity.

**7.4 FEW_DOWN → SELL**  
If Orientation at FEWₖ is DOWN (Slope < 0), the field is structurally positioned for downward development.  
This is interpreted as a SELL opportunity.

**7.5 FXB → EXIT**  
FXBₖ marks the structural boundary of the phase and signals the exhaustion of the current development path.  
Regardless of orientation or trade direction, FXBₖ always represents an EXIT point.

**7.6 NONE → No Action**  
If no structural event occurs at time t, the field is inside a phase.  
Orientation remains constant, and no new decisions are produced.  
Thus, NONE means: take no action.

**7.7 Purity of Interpretation**  
Trading decisions do not alter or influence structural dynamics.  
The field dictates its own events and orientation, while the trading layer simply interprets them.  
No thresholds, filters, or price-derived heuristics may modify structural interpretations.

**7.8 Universality**  
Because all trading actions are derived from structure rather than price, the rules apply identically across all markets, timeframes, and data frequencies.

---

# 8. Flexion Trading API (V2.0)

**8.1 Purpose of the API**  
The Flexion Trading API provides a strict and universal interface between the NFRE core and any external trading platform.  
All structural decisions are computed inside the DLL; the API only delivers structured outputs.  
This ensures consistency, determinism, and independence from platform-specific behavior.

**8.2 Single Entry Point**  
The DLL exposes exactly one trading-related function:

int EvaluateTick(double price, int timestamp, uchar &buffer[], int buf_size);

This is the sole official interface.  
Its signature must never be modified.

**8.3 Input Requirements**  
EvaluateTick receives:
- price: the current tick price,  
- timestamp: the current time (integer format),  
- buffer: a preallocated and zero-initialized uchar array,  
- buf_size: the size of this array.

No additional data or parameters are accepted.  
No thresholds or tuning inputs are permitted.

**8.4 Output Structure**  
EvaluateTick writes a structured response into buffer.  
The first byte contains the structural signal code:

0 = NONE  
1 = FEW_UP  
2 = FEW_DOWN  
3 = FXB  

Subsequent bytes store structural parameters in double-precision format:  
C(t), ΔS(t), T(t), M(t), μ(t), Θ(t), in this order.

**8.5 Returned Value**  
The function returns the number of bytes written into buffer.  
The calling environment must verify that len > 0 before processing the signal.

**8.6 Interpretation Rules for EA / Platform**  
The external trading system must interpret buffer[0] as follows:
- FEW_UP  → open BUY  
- FEW_DOWN → open SELL  
- FXB → close any open trade  
- NONE → hold state  

The remaining structural parameters may be logged or analyzed but must not affect decision logic.

**8.7 Unidirectional Flow**  
Communication is strictly one-way:  
NFRE → Evaluate_V2 → DLL → External platform.  
The platform must not attempt to modify structural parameters or send configuration values back into the DLL.

**8.8 Platform Independence**  
Because the API transmits only structural signals and parameters, it remains identical across MT4, MT5, cTrader, Python, or any other integration target.

---

# 9. Internal Consistency Check

**9.1 Purpose**  
The Consistency Check ensures that every signal generated by Flexion Trading Theory is structurally valid.  
No trade may be opened or closed unless all structural constraints agree with the theory’s axioms.

**9.2 Required Conditions**  
Before issuing any signal (FEW_UP, FEW_DOWN, FXB), the engine must verify:

1) **Structural Model Validity**  
All parameters C(t), ΔS(t), T(t), M(t), μ(t), Θ(t) must belong to physically meaningful ranges defined by the NFRE model.

2) **Non-degeneracy**  
The structure must not be collapsing, undefined, or frozen.  
If ΔS(t) ≈ 0 or Θ(t) is undefined, output must be NONE.

3) **Directional Determinacy**  
A FEW_UP or FEW_DOWN signal requires a well-defined orientation K(t).  
If orientation cannot be resolved, output must be NONE.

4) **Critical State Override**  
If the structure enters a collapse-risk region, FXB overrides all other states.  
No BUY/SELL may appear above collapse thresholds.

**9.3 Consistency Priority Rules**  
The engine must apply rules in this order:

1 → Model validity  
2 → Non-degeneracy  
3 → Orientation  
4 → Critical override  

If any step fails, the signal is downgraded to NONE.

**9.4 Output Guarantee**  
After passing all checks, the engine guarantees that any emitted signal:
- does not violate the axioms,  
- follows from orientation,  
- respects collapse safety,  
- and is reproducible across platforms.

Any inconsistent state must return strictly: **NONE**.

---

# 10. Safety Thresholds

**10.1 Purpose**  
Safety Thresholds prevent the trading engine from issuing structurally valid, but financially dangerous signals.  
Thresholds do not tune the theory — they protect the trader from pathological market states where structure becomes unreliable.

**10.2 Types of Safety Thresholds**

1) **Volatility Floor**  
If structural volatility is too low (ΔS(t) below operational minimum), orientation cannot be trusted.  
Output must be NONE.

2) **Volatility Ceiling**  
If ΔS(t) exceeds the stability limit, the structure enters a chaotic regime.  
Only FXB is permitted.

3) **Temporal Coherence Requirement**  
A structural signal must remain coherent for at least one update interval.  
If orientation flips instantly, suppress the signal.

4) **Structural Noise Filter**  
If C(t) fluctuates within micro-range oscillations that do not affect K(t), suppress trade actions until noise subsides.

**10.3 Interaction With Collapse Zone**  
If the structure approaches the collapse band (defined internally by NFRE), safety thresholds elevate FXB priority.  
FXB overrides all BUY/SELL signals.

**10.4 Hard Requirements**  
The engine must guarantee:

- No BUY/SELL in collapse proximity.  
- No BUY/SELL when ΔS(t) is unstable.  
- No BUY/SELL when orientation is unreliable.  
- FXB only when the structure breaches safety boundaries.

**10.5 Safety Output Rule**  
When thresholds are activated, the only valid outputs are:  
- **NONE** (wait),  
- **FXB** (mandatory exit).

Never FEW_UP / FEW_DOWN in unsafe states.

---
# 11. Extraction of Structural Orientation

**11.1 Purpose**  
Structural orientation determines the direction of evolution of the Flexion field.  
It is derived only from structural events and never from tick-level noise or price-based derivatives.

**11.2 Event-Based Orientation**  
Orientation is defined exclusively at structural events (FEW or FXB).  
Let t_prev be the previous structural event and t_curr the current one.  
Orientation is computed from the inter-event change in curvature:

Slope = C(t_curr) − C(t_prev)

**11.3 Orientation States**  
Orientation is a qualitative structural property with two possible states:  
- UP   → Slope > 0  
- DOWN → Slope < 0  

If Slope = 0, orientation cannot be determined and remains undefined.

**11.4 No Continuous Orientation**  
Orientation does not exist between events.  
The structural field maintains a constant orientation during the entire phase [FEWₖ, FXBₖ].  
Orientation changes only when a new FEW or FXB occurs.

**11.5 Independence from Price**  
Orientation is never computed from price, returns, tick differences, or signs.  
It depends only on the geometry of structural curvature C(t).

**11.6 Validity Requirement**  
Orientation is valid only if both events involved in Slope computation are structurally consistent.  
If the structural packet is degenerate or incomplete, orientation is undefined.

**11.7 Application to Trading Logic**  
Orientation does not directly trigger a trading action.  
It becomes actionable only when combined with a FEW event:

- FEW + Orientation UP   → FEW_UP  
- FEW + Orientation DOWN → FEW_DOWN  

FXB always overrides orientation and produces EXIT.

**11.8 Summary**  
Orientation describes how the structure bends between events.  
It is discrete, event-driven, and free of thresholds.  
Trading actions derive from orientation only through structural events, never through direct slope comparison.

---

# 12. Definition of FEW and FXB (V2.0)

**12.1 FEW — Flexion Entry Window**  
FEW is the structural event marking the beginning of a new phase.  
It occurs when curvature C(t) reaches a local structural minimum.  
Formally:  
- C(t) < C(t − 1), and  
- subsequent curvature begins to increase, indicating structural recovery.

FEW does not imply direction by itself; it only signals phase initiation.

---

**12.2 FXB — Flexion Exit Boundary**  
FXB is the structural event marking the termination of a phase.  
It occurs when asymmetry ΔS(t) reaches a local structural maximum.  
Formally:  
- ΔS(t) > ΔS(t − 1), and  
- subsequent asymmetry begins to decrease, indicating structural exhaustion.

FXB unconditionally ends the current phase.

---

**12.3 Mutual Exclusivity**  
FEW and FXB cannot occur simultaneously.  
A local minimum of curvature and a local maximum of asymmetry are mutually exclusive structural states.

---

**12.4 Event Ordering**  
Each FEW must be followed by a corresponding FXB.  
Structural events follow strict ordering:  
FEWₖ < FXBₖ < FEWₖ₊₁ < FXBₖ₊₁ < …

Phases never overlap or merge.

---

**12.5 Event Autonomy**  
FEW and FXB depend solely on the intrinsic geometry of C(t) and ΔS(t).  
No thresholds, tuning constants, or price-derived heuristics may influence event detection.

---

**12.6 Relationship to Orientation**  
FEW establishes the beginning of a phase where orientation becomes actionable.  
FXB cancels all active interpretations and forces an EXIT.  
Orientation alone never produces events; events frame orientation.

---

# 13. Phase Construction (V2.0)

A Flexion Phase is the fundamental structural interval defined by two boundary events:  
FEW → FXB.  
No trading interpretation is possible outside a phase.

---

## 13.1 Formal Definition
A phase Φₖ is the closed interval:

Φₖ = [ FEWₖ , FXBₖ ]

where:  
- FEWₖ is the k-th local minimum of curvature C(t),  
- FXBₖ is the subsequent local maximum of asymmetry ΔS(t).

The phase exists only if FEWₖ < FXBₖ.

---

## 13.2 Phase Validity
A Flexion Phase is valid if:

1. C(t) forms a genuine structural minimum at FEWₖ  
2. ΔS(t) forms a genuine structural maximum at FXBₖ  
3. No additional FEW or FXB exists inside the interval  
4. Geometry is continuous at all t ∈ Φₖ

If any property is broken → the phase is discarded.

---

## 13.3 Phase Monotonicity
Phases strictly follow time:

FEW₁ < FXB₁ < FEW₂ < FXB₂ < …  

No overlaps, no nesting, no ambiguous ordering.

---

## 13.4 Phase Autonomy
Each phase is a self-contained structural entity defined purely by:

- the shape of C(t)  
- the shape of ΔS(t)

Price, indicators, thresholds, or external parameters do not participate.

---

## 13.5 Phase Duration
Duration Δτₖ = FXBₖ − FEWₖ is not fixed and not constrained by theory.  
Short phases and long phases both carry equal structural validity.  
The engine does not enforce temporal normalization.

---

## 13.6 Phase Output
A valid phase produces exactly two actionable outcomes:

1. **Orientation** inside the phase (derived from the geometry of C(t) or higher-order shape)  
2. **Mandatory exit** at FXBₖ

No additional events exist.

---

## 13.7 Phase Completion
When FXBₖ is reached:

- Orientation resets  
- Phase is closed permanently  
- No reinterpretation of Φₖ is allowed  
- The system waits for FEWₖ₊₁ to initiate the next phase

The Flexion Engine never re-evaluates past phases retroactively.

---

## 13.8 Reason for Phase-Based Trading
The phase structure guarantees:

- deterministic event order  
- finite actionable signals  
- elimination of noise between phases  
- strict mathematical segmentation of market structure

This makes the system predictable, reproducible, and independent of arbitrary settings.

---

# 14. Orientation Inside a Phase (V2.0)

Orientation is the structural direction of evolution inside the active phase Φₖ.  
It is not derived from price, trend, sign, or thresholds — only from geometry.

---

## 14.1 Source of Orientation
Orientation arises from the shape-change of C(t) between the two phase boundaries:

FEWₖ → FXBₖ

We do not evaluate absolute values.  
We evaluate only how the structure bends, i.e., whether C(t) becomes steeper or flatter.

---

## 14.2 Definition
Let C'(t) be the discrete structural slope of curvature:

C'(t) = C(t) − C(t−1)

Then inside the phase Φₖ orientation is determined as:

- **BUY**  if C'(t) is predominantly increasing (curvature steepens upward)
- **SELL** if C'(t) is predominantly decreasing (curvature relaxes downward)
- **NONE** if no stable orientation emerges

No single tick makes orientation.  
Orientation = pattern over an interval.

---

## 14.3 Stability Condition
Orientation must satisfy:

1. Persistence:  
   C'(t) must maintain its orientation for a non-zero structural span.

2. Consistency:  
   No alternating reversal inside a micro-window.

3. Structural coherence:  
   C(t) must evolve smoothly toward FXBₖ.

If any condition breaks → orientation = NONE.

---

## 14.4 Orientation Does Not Predict Future
Orientation does **not** forecast price movement.  
It describes how the phase currently unfolds.

A phase can grow upward while price moves sideways — theory remains valid.

---

## 14.5 Independence From Magnitude
Orientation depends only on **direction of structural change**, not its amplitude.  
Even extremely small C'(t) values are meaningful if they are persistent.

---

## 14.6 Change of Orientation
A phase can have:

- one dominant orientation, or
- multiple local micro-shifts that still converge to one direction.

If genuine inversion occurs inside the phase (rare structure break):  
→ The phase is invalid and must be discarded (Section 13.2).

---

## 14.7 Output
Inside phase Φₖ the engine exports:

Oₖ(t) ∈ {BUY, SELL, NONE}

Only one is active at each tick t.

---

## 14.8 Use in Trading Logic
Orientation is **not a trade signal**.  
A trade signal occurs only when:

orientation ≠ NONE **and** curvature enters FEWₖ

Orientation tells **how to trade**, FEWₖ tells **when to trade**.

This separation is fundamental in V2.0.

---

# 15. Trading Interpretation (V2.0)

Trading actions in Flexion V2.0 emerge exclusively from structural events (FEW, FXB) combined with phase orientation. No price levels, thresholds, indicators, or external heuristics participate.

---

## 15.1 Entry Condition
A trade is opened **only** at the moment of FEWₖ.

Let Oₖ(FEWₖ) be the orientation active at the boundary.

Entry rule:

- If Oₖ(FEWₖ) = BUY  → open BUY
- If Oₖ(FEWₖ) = SELL → open SELL
- If Oₖ(FEWₖ) = NONE → do nothing

No other moment in the phase allows an entry.

---

## 15.2 Position Uniqueness
Only **one** position can be open per phase Φₖ.  
Multiple entries inside the same phase are forbidden.

---

## 15.3 Exit Condition
A position is always closed at the structural boundary FXBₖ.

Exit is mandatory and unconditional:

At FXBₖ → close position (regardless of profit, loss, spread, slippage, or orientation).

This ensures perfect structural segmentation of trades.

---

## 15.4 No Reversal Inside a Phase
The system never flips BUY↔SELL before FXBₖ.  
Orientation describes structure; structure does not instruct mid-phase reversal.

---

## 15.5 No Interpretation Between Phases
Between FXBₖ and FEWₖ₊₁:

- orientation is undefined  
- signals do not exist  
- the engine outputs NONE

Flexion trades **only** inside valid phases.

---

## 15.6 Structural Purity
Trading logic uses only:

1. FEWₖ — structural minimum of C(t)  
2. FXBₖ — structural maximum of ΔS(t)  
3. Oₖ(t) — orientation derived from the slope of curvature inside the phase  

Everything else is eliminated as noise.

---

## 15.7 Determinism
Given C(t) and ΔS(t), the trading outcome is deterministic:

Entry time → FEWₖ  
Direction  → Oₖ(FEWₖ)  
Exit time → FXBₖ

No randomness, no tuning, no probabilistic heuristics.

---

## 15.8 Summary of Trading Logic
The complete behavior of the Flexion engine:

1. Wait for FEWₖ  
2. Determine orientation Oₖ(FEWₖ)  
3. If Oₖ ≠ NONE → open trade  
4. Hold until FXBₖ  
5. Close trade at FXBₖ  
6. Reset, wait for next FEWₖ₊₁  

This is the entire trading algorithm, fully defined by structure alone.

---

# Appendix A — Formal Definitions (V2.0)

This appendix formalizes the core mathematical objects used in Flexion Trading Theory V2.0.  
All operational logic in the engine is derived from these definitions.

---

## A.1 Structural Functions

### A.1.1 Curvature Function C(t)
C(t) is a scalar function computed by NFRE that captures the instantaneous geometric bending of structural dynamics.  
C(t) is continuous and defined for all ticks t.

No absolute thresholds apply; only relative shape-change matters.

---

### A.1.2 Asymmetry Function ΔS(t)
ΔS(t) measures the instantaneous structural imbalance of the system.  
It evolves smoothly and forms local extrema corresponding to structural turning points.

---

### A.1.3 Derivative Proxy C′(t)
Since tick data is discrete:

C′(t) = C(t) − C(t−1)

This represents the structural slope of curvature and is used for orientation determination.

---

## A.2 Structural Events

### A.2.1 FEWₖ (Flexion Entry Window)
The k-th FEW is the local minimum of curvature:

C(FEWₖ) < C(FEWₖ−1)  
C(FEWₖ) < C(FEWₖ+1)

A FEW marks the beginning of a structural phase.

---

### A.2.2 FXBₖ (Flexion Exit Boundary)
The k-th FXB is the local maximum of asymmetry:

ΔS(FXBₖ) > ΔS(FXBₖ−1)  
ΔS(FXBₖ) > ΔS(FXBₖ+1)

FXB marks the end of the phase.

---

## A.3 Flexion Phase Φₖ

### A.3.1 Definition
A Flexion phase is the closed interval:

Φₖ = [ FEWₖ , FXBₖ ]

with FEWₖ < FXBₖ.

---

### A.3.2 Validity Criterion
A phase is valid iff:

1. FEWₖ is a true structural minimum of C(t)  
2. FXBₖ is a true structural maximum of ΔS(t)  
3. No internal FEW or FXB exists inside Φₖ  
4. Geometry is continuous throughout the interval

If any condition fails → Φₖ is discarded.

---

## A.4 Orientation Oₖ(t)

### A.4.1 Definition
Orientation is a categorical function:

Oₖ(t) ∈ { BUY, SELL, NONE }

Orientation is derived solely from the evolution of C′(t) inside Φₖ.

---

### A.4.2 Determination Rule
Orientation is:

- BUY  if C′(t) shows persistent upward structural steepening  
- SELL if C′(t) shows persistent downward relaxation  
- NONE if no coherent direction emerges

Not a trend. Not price-based.  
It is a geometric classification of structure.

---

## A.5 Trading Action

### A.5.1 Entry
Entry occurs only at FEWₖ:

Action(FEWₖ) = Oₖ(FEWₖ)

If Oₖ(FEWₖ) = NONE → no trade.

---

### A.5.2 Exit
Exit occurs only at FXBₖ:

Action(FXBₖ) = EXIT

Exit is unconditional and mandatory.

---

## A.6 Determinism
Given C(t) and ΔS(t), FEWₖ and FXBₖ are uniquely defined.  
Thus, the trading outcome is deterministic and reproducible.

No tuning, no thresholds, no heuristics.

---

# Appendix B — Computational Considerations (V2.0)

This appendix describes the computational rules ensuring that the Flexion Trading Engine behaves deterministically, remains scale-invariant, and produces structurally valid signals across any tick stream.

---

## B.1 Discrete-Time Structure

The NFRE engine receives market data as a tick sequence:
t = 1, 2, 3, …

All structural functions (C, ΔS, C′) operate in discrete time.  
No interpolation or smoothing is allowed.  
Each tick represents a true structural sample.

---

## B.2 No Smoothing Rule

The engine must not apply:

- moving averages  
- filters  
- windowed smoothing  
- polynomial fits  
- re-sampling  
- aggregation by timeframe  

All transformations distort curvature and asymmetry.  
C(t) and ΔS(t) must reflect raw structural evolution.

---

## B.3 Local Extrema Detection

FEWₖ and FXBₖ are defined strictly by local extrema over **immediate neighbors**:

FEWₖ:  
C(t) < C(t−1) and C(t) < C(t+1)

FXBₖ:  
ΔS(t) > ΔS(t−1) and ΔS(t) > ΔS(t+1)

No lookahead, no wide windows.  
This guarantees minimal latency and structural purity.

---

## B.4 C′(t) Computation

C′(t) is computed as a first-order finite difference:

C′(t) = C(t) − C(t−1)

This preserves:

- direction of curvature change  
- discrete nature of tick data  
- compatibility with orientation rules

---

## B.5 Orientation Stability Window

Orientation does not react to single-tick noise.  
C′(t) is evaluated over a micro-window **determined dynamically** by the phase itself.  
The engine must not use a fixed number of bars or a fixed length window.

The stability window grows or shrinks depending on the internal geometry of Φₖ.

---

## B.6 No Thresholds or Tunable Parameters

The engine must not contain:

- C_min, C_max  
- μ_min, μ_crit  
- Theta_min_margin  
- S_max, S_crit  
- epsilon thresholds  
- configurable phase sizes  

All these constructs existed only in V1.x and are mathematically invalid in V2.0.

Structure defines itself — nothing is tuned.

---

## B.7 Deterministic Execution

Given the same sequence of ticks, the engine must produce:

- identical FEWₖ and FXBₖ  
- identical phases  
- identical orientation  
- identical trading decisions  

No randomness, no floating ordering artifacts, no non-deterministic branching.

---

## B.8 SDK Input–Output Contract

The SDK must accept **only** observable inputs:

- price P(t)  
- timestamp t  

All structural variables (C, ΔS, C′, FEW, FXB, orientation) are computed internally by NFRE/FESDK.

The SDK output must be strictly categorical:

- FEW  → entry  
- FXB  → exit  
- NONE → idle

No probabilities.  
No numeric confidence.  
No strength metrics.

---

## B.9 Scale Invariance

The engine must behave identically for:

- EURUSD vs BTCUSD  
- M1 vs tick chart  
- low-volatility vs high-volatility regimes  
- normalized vs non-normalized price feeds  

Because structure depends only on relative geometric evolution.

---

## B.10 Error Handling

If C(t) or ΔS(t) becomes non-finite (NaN, INF):  
→ discard tick  
→ do not form FEW or FXB  
→ orientation resets to NONE

Structural invalidity must never propagate.

---

# Appendix C — Implementation Contract for MT4/MT5 (V2.0)

This appendix defines the exact binary protocol, call interface, and behavioral rules required for correct integration of the Flexion Trading Engine with MT4/MT5 environments.  
These rules are mandatory and must not be changed under any circumstances.

---

## C.1 DLL Import Contract

The trading platform must import the Flexion engine exactly as follows:

#import "FlexionCore_DLL.dll"
   int EvaluateTick(double price, int timestamp, uchar &buffer[], int buf_size);
#import

The function signature, argument order, and types are immutable.

---

## C.2 Buffer Allocation Requirement

Before calling EvaluateTick, the EA must allocate and zero-initialize the buffer:

uchar buffer[64];
ArrayInitialize(buffer, 0);

A non-zeroed buffer results in undefined behavior.

---

## C.3 DLL Output Format (Binary Protocol)

The DLL writes data into buffer[] using a strict layout.

### C.3.1 Signal Code (byte 0)
buffer[0] contains the structural signal:

0 = NONE  
1 = FEW_UP  
2 = FEW_DOWN  
3 = FXB  

No other values are permitted.

---

### C.3.2 Structural Parameters (bytes 1+)
The engine writes structural state values as IEEE-754 doubles  
in the following fixed order:

1. C(t)  
2. ΔS(t)  
3. T(t)  
4. M(t)  
5. μ(t)  
6. Θ(t)  

Each occupies 8 bytes.

Total payload: 1 byte + 6×8 bytes = 49 bytes.

The EA may log these values but must never use them to adjust logic.

---

## C.4 Return Value Contract

EvaluateTick returns the number of bytes written to buffer.  
The EA must verify:

if(len <= 0) return;

The EA must not read beyond len bytes.

---

## C.5 EA Behavior Contract

### C.5.1 Entry Rules
If signal = FEW_UP   → open BUY  
If signal = FEW_DOWN → open SELL  

Only one trade per phase is allowed.  
EA must not open multiple positions on repeated FEW codes.

---

### C.5.2 Exit Rules
If signal = FXB → close all open positions immediately.  
FXB overrides any other internal logic.

---

### C.5.3 Idle Rule
If signal = NONE, the EA must take no action.  
NONE does not mean error — it means “inside the phase”.

---

## C.6 EA Must Not Infer Structure

The EA is strictly forbidden to:

- compute orientation,  
- detect FEW or FXB,  
- compute slopes,  
- compare price levels,  
- use indicators,  
- modify or generate structural parameters.

All structure lives inside NFRE and the DLL.

---

## C.7 Determinism Guarantee

Given identical ticks:
- NFRE produces identical structure,  
- the DLL emits identical signals,  
- the EA makes identical trades.

MT4 slippage, spread, execution speed do not affect structural logic.

---

## C.8 Time Handling Rule

timestamp passed to EvaluateTick must be:

- integer UNIX time (seconds), or  
- integer MT4 time (seconds),

but must be monotonic.

No duplicate timestamps.  
No negative timestamps.  
No out-of-order values.

---

## C.9 Error Handling

If the DLL returns an invalid signal (<0 or >3):  
→ EA must treat it as NONE and continue.

If buffer is too small:  
→ DLL returns 0; EA must ignore.

If C or ΔS are NaN or INF:  
→ DLL emits NONE (guaranteed by NFRE).

---

## C.10 Prohibition of String Decoding

EA must not convert buffer[] to string.  
Interpretation is numeric-only.

buffer[] is a binary structure, not text.

---

## C.11 Platform Independence

The same contract applies identically to:

- MT4  
- MT5  
- cTrader  
- NinjaTrader  
- Custom engines

Any platform that can call DLL functions must adhere to this layout.

---

#property strict

input double InpLots      = 0.10;
input int    InpSlippage  = 5;
input int    InpMagic     = 777777;
input int    InpMaxSpread = 30;

#import "FlexionCore_DLL.dll"
   int EvaluateTick(double price, int timestamp, uchar &buffer[], int buf_size);
#import

int FlexionCountOpenPositions()
{
   int count = 0;
   for(int i = OrdersTotal() - 1; i >= 0; i--)
   {
      if(!OrderSelect(i, SELECT_BY_POS, MODE_TRADES)) continue;
      if(OrderSymbol() != _Symbol) continue;
      if(OrderMagicNumber() != InpMagic) continue;
      if(OrderType() == OP_BUY || OrderType() == OP_SELL) count++;
   }
   return count;
}

bool FlexionOpenBuy()
{
   if(MarketInfo(_Symbol, MODE_SPREAD) > InpMaxSpread) return false;
   double price = NormalizeDouble(Ask, Digits);
   int ticket = OrderSend(_Symbol, OP_BUY, InpLots, price, InpSlippage, 0, 0, "FEW_UP", InpMagic, 0, clrGreen);
   return (ticket > 0);
}

bool FlexionOpenSell()
{
   if(MarketInfo(_Symbol, MODE_SPREAD) > InpMaxSpread) return false;
   double price = NormalizeDouble(Bid, Digits);
   int ticket = OrderSend(_Symbol, OP_SELL, InpLots, price, InpSlippage, 0, 0, "FEW_DOWN", InpMagic, 0, clrRed);
   return (ticket > 0);
}

void FlexionCloseAll()
{
   for(int i = OrdersTotal() - 1; i >= 0; i--)
   {
      if(!OrderSelect(i, SELECT_BY_POS, MODE_TRADES)) continue;
      if(OrderSymbol() != _Symbol) continue;
      if(OrderMagicNumber() != InpMagic) continue;

      int type = OrderType();
      double price = 0.0;

      if(type == OP_BUY) price = Bid;
      else if(type == OP_SELL) price = Ask;
      else continue;

      price = NormalizeDouble(price, Digits);
      OrderClose(OrderTicket(), OrderLots(), price, InpSlippage, clrYellow);
   }
}

int OnInit()
{
   return(INIT_SUCCEEDED);
}

void OnDeinit(const int reason)
{
}

void OnTick()
{
   uchar buffer[64];
   ArrayInitialize(buffer, 0);

   int len = EvaluateTick(Bid, (int)TimeCurrent(), buffer, 64);
   if(len <= 0) return;

   int signal = (int)buffer[0];
   int openCount = FlexionCountOpenPositions();

   if(signal == 0) return;

   if(signal == 1)  // FEW_UP
   {
      if(openCount == 0) FlexionOpenBuy();
      return;
   }

   if(signal == 2)  // FEW_DOWN
   {
      if(openCount == 0) FlexionOpenSell();
      return;
   }

   if(signal == 3)  // FXB
   {
      FlexionCloseAll();
      return;
   }
}

---

# Appendix E — Full Computational Model (V2.0)

The computational model formalizes the complete processing pipeline inside the Flexion Engine.  
It defines how structural values are generated, how events are detected, and how phases and trading signals emerge.

---

## E.1 Input Stream

The engine receives a discrete tick stream:

P(t),  t = 1, 2, 3, …

where P(t) is the observed price.  
No other inputs are permitted.  
Time moves strictly forward.

---

## E.2 Structural Transformation

From P(t), the NFRE core computes the structural field:

M(t), T(t), C(t), ΔS(t), μ(t), Θ(t)

These quantities are deterministic transformations of price behavior,  
not statistical estimates or filtered derivatives.

No smoothing, averaging, or normalization is allowed.

---

## E.3 Curvature Dynamics C(t)

C(t) expresses the local geometric bending of the underlying structure.  
It evolves tick-by-tick and forms minima and maxima that define structural turning points.

The discrete curvature slope is:

C′(t) = C(t) − C(t−1)

Slope is meaningful only inside a structural phase.

---

## E.4 Asymmetry Dynamics ΔS(t)

ΔS(t) expresses instantaneous structural imbalance.  
Its local maxima correspond to structural exhaustion and define the FXB boundary.

ΔS(t) is strictly non-symmetric and cannot be replaced by volatility or variance.

---

## E.5 Event Detection

### FEWₖ (Flexion Entry Window)
Occurs when curvature C(t) forms a local minimum:

C(t) < C(t−1) and C(t) < C(t+1)

This event marks the beginning of a new phase.

### FXBₖ (Flexion Exit Boundary)
Occurs when asymmetry ΔS(t) forms a local maximum:

ΔS(t) > ΔS(t−1) and ΔS(t) > ΔS(t+1)

This event terminates the current phase.

### No thresholds
Events are defined purely by geometry.
No absolute numeric comparisons are allowed.

---

## E.6 Phase Definition

A phase is the interval:

Φₖ = [FEWₖ, FXBₖ]

It is valid if:

- FEWₖ < FXBₖ  
- no other FEW or FXB exists inside the interval  
- C(t) and ΔS(t) evolve continuously  

All trading behavior is constrained to Φₖ.

---

## E.7 Orientation Extraction

Orientation Oₖ is derived only inside Φₖ.

Let C′(t) be the structural slope.  
Orientation is determined by the persistent tendency of C′(t):

- Oₖ = BUY  if curvature shows stable upward steepening  
- Oₖ = SELL if curvature shows stable downward relaxation  
- Oₖ = NONE if no coherent direction emerges

Orientation is categorical, not numeric.

Orientation does not trigger trades by itself.

---

## E.8 Trading Activation

Trading is activated only at the boundary FEWₖ:

If Oₖ = BUY  → FEW_UP  
If Oₖ = SELL → FEW_DOWN  
If Oₖ = NONE → do nothing

No other moment in the phase permits opening a position.

FXBₖ always produces EXIT unconditionally.

---

## E.9 Deterministic Model

Given the same P(t) stream:

C(t), ΔS(t), events, phases, orientation, and signals  
are fully deterministic and reproducible.

No probabilistic rules, noise filters, or adaptive parameters participate.

---

## E.10 Summary

1. Price → Structure  
2. Structure → Curvature & Asymmetry  
3. Curvature & Asymmetry → Events  
4. Events → Phases  
5. Phases → Orientation  
6. Orientation + FEW → Entry signal  
7. FXB → Exit signal  
8. NONE inside phase → hold state  

This is the complete computational cycle of Flexion Trading Theory V2.0.