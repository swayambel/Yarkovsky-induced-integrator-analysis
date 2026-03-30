# Impact of Yarkovsky Effect on Orbital Stability under Different Numerical Integrators

## Overview

This project investigates how small non-gravitational perturbations, specifically the Yarkovsky effect, influence orbital evolution over long timescales and how different numerical integrators handle such perturbations.

While classical two-body simulations assume purely gravitational dynamics, real asteroid motion is affected by subtle forces that can cause measurable drift. This project explores how accurately different numerical methods capture this behavior.

---

## Objectives

- Model orbital motion with both gravitational and non-gravitational forces  
- Implement a simplified Yarkovsky acceleration model  
- Compare numerical integrators in long-term simulations  
- Analyze how numerical errors interact with physical perturbations  

---

## Key Concepts

- Two-body orbital dynamics  
- Yarkovsky effect (simplified tangential acceleration model)  
- Numerical integration methods:
  - Euler Method  
  - Runge-Kutta 4 (RK4)  
  - Velocity Verlet (Symplectic)  

---

## Methodology

1. Simulate an asteroid in an elliptical orbit under solar gravity  
2. Introduce a small tangential acceleration to model the Yarkovsky effect  
3. Run simulations using different numerical integrators  
4. Track and compare:
   - Orbital trajectory  
   - Semi-major axis drift  
   - Energy evolution  
   - Angular momentum conservation  

---

## Expected Outcomes

- Symplectic integrators preserve orbital structure better over long timescales  
- Non-symplectic methods introduce artificial drift  
- Numerical error can amplify or mask real physical perturbations  

---

## Project Structure
simulation.ipynb # Main simulation and analysis
README.md # Project documentation

---

## Why This Project Matters

This project connects numerical methods with real-world orbital dynamics by showing that:

> The choice of integrator is not just a computational detail — it directly affects the physical interpretation of long-term simulations.

---

## Future Scope

- Incorporating spin-dependent Yarkovsky models  
- Extending to YORP-driven evolution  
- Parameter sensitivity analysis  

---

## Author

Swayam Beluse
