---
title: "Tool Design Optimization"
layout: single
date: 2025-11-14
highlight: true
highlight_order: 3
toc: true
categories: [Projects]
excerpt: "Anatomically-constrained design optimization of TORS surgical tools."
header:
  teaser: /assets/images/Workspace.png
tags:
  - Python
  - SciPy
---

<img src="{{ '/assets/images/Combined_Workspace.png' | relative_url }}"
     alt="Workspace"
     style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

[View the poster for this project.]({{ "/assets/files/TORS_Poster.pdf" | relative_url }})

### Executive Summary

- Find the optimal design parameters for the surgical tools used in transoral robotic surgery based on anatomical constraints.

- Adapted a simple model of the back of the oropharynx and computed workspace values for various tool parameters. Used response surface methodology to ascertain optimal design parameters.

- Results are being integrated into the [Unicorn Capstone project]({% post_url 2026-01-11-Unicorn-Capstone %}).

- [Poster presentation at the RISEx 2025 conference in Edmonton, AB.](https://openreview.net/forum?id=5hqM7u5ku0)

### Experimental Setup

- Modeled the tool as a 2D, inextensible elastic beam (elastica model/2D Cosserat model).

- Solved the boundary value problem using Scipy Integrate.

- Estimate the tool workspace via Scipy Convex Hull.

- Full factorial response surface experiment to determine optimal design parameters.

<img src="{{ '/assets/images/Parametric_Curve.jpg' | relative_url }}"
     alt="Parametric Curve"
     style="display: block; width: 100%; margin: 0 auto; border-radius: 8px; 
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<img src="{{ '/assets/images/Tool.jpg' | relative_url }}"
     alt="Tool"
     style="display: block; width: 80%; margin: 0 auto; border-radius: 8px; 
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

### Constrained Optimization Results

- Global optimum when tools are slender and long (L = 80 mm, d = 2 mm). This is impractical for real flexural tool design.

- A more realstic sweetspot occurs with tools with larger diameter at around L = 60 mm, d = 5 mm.

<img src="{{ '/assets/images/E_5mPa.png' | relative_url }}"
     alt="Response Surface"
     style="display: block; width: 100%; margin: 0 auto; border-radius: 8px; 
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em; text-align: center;">
  <small>
    Response surface for E = 5 MPa. x and y-axis are design parameters, z-axis is objective function.
  </small>
</p>

### Acknowledgments

I'd like to thank Professor Amir Hooshiar for his supervision and support.