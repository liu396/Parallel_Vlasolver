# **ParaVlasolver: Parallel Grid-Based Kinetic Vlasov Solver**

A Parallel High-Performance Grid-Based Kinetic 1D1V Vlasov Solver for Computational Plasma Dynamics

## **Outline**
---

### 1. **Author and Maintainer**
* Chen Cui (cuichen@usc.edu) 
* Qiancheng Zhao (qianchez@usc.edu)

### 2. **Problem Description**

**Physical Processes Need to be Studied in the Plasma Flow of Electric Propulsion Thrusters**
* Electrons in plasma expansion problems are proven to be non-equilibrium, fluid desscription is not valid anymore.
* Electrons' temperature is proven to be anisotropic, thermodynamics and energy transfer process need to be studied.
* Kinetic Method need to be used instead of fluid method to resolve physical processes.

**Low Noise Method is Needed to Resolve Physical Processes**
* Numerical noise will combine with physical processes and make the physical processes hard to be studied.
* Particle-based kinetic method is easy to be implemented but with big numerical noise. Grid-based kinetic method have no-inherent numerical noise but with huge computational cost.
* Parallel grid-based kinetic method need to be developed.

### 3. **Methods and Techniques**
**Algorithms**
* Semi-Lagrangian time stepping.
* Third Order Positive Flux Conservation [1] method on phase domain discretization. 

**Parallelization**
* Thread Parallelization: ***OpenMP***
* Domain Decomposition: ***OpenMPI***
* Inhomogeneous Parallelization: ***CUDA[2]***

### 4. **Expected Results**
* Improve the computational efficency of the original ***Vlasover***
* Keep the possiblity of achieving higher dimensional ***Vlasolver***

## **Reference**
---
[1]: Filbet, Francis, Eric Sonnendrücker, and Pierre Bertrand. "Conservative numerical schemes for the Vlasov equation." Journal of Computational Physics 172.1 (2001): 166-187.

[2]: Einkemmer, Lukas. "Semi-Lagrangian Vlasov simulation on GPUs." arXiv preprint arXiv:1907.08316 (2019).