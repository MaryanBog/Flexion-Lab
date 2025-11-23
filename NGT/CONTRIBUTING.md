# Contributing to NGT-2.0

Thank you for your interest in contributing to the NGT-2.0 project.  
This document outlines the contribution process and technical expectations.

NGT-2.0 is a Structural Reserve Protocol based on Flexion Dynamics V2.0.  
All contributions must respect the mathematical invariants of the system:
Φ ≤ Φ_max, M ≤ M_max, ||Δ|| ≤ Δ_max, κ ≥ 0.

---

## 1. How to Contribute

### Option A — Documentation Contributions
You can contribute by improving:
- technical documentation
- diagrams
- specification clarity
- explanation of structural components

Make changes in Markdown files inside `/docs` or root-level docs.

### Option B — Simulation / Code Contributions
If working on the simulator or prototype implementation:
- follow the structural flow specification
- never implement price-based triggers or heuristics
- respect viability domain constraints
- ensure κ cannot become negative
- use deterministic logic only

Submit contributions in a separate branch:
`feature/<your-feature-name>`

---

## 2. Branch Workflow

1. Fork the repository  
2. Create a feature branch:
   `git checkout -b feature/my-update`
3. Make your changes  
4. Submit a Pull Request to `main`  
5. PR will be reviewed for:
   - correctness  
   - consistency with Flexion Dynamics  
   - safety invariants  
   - clarity of documentation  

---

## 3. Coding Requirements

### Mandatory Rules
- No heuristic or market-reactive logic  
- No liquidation triggers  
- No loops that may diverge without κ-checks  
- All structural transitions must be bounded  
- Memory (M) must only increase through valid definitions  
- Do not introduce any operation that may violate D  

### Recommended
- Keep modules small and explicit  
- Use deterministic functional patterns  
- Provide examples and tests where applicable  

---

## 4. Documentation Requirements

Each contribution must include:
- clear explanation of purpose  
- formulas or diagrams if structural elements are affected  
- reasoning for safety (Φ, M, Δ, κ impact)  
- updated references if needed  

---

## 5. Communication

For discussions, clarifications, or pre-proposal checks:

Email: **m7823445@gmail.com**  
GitHub: https://github.com/MaryanBog  

If unsure whether a contribution aligns with Flexion Dynamics —  
ask before implementing.

---

## 6. Code of Conduct

- Be respectful and constructive  
- Keep feedback technical and objective  
- No speculation-based or price-focused discussions  
- Maintain the scientific integrity of the project  

---

## 7. Contribution Philosophy

NGT-2.0 is not a speculative protocol.  
It is a mathematically governed structural system.

Contributions must strengthen:
- structural correctness  
- safety  
- clarity  
- long-term viability  

Every change must help the protocol remain **structurally alive**.

