---
layout: project
title: "Static Thrust Testing Rig"
subtitle: "AKA: do we have enough power?"
date: 2025-9-12
image: assets/images/rigCAD.png
tags: [thrust, testing, modelling]
---

**Design**  
A big part of making our plane fly is picking out the best possible propulsion system. Since small changes in motors, propellers, or batteries can make a big difference in performance, we needed a way to directly test and compare different setups. To do this, I designed and built a thrust testing rig with the motor mounted at the center of a wooden plank. The rig was intentionally constructed from wood to maximize flexibility, allowing mounting locations to be easily drilled and adjusted as testing needs evolved. This design made it straightforward to reposition the motor between tests and left the option open to adapt the rig for dual-motor testing in the future if required.

<p align="center">
  <img src="{{ site.baseurl }}/assets/images/rigpic.png" width="70%">
</p>

**Method**  
As the propeller rotates, it generates a moment about the axle, causing the lower beam of the rig to press down on a built-on load cell. Because the two beams of the rig are equal in length away from the pivot point, the force measured by the load cell (mass multiplied by gravitational acceleration) directly corresponds to the thrust produced by the motor.  

For each propeller configuration, tests were run using the aircraft’s flight controller, with the throttle manually ramped to full and maintained for five minutes to replicate competition flight conditions.

<div style="display: flex; gap: 10px; justify-content: center; align-items: flex-start;">
  <figure style="width:48%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/rigphysics.jpeg"
         alt="rig physics"
         class="project-image"
         style="width:100%;">
  </figure>

  <figure style="width:48%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/hugosmirk.png"
         alt="image during test"
         class="project-image"
         style="width:100%;">
  </figure>
</div>

**Electrical and Battery Data Integration**  
In addition to measuring thrust with the load cell, I wanted to add a battery monitoring setup to the static thrust test to track voltage, current, and power. As lead, I worked with one of my Electrical and Computer Engineering subteam members to make this possible. An INA226EVM and shunt resistor were integrated into the existing test circuit to monitor both the ESC and battery power lines. Data from the INA226EVM was sent to the Arduino over I²C and synced with thrust data from the HX711 load cell. The Arduino logged everything together and exported the results to an Excel spreadsheet for analysis, allowing us to see how different throttle settings impacted battery usage over time.


<p align="center">
  <img src="{{ site.baseurl }}/assets/images/wiringdiagram.png" width="70%">
</p>

**Results**  
This year, we were considering a few different motor–battery configurations for our aircraft. To find the best one, we ran static thrust tests across multiple propeller and battery combinations and recorded thrust–throttle data for each setup. This allowed us to directly compare the performance of a 4200 mAh battery versus a 4500 mAh battery under the same conditions.  

We also compared the experimental results to MATLAB-based performance predictions generated using propeller data and basic motor and battery equations to estimate steady-state behavior at different throttle settings. While the overall trends aligned well, the measured static thrust values were typically about 1–2 kg lower than the predicted values, highlighting real-world losses not captured in the models and potentially indicating sources of error in the thrust rig itself.

<p align="center">
  <img src="{{ site.baseurl }}/assets/images/thrustresults.png" width="70%">
</p>

**Future Improvements**  
In the future, it could make sense to transition this rig to a metal structure and add automated throttle ramp-up and data collection for more repeatable testing. For now, though, wood was a great choice. It was inexpensive, easy to get, and simple to modify as the design evolved. It let us build and iterate quickly, and it ultimately got the job done well without adding unnecessary complexity.

<div style="display:flex; gap:10px; justify-content:center; align-items:flex-start;">
  <figure style="width:48%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/rigconstruct.png"
         alt="Sawing wood"
         style="width:100%; height:300px; object-fit:cover; border-radius:8px;">
  </figure>

  <figure style="width:48%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/shopping.jpeg"
         alt="Buying wood"
         style="width:100%; height:300px; object-fit:cover; border-radius:8px;">
  </figure>
</div>
