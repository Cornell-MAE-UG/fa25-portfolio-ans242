---
layout: project
title: "Glider Design Project"
subtitle: "AKA: Galider the Good"
date: 2025-12-12
image: assets/images/galiderCAD.png
tags: [glider, XFLR5, design]
---

### Summary
The goal of this project was to design a glider with a minimized cruise velocity while ensuring the aircraft can still travel the required distance of 20 meters when launched from a height of 5 meters. In order to achieve this goal, it was necessary to design a glider such that it would fly as close to stall as possible, maximize Cl/Cd such that it flies as efficiently as possible, maximize Cl such that the plane will fly as slow as possible without stalling, and maximize static margin to increase stability. In order to make design decisions, it was assumed that the velocity would be constant and the glider would trim to fly in a steady state. An iterative design process was used, including analytical calculations and XFLR5 analyses, to hone in on the finalized design. Initial estimates were made using general knowledge, best practices, and concepts from MAE 3050 (Intro to Aeronautics) lecture and discussion. Additionally, several test flights of the first iteration were conducted, and the results from them were used to inform the final design. The final design is a glider with a large aspect ratio, a relatively large static margin, and a maximized wingspan designed to fly at a low cruise velocity and high angle of attack.

<p align="center">
  <img src="{{ site.baseurl }}/assets/images/galiderDrawing.png" width="70%">
</p>

### Airfoil Selection
An analysis of multiple airfoil candidates was conducted using XFLR5 over the relevant Reynolds number range, and the S3021 was chosen because it performed best across all target categories throughout the range. The full analysis results are shown below. This analysis also produced an estimate of the CL at the target angle of attack, which was used to refine the calculations further. The S3021 (hot pink lines) performed the best according to the set targets. Most notably, it exhibited a CL/CD peak at the target alpha, a relatively high CL at the target alpha, and gentle stall characteristics beyond that. This airfoil was used for both the initial and final designs of the glider.

<div style="display: flex; justify-content: center;">
  <figure style="width:45%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/clafoil.png"
         alt="cl/alpha graph"
         class="project-image"
         style="width:100%;">
    <figcaption style="font-size: 0.85em; color: #777;">
      Cm vs Alpha
    </figcaption>
  </figure>
</div>

### Sizing Considerations
Material limits set an initial wingspan target of 1.5 m, but testing showed a 1.4 m wing provided the required stiffness by using the remaining spar length as a root doubler. With the final span selected, the lift equation was used to size the chord at 0.183 m and refine the Reynolds number, confirming the chosen airfoil remained valid.

After finalizing the wing dimensions, the fuselage length and empennage were sized using material constraints and standard aircraft design practices. The fuselage length was set to 0.91 m based on the available spruce stock, and wing placement was selected using Raymer’s conceptual design guidelines. Tail sizing was completed using the tail volume coefficient method and refined across iterations to improve static margin. A full CAD model was created to validate mass estimates.

A stability analysis was then performed in XFLR5 to determine ballast requirements and verify performance. The aircraft geometry and mass properties were modeled, with a NACA 0004 as the horizontal and vertical stabilizers’ airfoil even though the true design used a simple flat plate. Results showed lift and efficiency close to predictions, with stable longitudinal and lateral modes and an expected mildly unstable spiral mode with acceptable time-to-double behavior.

<div style="display: flex; justify-content: center;">
  <figure style="width:45%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/cma.png"
         alt="cm/alpha graph"
         class="project-image"
         style="width:100%;">
    <figcaption style="font-size: 0.85em; color: #777;">
      Cm vs Alpha
    </figcaption>
  </figure>
</div>

<div style="display: flex; gap: 10px; justify-content: center; align-items: flex-start;">
  <figure style="width:48%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/cla.png"
         alt="cl/alpha graph"
         class="project-image"
         style="width:100%;">
    <figcaption style="font-size: 0.85em; color: #777;">
      CL vs Alpha
    </figcaption>
  </figure>

  <figure style="width:48%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/clcda.png"
         alt="cl/cd/alpha graph"
         class="project-image"
         style="width:100%;">
    <figcaption style="font-size: 0.85em; color: #777;">
      CL/CD vs Alpha
    </figcaption>
  </figure>
</div>

### Construction
We were given a limited amount of spruce, glue, clay, and tissue paper, with complete freedom in all other design choices. To maximize precision and consistency, we laser-cut our airfoils, which required CAD modeling and layout optimization to fit as many ribs as possible onto each plank.

<p align="center">
  <img src="{{ site.baseurl }}/assets/images/lasercuts.png" width="70%">
</p>


### Results
On the last day of class, there was a glider performance competition. Out of 15 teams, our glider placed second and flew the farthest distance! 

<div style="display: flex; justify-content: center; margin: 20px 0;">
  <video width="70%" controls>
    <source src="{{ site.baseurl }}/assets/images/gliderfly.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

<div style="display: flex; gap: 10px; justify-content: center; align-items: flex-start;">
  <figure style="width:48%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/gliderpic.png"
         alt="drone in flight"
         class="project-image"
         style="width:100%;">
    <figcaption style="font-size: 0.85em; color: #777;">
      final product
    </figcaption>
  </figure>

  <figure style="width:48%; text-align:center;">
    <img src="{{ site.baseurl }}/assets/images/airyay.png"
         alt="Hands-on fabrication of Magnus Effect drone"
         class="project-image"
         style="width:100%;">
    <figcaption style="font-size: 0.85em; color: #777;">
      the team and our award!
    </figcaption>
  </figure>
</div>