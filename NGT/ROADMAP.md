# NGT-2.0 — Roadmap (6 Months)

This roadmap defines the core development milestones required to bring NGT-2.0 from a fully specified mathematical model to a functional structural-economic protocol with testable components.

---

## Phase 1 — Structural Simulation Layer (Month 1–2)

### Milestones
- Implement Structural State Engine (Δ, Φ, M, κ)
- Build Viability Domain checker (Φ ≤ Φ_max, M ≤ M_max, ||Δ|| ≤ Δ_max, κ ≥ 0)
- Implement Structural Flow primitive:
  - energy gradient module
  - deviation correction module
  - memory penalty module
  - contractivity guard
- Create minimal simulation scripts:
  - JSON state snapshots
  - step-by-step structural transitions
- Publish “Structural Flow Simulator v0.1”

### Deliverables
- Simulation engine (TypeScript/Python)
- Test cases
- State visualizer (console or basic web UI)

---

## Phase 2 — Vault & Reserve Engine (Month 2–3)

### Milestones
- Implement Vault Layer (reversibility buffer)
- Implement Reserve Layer structure:
  - asset slots
  - rotation model
  - symmetric liquidity checks
- Map Structural Flow → Reserve/Vault operations
- Implement soft vs hard correction logic
- Publish “Reserve Engine v0.1”

### Deliverables
- Reserve/Vault simulator modules
- Safe operation ruleset (κ-guard)
- Documentation for rotation logic

---

## Phase 3 — Smart Contract Framework (Month 3–4)

### Milestones
- Create Solidity/Rust interfaces for:
  - structural metrics input
  - reserve/vault operations
  - governance boundaries
- Implement contractivity guard on-chain (κ ≥ 0)
- Publish “NGT-2.0 Contracts v0.1”
- Security model draft

### Deliverables
- Core contract scaffolding
- κ-guard contract
- Structural metrics interface
- Audit-prep notes

---

## Phase 4 — Governance 2.0 Layer (Month 4–5)

### Milestones
- Implement DAO boundaries module:
  - Φ_max
  - M_max
  - Δ_max
  - asset eligibility
- Build boundary update logic
- Integrate with Structural Flow simulator
- Publish “Governance 2.0 v0.1”

### Deliverables
- DAO parameter contracts
- Governance → boundaries API
- Full documentation

---

## Phase 5 — EFM (Emergency Flexion Mode) (Month 5–6)

### Milestones
- Implement EFM structural projection
- Build safe mode ruleset:
  - low-impact corrections
  - vault-priority operations
  - energy suppression logic
  - collapse boundary guard
- Publish “EFM Engine v1.0”

### Deliverables
- EFM simulation module
- Safety proofs (Δ, Φ, M, κ)
- Final integration tests

---

## Final Output (End of Month 6)

- Full Structural Simulation Suite  
- Reserve/Vault Engine  
- Contractivity Safety Engine  
- Governance 2.0 Modules  
- EFM Engine  
- Solidity/Rust prototype  
- Public documentation + SDK v1.0  

NGT-2.0 becomes the first fully operational **Structural Reserve Protocol**.
