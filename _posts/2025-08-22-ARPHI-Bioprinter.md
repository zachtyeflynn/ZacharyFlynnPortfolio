---
title: "ARPHI Bioprinter"
layout: single
date: 2025-08-22
highlight: true
highlight_order: 2
classes: wide
toc: true
categories: [Projects]
excerpt: "Soft robotic bioprinter for esophogeal surgery."
header:
  teaser: /assets/videos/ARPHI_demo.gif
tags:
  - ROS 2
  - C++
  - Arduino
  - Python
  - Fusion 360
  - Electronics
---

<img src="{{ '/assets/videos/ARPHI_demo.gif' | relative_url }}"
     style="display: block; width: 75%; border-radius: 8px; margin: 0 auto; box-shadow: 0 4px 8px rgba(0,0,0,0.1);"
     alt="ARPHI demo animation">

<img src="{{ '/assets/videos/AR4_demo.gif' | relative_url }}"
     style="display: block; width: 75%; border-radius: 8px; margin: 0 auto; box-shadow: 0 4px 8px rgba(0,0,0,0.1);"
     alt="AR4 demo animation">

[View the poster for this project.]({{ "/assets/files/ARPHI_Poster.pdf" | relative_url }})

### Executive Summary

- Assembled and repurposed the AR4 MK3 robotic manipulator from Annin Robotics into a soft robotic bioprinter prototype.

- Designed the mechanical enclosure for the electronics of the bioprinter on the end-effector.

- Wired the electronics of the robotic arm and bioprinter.

- Developed a custom driver for the AR4 and the ARPHI bioprinter in ROS 2.

<div style="display: flex; gap: 5px; flex-wrap: wrap; align-items: flex-start;">

  <!-- Left image: 30% width, original aspect ratio -->
  <div style="flex: 0 0 25.32%;">
    <img src="{{ '/assets/images/Printhead.png' | relative_url }}"
         alt="Continuum printhead"
         style="width: 100%; height: auto; margin: 0 auto;border-radius: 8px;
                box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  </div>

  <!-- Right image: take remaining space, keep aspect ratio -->
  <div style="flex: 1 1 0;">
    <img src="{{ '/assets/images/Annotated_AR4.png' | relative_url }}"
         alt="Annotated AR4 diagram"
         style="width: 100%; height: auto; margin: 0 auto;border-radius: 8px;
                box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  </div>

</div>

<p style="margin-top: 0.5em;">
  <small>
    Continuum printhead designed by Swen Groen (<a href="https://doi.org/10.1016/j.device.2025.100973" target="_blank" rel="noopener">DOI</a>). The AR4 MK3 is a 3D-printed hobbyist robot made from off-the-shelf parts.
  </small>
</p>

### Bioprinter Enclosure CAD

- Optimized the layout, weight and spatial profile of the enclosure to fit the constraints of the AR4's payload.

- Fully parametrized with proper constraints for rapid prototyping.

<img src="{{ '/assets/images/Annotated_CAD_Rendering.png' | relative_url }}"
     alt="Workspace"
     style="display: block; width: 85%; margin: 0 auto; border-radius: 8px; 
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

<div style="display: flex; gap: 5px; flex-wrap: wrap; align-items: flex-start;">

  <!-- Left image: 30% width, original aspect ratio -->
  <div style="flex: 0 0 44.2%;">
    <img src="{{ '/assets/images/Enclosure.jpg' | relative_url }}"
         alt="Continuum printhead"
         style="width: 100%; height: auto; border-radius: 8px;
                box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  </div>

  <!-- Right image: take remaining space, keep aspect ratio -->
  <div style="flex: 1 1 0;">
    <img src="{{ '/assets/images/Enclosure_Render.png' | relative_url }}"
         alt="Annotated AR4 diagram"
         style="width: 100%; height: auto; border-radius: 8px;
                box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  </div>

</div>

### ROS 2 Control Driver

- Custom, low-latency driver which links the high-level control elements with the low-level code on the microcontrollers (Teensy 4.1 and Arduino Nano).

- Custom interfaces (for topics and services).

<img src="{{ '/assets/images/Operational_Diagram.jpg' | relative_url }}"
     alt="Workspace"
     style="display: block; width: 50%; margin: 0 auto; border-radius: 8px; 
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

[View the repository on GitHub.](https://github.com/zachtyeflynn/arphi_driver.git)

### Arduino & Electronics

- Prototyping with breadboard, stepper motors and microcontrollers.

- Experience with low-level embedded software development.

<img src="{{ '/assets/videos/Electronics.gif' | relative_url }}"
     style="display: block; width: 75%; border-radius: 8px; margin: 0 auto; box-shadow: 0 4px 8px rgba(0,0,0,0.1);"
     alt="AR4 demo animation">

### Acknowledgements

I'd like to thank Yitian Zhang for collaborating, Professor Audrey Sedal and Professor Matt Kinsella for supervising, as well as Swen Groen and Omar Peza Chavez for their support and contributions.