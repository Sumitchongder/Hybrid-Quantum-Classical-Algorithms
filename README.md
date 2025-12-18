# Hybrid Quantum–Classical QAOA Evaluation Framework with Multi‑Optimizer GUI

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Qiskit](https://img.shields.io/badge/Qiskit-Framework-6929C4?style=for-the-badge&logo=qiskit&logoColor=white)](https://qiskit.org/)
[![GPU Acceleration](https://img.shields.io/badge/GPU-Accelerated-76B900?style=for-the-badge&logo=nvidia&logoColor=white)](https://qiskit.org/ecosystem/aer/)
[![License](https://img.shields.io/badge/License-MIT-red?style=for-the-badge)](LICENSE)

---

## 📌 Overview
This repository presents a **comprehensive evaluation framework** for the **Quantum Approximate Optimization Algorithm (QAOA)**, implemented entirely in **Qiskit** for the quantum path and integrated with a wide range of classical optimizers. The framework supports **GPU‑accelerated simulation**, **multi‑optimizer benchmarking**, and **interactive GUIs (Tkinter, Jupyter widgets)** for comparative analysis.

The project was developed as part of my research contributions under **Kirankumar Sir**, extending beyond the scope of **qHiPSTER** (Quantum High Performance Software Testing Environment). While qHiPSTER focused on scalable quantum simulation, this framework advances the field by introducing **hybrid quantum–classical orchestration, optimizer benchmarking, and reproducible visualization pipelines**.

---

## 🎯 Motivation
Variational quantum algorithms like QAOA rely on a hybrid loop: a quantum circuit prepares states, while a classical optimizer tunes parameters. The performance of QAOA depends critically on the choice of optimizer, circuit depth, and computational resources.  
This project addresses these challenges by:
- Benchmarking multiple optimizers (gradient‑based vs gradient‑free).
- Providing reproducible sweeps over depth and repetition cost.
- Integrating GPU acceleration for realistic performance.
- Offering interactive GUIs for exploration and reporting.

---

## ✨ Key Features
- **Quantum path (Qiskit‑only):**
  - QAOA circuit construction for MAX‑CUT on regular graphs.
  - AerSimulator with GPU acceleration (`device="GPU"`) and fallback to CPU.
  - Exact expectation via Statevector or sampling via measurements.

- **Classical optimization path:**
  - 12 optimizers integrated:
    - *Gradient‑based*: BFGS, L‑BFGS‑B, CG, Newton‑CG, SLSQP, Trust‑Constr.
    - *Gradient‑free*: Nelder‑Mead, Powell, COBYLA, Differential Evolution, Basin‑Hopping, SHGO.
  - Multi‑start runs to avoid poor local minima.
  - Unified interface for optimizer benchmarking.

- **Evaluation sweeps:**
  - Satisfaction vs **QAOA depth** \(p\).
  - Satisfaction vs **repetition cost** (proxy for runtime budget).
  - Smoothed monotonic curves for publication‑ready plots.

- **Interactive GUIs:**
  - **Jupyter widgets**: toggle optimizers, sliders for depth/runs, live plots.
  - **Tkinter desktop GUI**: checkboxes for optimizers, sliders, dropdowns, and comparison plots.

<p align="center">
  <img width="300" height="600" alt="Image" src="https://github.com/user-attachments/assets/e5524b89-8f48-4cb5-ab88-a719b2ec8532" />
</p>

- **Artifacts:**
  - JSON outputs for reproducibility.
  - PNG plots for reporting.
  - Human‑readable summaries for recruiters and collaborators.

---

## 🧑‍🔬 Contributions Beyond qHiPSTER
- **Hybrid orchestration**: Designed a full loop integrating Qiskit circuits with SciPy optimizers, extending qHiPSTER’s simulation focus into hybrid algorithm evaluation.
- **Optimizer benchmarking**: Implemented a comparative study of 12 optimizers, classifying them into gradient‑based and gradient‑free categories, and analyzing their performance on QAOA.
- **GPU integration**: Enabled GPU acceleration in AerSimulator, demonstrating HPC readiness and aligning with resume claims of GPU‑aware quantum simulation.
- **Interactive GUIs**: Built both notebook‑friendly (ipywidgets) and desktop (Tkinter) interfaces, showcasing ability to translate research into recruiter‑friendly demos.
- **Visualization pipeline**: Developed smoothing and cumulative comparison plots, making noisy optimizer behavior interpretable and publication‑ready.
- **Research alignment**: Positioned the framework as a bridge between qHiPSTER’s scalable simulation and practical hybrid algorithm evaluation, contributing to the broader research paper context.

---

## 🏗️ System Architecture

The framework is designed as a **layered hybrid system**, ensuring clarity, reproducibility, and extensibility:

<p align="center">
  <img width="700" height="500" alt="Image" src="https://github.com/user-attachments/assets/1298d725-207e-48c8-9f95-2a43879d34dc" />
</p>

1. **Quantum Layer (Qiskit)**
   - Constructs QAOA circuits for MAX‑CUT on regular graphs.
   - Uses AerSimulator with GPU acceleration (CUDA) or CPU fallback.
   - Provides exact expectation values via Statevector or sampling via measurements.

2. **Classical Layer (SciPy Optimizers)**
   - Integrates 12 optimizers:
     - *Gradient‑based*: BFGS, L‑BFGS‑B, CG, Newton‑CG, SLSQP, Trust‑Constr.
     - *Gradient‑free*: Nelder‑Mead, Powell, COBYLA, Differential Evolution, Basin‑Hopping, SHGO.
   - Supports multi‑start runs to mitigate local minima.
   - Offers unified benchmarking across optimizers.

3. **Evaluation Layer**
   - Performs sweeps over QAOA depth \(p\) and repetition cost (proxy for runtime budget).
   - Applies smoothing and monotonic enforcement to produce publication‑ready curves.
   - Outputs JSON artifacts and PNG plots for reproducibility.

4. **GUI Layer**
   - **Jupyter Widgets**: interactive sliders, toggles, and live plots for exploratory research.
   - **Tkinter GUI**: desktop application with checkboxes, sliders, and comparison plots for recruiter‑friendly demos.
   - Bridges research and communication by making results accessible to both technical and non‑technical audiences.

---

## 🔬 Research Directions
This framework opens multiple avenues for deeper exploration:

- **Warm‑start heuristics**: Incorporating classical approximations (e.g., Goemans–Williamson) to initialize QAOA parameters.
- **Advanced mixers**: Exploring XY and constrained mixers for structured optimization problems.
- **Noise studies**: Switching to density matrix simulation with realistic noise models and error mitigation strategies.
- **Scaling analysis**: Benchmarking optimizer sensitivity on larger graphs and higher depths.
- **Hybrid HPC integration**: Extending to distributed simulation environments (e.g., qHiPSTER) for large‑scale hybrid experiments.
- **Optimizer taxonomy**: Systematically classifying optimizer performance across problem sizes, noise levels, and resource budgets.

---

## 🌍 Industry & Career Impact
This project demonstrates skills that are directly relevant to both **research labs** and **industry recruiters**:

- **Systems Integration**: Ability to combine quantum simulation, classical optimization, GPU acceleration, and GUI design into a cohesive framework.
- **Reproducibility & Rigor**: JSON artifacts, plots, and seeded experiments ensure results can be replicated and trusted.
- **Industry Relevance**: Hybrid quantum–classical workflows are central to near‑term quantum computing applications in optimization, logistics, and finance.
- **Scientific Communication**: Interactive GUIs and clear plots make complex research accessible to non‑experts, showing leadership in bridging technical depth with stakeholder communication.
- **Innovation Beyond qHiPSTER**: Extends prior simulation work into hybrid algorithm evaluation, optimizer benchmarking, and recruiter‑friendly visualization — demonstrating initiative and originality.
