---
title: "Robust Controller Design"
layout: single
date: 2025-12-22
highlight: false
categories: [Projects]
excerpt: "Designed a controller for the McGill Formula Electric car (MECH 513)."
header:
  teaser: /assets/images/Block_Diagram.jpg
tags:
  - Python
  - Python Control
  - dkpy
---

<img src="{{ '/assets/images/Full_Block_Diagram.jpg' | relative_url }}"
     alt="Workspace"
     style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em;">
  <small>
    Block diagram of the control system used in the project.
  </small>
</p>

### Executive Summary

- Designed a robust yet optimal controller for the water pump on the McGill Formula Electric car.

- Performed system ID of the water pump's dynamics, characterized its uncertainty.

- Used mu-synthesis and DK iteration to design the controller using Python Control and dkpy.

- Reduced the power consumption of the water pump by 30 %.

### System Identification and Uncertainty Modelling

- Fit a first-order linear transfer function & inverse multiplicative uncertainty model to the system ID data.

- Validated model on test data to ensure acceptable error.

<img src="{{ '/assets/images/FreqDomainVis.png' | relative_url }}"
     alt="Workspace"
     style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em;">
  <small>
    Linear and nonlinear least squares fit of a first-order plant to the water pump data collected.
  </small>
</p>

<img src="{{ '/assets/images/IMUncertainty.png' | relative_url }}"
     alt="Workspace"
     style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em;">
  <small>
    Inverse multiplicative uncertainty model based on the variation between system IDed plants.
  </small>
</p>

<img src="{{ '/assets/images/Error.png' | relative_url }}"
     alt="Workspace"
     style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em;">
  <small>
    Validation of system IDed plant on test data.
  </small>
</p>

### Controller Design Via mu-Synthesis

- Implemented the block diagram of the control system in Python Control and setup dkpy for mu-synthesis.

- Input a reference flow output for the controller to track.

<img src="{{ '/assets/images/Result_Controller.png' | relative_url }}"
     alt="Workspace"
     style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<p style="margin-top: 0.5em;">
  <small>
    Final result of the controller to track a reference for the water pump. Discrepencies are caused by simulated noise.
  </small>
</p>

### Acknowledgements

This was the final project for MECH 513: Control Systems at McGill University. I'd like to thank Professor James Richard Forbes and the McGill Formula Electric team for formulating this project. Further, I'd like to thank Christopher Zhang for collaborating.

I must withhold specfic details about our implementation and restrict access to our GitHub repository as to not violate McGill University's academic integrity policy as well as respect Professor Forbes' intellectual property.