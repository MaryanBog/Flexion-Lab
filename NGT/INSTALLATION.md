# Installation & Setup Guide
### NGT-2.0 — Structural Reserve Protocol

This guide explains how to set up the environment for working with the NGT-2.0 repository.  
The project currently includes documentation, specifications, architecture files, and upcoming simulation modules.

---

## 1. Requirements

Software:
- Node.js 18+
- Python 3.10+
- Git
- Markdown editor (VS Code recommended)

Optional:
- Python virtual environment
- Node Version Manager (nvm)

---

## 2. Clone the Repository

git clone https://github.com/MaryanBog/NGT-Whitepaper
cd NGT-Whitepaper

---

## 3. Directory Structure Overview

/
├── docs/
├── Archives/
├── PROJECT_OVERVIEW.md
├── ROADMAP.md
├── TECHNICAL_SPECS.md
├── GRANT_PROPOSAL.md
├── TEAM.md
├── CONTRIBUTING.md
└── INSTALLATION.md

---

## 4. Simulation Environment (Upcoming)

When the Structural Flow Simulator is added:

Install dependencies:
npm install

Run the simulator:
npm run simulate

Expected functionality:
- load structural state X = (Δ, Φ, M, κ)
- compute Structural Flow
- check viability (X ∈ D)
- output JSON logs

---

## 5. Python Tools (Optional)

For structural analysis:

pip install -r requirements.txt

Future scripts may include:
- analyze_state.py
- plot_flow.py
- check_viability.py

---

## 6. Adding New Modules

Rules:
1. New code goes into dedicated folders (/simulator/, /contracts/, /tools/)
2. Only deterministic logic allowed
3. No heuristic or market triggers
4. κ must never become negative
5. All operations must respect Viability Domain D

See CONTRIBUTING.md for full guidelines.

---

## 7. Documentation Build (Optional)

If a documentation generator is added:

npm run docs  
or  
python generate_docs.py

(Not active yet.)

---

## 8. Troubleshooting

If dependencies fail:
- update Node.js
- recreate Python venv
- delete node_modules and reinstall

Update repository:
git pull origin main

Questions or unclear parts:
Email: m7823445@gmail.com

---

## 9. Project Status

NGT-2.0 is currently in:
- documentation/specification phase
- simulator and contract system engineering next
- preparing for grant implementation

This installation guide will expand as code modules are added.

---

## 10. Final Notes

This repository is designed for clarity, safety, and long-term architectural correctness.  
All future modules (simulator, contracts, SDK) will use this installation workflow.

