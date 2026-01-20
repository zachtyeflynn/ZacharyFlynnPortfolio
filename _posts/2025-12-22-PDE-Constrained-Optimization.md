---
title: "CPU Design Optimization"
layout: single
date: 2025-12-22
highlight: false
categories: [Projects]
excerpt: "Conducted PDE-constrained design optimization of a CPU (MECH 579)."
header:
  teaser: /assets/images/Contour.jpg
tags:
  - Python
  - SciPy
  - Jax
---

<img src="{{ '/assets/images/Contour.jpg' | relative_url }}"
     alt="ContourPlotTemperature"
     style="display: block; width: 70%; margin: 0 auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em; text-align: center;">
  <small>
    Steady-state temperature distribution of the CPU with the optimal design parameters. Solved via a provided finite difference PDE solver.
  </small>
</p>

### Executive Summary

- Optimizing the design parameters of a CPU while respecting the constraints imposed by the 2D heat equation.

- Further constraints relating to maximum power consumption and fan speed.

- Used finite difference and automatic differentiation methods to perform gradient based optimization in Scipy Optimize and Jax.

- Performed gradient-based sensitivity analysis to determine the most influential design variables.

### Implementation

- The sequential quadratic programming and trust region solvers were used within SciPy Optimize. Both finite differences and automatic differentiation was used.

- Numerical precision between the FD and AD implementation was compared and tweaked to reduce computation times.

<img src="{{ '/assets/images/GradAD.jpg' | relative_url }}"
     alt="GradientConvergence"
     style="display: block; width: 100%; margin: 0 auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em">
  <small>
    Convergence of the Lagrangian as a function of iterations with the trust region solver and automatic differentiation.
  </small>
</p>

<img src="{{ '/assets/images/SensitivityAnalysis.png' | relative_url }}"
     alt="SensitivityAnalysis"
     style="display: block; width: 100%; margin: 0 auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em">
  <small>
    Sensitivity analysis between design variables: the fan speed of the CPU v, and the circuitry parameters a, b and c.
  </small>
</p>

### Acknowledgements

This was the final project for MECH 579: Numerical Optimization at McGill University. I'd like to thank Professor Siva Nadarajah for formulating this project. Further, I'd like to thank Lingyun Di for collaborating.

I must withhold specfic details about our implementation and restrict access to our GitHub repository as to not violate McGill University's academic integrity policy as well as respect Professor Nadarajah's intellectual property.