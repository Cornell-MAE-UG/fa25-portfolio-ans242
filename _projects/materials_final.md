---
layout: project
title: "Torque Wrench Design & Finite Element Analysis - MAE 3270 Final Project"
subtitle: ""
date: 2025-12-05
image: assets/images/materials-final/cadRender.jpg
tags: [materials, fem, analysis]
---

### Summaryof design
The goal of this project was to design a non-ratcheting torque wrench capable of meeting several design and performance specifications. I used a MATLAB script to perform analytical calculations and run through possible designs. Using the best result from the script, I then CADed a model in Fusion360 and created a Finite Element Model (FEM) using Ansys Static Structural. I conducted analysis and then compared it to the results of the analytical calculations.

---

### 1) CAD Model
<div class="image-block-full">
  <img src="{{ site.baseurl }}/assets/images/materials-final/TWCAD.png" alt="CAD model with key dimensions" class="project-image" style="width:100%;">
</div>

---

### 2) Material & Relevant Mechanical Properties
Material: Aluminum 7075-T6

E = 71 GPa (= 10.3 Msi)

ν = 0.33

σᵧ ≈ 503 MPa (= 73 ksi) (allowable ≈ yield)

Fracture toughness K₁C ≈ 27.5 MPa√m (= 25 ksi√in)

Fatigue strength ≈ 159 MPa (= 23 ksi) (~10⁶ cycles)

Source: Aluminum Association / MIL-HDBK-5 / Ansys Granta

---

### 3) Finite Element Model Setup (Loads and Boundary Conditions)
<div class="image-block-full">
  <img src="{{ site.baseurl }}/assets/images/materials-final/CTW.jpeg" alt="Loads and boundary conditions" class="project-image" style="width:100%;">
</div>
- Constraints: four faces of the block above the drive were constrained to have zero displacement
- Load: A load of 600 lbf * in was applied at the end of the wrench handle

---

### 4) Normal Strain Contours
<div class="image-block-full">
  <img src="{{ site.baseurl }}/assets/images/materials-final/straincontourREAL.png" alt="Normal strain contours in gauge direction" class="project-image" style="width:100%;">
</div>

---

### 5) Maximum Principal Stress Contour
<div class="image-block-full">
  <img src="{{ site.baseurl }}/assets/images/materials-final/RealMaxPrincipalStressTW.png" alt="Maximum principal stress contour" class="project-image" style="width:100%;">
</div>

---


### 7) Max Normal Stress
- **Value:** **1.457 x 10^5 psi**

<div class="image-block-full">
  <img src="{{ site.baseurl }}/assets/images/materials-final/StressTW.png"
       alt="Max normal stress contour from FEM">
</div>

---

### 8) Deflection at Load Point
- **Value: 0.8275 in**

<div class="image-block-full">
  <img src="{{ site.baseurl }}/assets/images/materials-final/DeformationTW.png"
       alt="Deflection field and load-point displacement">
</div>

---


### 9) Strain at Gauge
- **Value:** **1599.3 µε** at the set gauge location

<div style="display:flex; gap:1rem; clear:both; width:100%; margin:1rem 0 2rem;">
  <!-- Main image (~2/3 width) -->
  <div style="flex:2 1 0; min-width:0;">
    <img src="{{ site.baseurl }}/assets/images/materials-final/ProbeStrain.png"
         alt="Strain at gauge location (field view)"
         style="display:block; width:100%; height:auto;">
  </div>


---

### 10) Torque-Wrench Sensitivity
- Measured strain from the strain gauge in the model **ε = 1,397.9 µε**
- Gauge factor: **K = 2**
- Bridge setup used:  **half**
- **Sensitivity: 1.398 mV/V** - meets the required criteria
<div style="display:flex; gap:1rem; clear:both; width:100%; margin:1rem 0 2rem;"> <div style="flex:2 1 0; min-width:0;"> <!-- (Add image here if you have one; otherwise this box stays empty like #9’s structure) --> </div> </div>


---

### 11) Strain Gauge Selection
- Gauge Type: **Bonded Foil Strain Gauge**
- Dimensions: **~ 7mm x 4mm**
- Bonding area on the part is larger than this, providing enough room
<div style="display:flex; gap:1rem; clear:both; width:100%; margin:1rem 0 2rem;"> <div style="flex:2 1 0; min-width:0;"> <!-- (Optional image slot, matching #9’s formatting) --> </div> </div>
