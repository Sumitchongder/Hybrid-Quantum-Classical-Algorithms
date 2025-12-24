# Contributing to the Hybrid Quantum–Classical QAOA Evaluation Framework

Thank you for your interest in contributing to this project ⚛️  
Contributions from researchers, students, and practitioners in quantum computing, optimization, and HPC are welcome.

---

## 🧪 Types of Contributions

We welcome contributions such as:

- New classical optimizers or optimizer variants
- Improvements to QAOA circuit construction or evaluation
- GPU or performance optimizations
- New benchmark problems beyond MAX-CUT
- Noise models or error mitigation techniques
- Visualization and GUI enhancements
- Documentation and reproducibility improvements

---

## 🛠 Development Setup

### Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate      # Windows
````

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 📐 Coding Standards

Please follow these guidelines:

* Follow **PEP 8** for Python style
* Write clean, modular, and readable code
* Add clear docstrings to all public functions and classes
* Avoid hard-coded constants; use parameters or configuration
* Use deterministic random seeds where applicable
* Ensure changes do not break existing experiments or GUIs

---

## 🧪 Research & Experimental Contributions

If contributing experiments or benchmarks:

* Clearly specify:

  * Graph structure and size
  * QAOA depth and repetition budget
  * Optimizers used and hyperparameters
* Ensure results are reproducible
* Save artifacts (JSON, plots) where appropriate
* Provide a short interpretation of results

---

## 🔄 Pull Request Process

1. Create a new branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Commit changes with descriptive messages:

   ```bash
   git commit -m "Add COBYLA vs BFGS comparison for p=3"
   ```

3. Push to your fork and open a Pull Request

4. Include in your PR:

   * Summary of changes
   * Motivation and impact
   * Assumptions or limitations
   * References (if applicable)

---

## 📜 Licensing

By contributing, you agree that your contributions will be licensed under the **MIT License**, consistent with this project.

---

## 🙏 Acknowledgement

All contributors will be acknowledged.
Substantial research contributions may be cited in future reports, presentations, or publications.

Thank you for helping advance hybrid quantum algorithms 🚀
