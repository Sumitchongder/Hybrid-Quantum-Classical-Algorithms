# Hybrid Quantum–Classical QAOA Evaluation Framework

## Overview
This project implements a evaluation framework for the **Quantum Approximate Optimization Algorithm (QAOA)** using **Qiskit** for quantum circuit construction and simulation, and **SciPy** for classical optimization. It demonstrates a **hybrid quantum–classical loop**, GPU-aware backend initialization, and reproducible sweeps.

---

## Key features
- **Qiskit-only quantum path:**
  - AerSimulator with `statevector` or `density_matrix` method.
  - **GPU auto-detection** with fallback to CPU.
  - Exact expectation via Statevector or sampling via measurement shots.
- **Hybrid classical optimization:**
  - Multi-start runs with `BFGS` or `Nelder–Mead`.
  - Configurable iteration budgets, tolerances, and finite-difference steps.
- **Reproducible sweeps and artifacts:**
  - Satisfaction vs **QAOA depth** and vs **repetition cost**.
  - Non-decreasing smoothed trends for clean reporting.
  - JSON results, PNG plots, and a human-readable summary.

---

## Metrics
- **Objective:** Fraction of satisfied cut edges (normalized MAX-CUT value).
- **Depth sweep:** Performance across QAOA layers \(p\).
- **Cost sweep:** Performance under varying repetition cost (proxy for runtime budget).

