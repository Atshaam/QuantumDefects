# Machine Learning Enabled Discovery of Point Defect Qubits for Quantum Technologies

**Authors:** Atshaam Ashraf, Dr Alex Ganose, Dr Katherine Inzani

**Institution:** Imperial College London

**Project Type:** Undergraduate Research Opportunities Programme (UROP)

---

## Overview

This repository accompanies the UROP project Machine Learning Enabled Discovery of Point Defect Qubits for Quantum Technologies, which explores the use of machine learning interatomic potentials (MLIPs) to accelerate the discovery of stable point defect qubits in transition-metal-doped insulating materials.

The work combines computational materials screening, density functional theory (DFT), and MLIPs to identify defect structures with desirable quantum properties such as long coherence times and optical addressability.

---

## Background

Quantum technologies rely on solid-state qubits with long coherence times. Spin-defect qubits—such as NV centres in diamond—are promising candidates, motivating exploration of similar defects in transition metal (TM) doped oxides and nitrides.

The project investigates:

* The formation energies of TM substitutional defects in wide-bandgap hosts.
* The reliability of MLIP models trained on bulk datasets for defect-level energetics.
* Benchmarking MLIP predictions against DFT calculations.

---

## Methods

1. **Materials Screening**

   * Data retrieved from the [Materials Project](https://materialsproject.org/) database (~198,972 crystal structures).
   * Filters applied: TM-containing oxides and nitrides, with available experimental data.

2. **Defect Creation and Relaxation**

   * Primitive cell relaxation using DFT.
   * Creation of neutral TM substitutional defects.
   * Structural relaxation with MLIPs and DFT for benchmarking.

3. **Defect Formation Energy**

   * Calculated using total energy differences between defective and pristine supercells.
   * GGA+U corrections applied for improved accuracy.

<p align="center">
  <img src="https://github.com/user-attachments/assets/27430279-c1d0-41ac-9cc0-56ec18407c01" alt="Defect formation energy plot" width="353" height="736">
</p>
The numbered steps in the figure correspond to the Jupyter notebooks in `notebooks/main_screening_notebooks`, which implement each stage of the workflow.

---

## Findings

* Negative formation energies were initially observed, corrected using empirical GGA+U adjustments.
* Benchmarking revealed:

  * Close agreement between MLIP and DFT for primitive cell relaxations.
  * Larger discrepancies for defect supercells.
* MLIPs that were reliable for bulk thermodynamic data were insufficient for predicting defect energetics.

---

## Conclusions

* Current MLIP datasets are inadequate for defect-level accuracy.
* Future MLIP training should incorporate hybrid-functional and defect-specific data.
* The approach demonstrates a scalable pathway for high-throughput defect discovery.

---

## Repository Structure

```
├── data/                   # Raw and processed data
├── notebooks/              # Jupyter notebooks used for analysis
├── figures/                # Output plots, tables, and figures
├── README.md               # Project overview (this file)
```

---

## Acknowledgments

This research was conducted as part of the Alchemy Student Internship Programme 2025, supported by the Engineering and Physical Sciences Research Council (EPSRC).
Special thanks to Dr Alex Ganose and Dr Katherine Inzani for their supervision and guidance.

---

## License

This repository is distributed under the [MIT License](LICENSE).

---
