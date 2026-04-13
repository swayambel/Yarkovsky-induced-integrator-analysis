# Impact of Yarkovsky Effect on Orbital Stability under Different Numerical Integrators

## Overview

This project investigates how weak non-gravitational perturbations, specifically the Yarkovsky effect, interact with numerical integration errors in orbital simulations.

The central challenge is not just modeling the perturbation, but determining whether it can be **distinguished from numerical drift** introduced by the integration scheme itself.

---

## Objectives

- Model orbital motion with gravitational + Yarkovsky forces  
- Quantify energy drift due to both numerical error and physical perturbation  
- Compare integrators in terms of accuracy, stability, and signal resolution  
- Determine conditions under which weak forces are reliably detectable  

---

## Key Contributions

- **Decomposition of energy drift** into:
  - Numerical error (pure gravity baseline)
  - Physical Yarkovsky-induced drift  

- **Signal-to-noise (SNR) analysis** to quantify detectability of weak perturbations  

- Identification of a **resolution-limited regime**, where physical signal ≈ numerical error  

- Demonstration of a **trade-off**:
  - RK4 → high accuracy, high SNR (short–medium term)
  - Velocity Verlet → bounded error, long-term structural stability  

---

## Methodology

1. Simulate a 2D two-body system with normalized units  
2. Add a tangential acceleration to model the Yarkovsky effect  
3. Run simulations using:
   - Euler (baseline failure case)
   - RK4 (high-order, non-symplectic)
   - Velocity Verlet (symplectic)

4. Analyze:
   - Orbital trajectories  
   - Energy evolution  
   - Numerical vs physical drift  
   - Timestep convergence  

---

## Key Results

- Euler is unstable and unsuitable for orbital simulations  
- RK4 achieves **very high signal-to-noise ratio**, clearly resolving Yarkovsky drift over short–medium timescales  
- Velocity Verlet maintains **bounded energy error**, but operates near the noise floor at chosen timestep  
- Detectability of weak forces depends critically on:
  - timestep  
  - integrator choice  
  - simulation duration  

---

## Core Insight

> Resolving weak physical perturbations requires that numerical error remains **below the physical signal**, not merely small.

This establishes a fundamental trade-off between:
- **Accuracy (RK4)** → detecting weak forces  
- **Symplectic stability (Verlet)** → long-term fidelity  

---

## Project Structure

- `yarkovsky_stability_analysis.ipynb` — full simulation, analysis, and figures  
- `README.md` — project summary  

---

## Why This Project Matters

In real-world orbital dynamics (asteroid tracking, planetary defense, mission design), small forces accumulate over long timescales.

This study shows that:
- numerical error can mimic or mask real physics  
- integrator choice directly affects scientific conclusions  

---

## Future Work

- Higher-order symplectic integrators (Yoshida schemes)  
- Coupled spin dynamics (YORP effect)  
- 3D orbital extensions  
- Adaptive timestep comparisons (RK45)  

---

## Author

Swayam Beluse
