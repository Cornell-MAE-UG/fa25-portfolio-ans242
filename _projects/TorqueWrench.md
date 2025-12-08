---
layout: project
title: Torque Wrench Design
description: Mechanics of Engineering Materials Final Project
technologies: [Autodesk Fusion, ANSYS, MATLAB]
image: /assets/images/radio-machine-cad.jpg
---

For my final project in MAE 3270, I designed an optimized torque wrench.

Here is the CAD model of my Wrench Design: 

![CAD]({{ "/assets/images/TWCAD.png" | relative_url }}){: .inline-image-r style="width: 200px"}

Material Selection

Material: Aluminum 7075-T6 

Young’s Modulus (E): 10.3×10⁶ psi

Poisson’s Ratio (ν): 0.33

Allowable Stress (≈ Yield Strength): 73,000 psi (73 ksi)

Fracture Toughness (K_IC): 25,000 psi·√in

Fatigue Strength (at 1×10⁶ cycles): 23,000 psi

FEM Load and Boundary Conditions

Normal Strain Contours

Maximum Principal Stress Contour

![Principal Stress Contour]({{ "/assets/images/RealMaxPrincipalStressTW.png" | relative_url }}){: .inline-image-l}

FEM Summary Results:

Max Normal Stress: 59230 Psi

Load Point Deflection: 0.71213 in

Strains at Gauge: 

Normal - X Axis,−4.518e-004 in/in

Normal - Y Axis,−4.7377e-004 in/in

Normal - Z Axis,1.3979e-003 in/in

Torque Wrench Sensitivity: 1.3979 mV/V

Strain Gauge Selection:

Optical foil strain gauges 

Dimensions: 4x7 mm

