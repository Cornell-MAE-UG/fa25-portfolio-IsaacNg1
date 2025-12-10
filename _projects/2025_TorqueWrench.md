---
layout: project
title: Torque Wrench
description: Comparing ANSYS FEM values and MatLAB hand calculations of a iterated torque wrench
technologies: [MATLAB, Solidworks CAD, ANSYS FEM]
image: /assets/images/Deformation.jpg
---

Here are images of my CAD with key dimensions

![CAD]({{ "/assets/images/TorqueWrenchCAD.jpg" | relative_url }}){: .inline-image-r}
![CADTopPlane]({{ "/assets/images/TopPlane.jpg" | relative_url }}){: .inline-image-r}
![CADRightPlane]({{ "/assets/images/RightPlane.jpg" | relative_url }}){: .inline-image-r}

The torque wrench was manufactured using Ti-6Al-4V, a widely used aerospace-grade titanium alloy chosen for its balanced combination of strength, toughness, and deformation behavior. Ti-6Al-4V has a Young’s modulus of approximately 16.1 Msi, which is significantly lower than that of steels and allows the wrench to generate higher elastic strain under the applied bending moment. This property directly supports the requirement of achieving at least 1.0 mV/V output from the strain gauge, since strain is inversely proportional to modulus. The alloy provides a tensile strength of about 160 ksi, which ensures that the maximum bending stress in the design remains far below material limits and results in a strength safety factor well above the required value. One of the most important properties for this application is the alloy’s high fracture toughness, around 82 ksi√in, which offers substantial resistance to crack initiation and growth, especially given the assumed surface flaw size in the analysis. Ti-6Al-4V also exhibits strong fatigue performance, with a fatigue strength near 100 ksi at 10⁶ cycles, allowing the wrench to endure repeated loading without risk of fatigue failure.

Here is a diagram of how Loads and Boundary Conditions were applied to my FEM model

![Loads and BC]({{ "/assets/images/Loads_BC.jpg" | relative_url }}){: .inline-image-r}

Here are the normal strain contours from my FEM 

![normalstrain]({{ "/assets/images/NormalStrainContours.jpg" | relative_url }}){: .inline-image-r}

Here are a summary of results from FEM highlighting Max Normal Stress, Load Point Deflection, and Strains the Strain Gauge Location

![Max Normal Stress]({{ "/assets/images/MaxPrincipalStress.jpg" | relative_url }}){: .inline-image-r}

In the image, the max principal stress is given by 23.7ksi because of a stress concentration on the top plane. Using the probe tool, the max stress found on the normal surface was found to be closer to 18ksi, which is consistent with the MatLAB hand calcs. The MatLAB script found the max normal stress to be 18.02ksi

![Load Point Deflection]({{ "/assets/images/Deformation.jpg" | relative_url }}){: .inline-image-r}

The FEM model found the max deflection at the load point to be 0.265 in which is consistent to the matLAB deflection of 0.2716 in

![Strain Probe]({{ "/assets/images/Strain Probe.jpg" | relative_url }}){: .inline-image-r}
![Strain Gauge Results]({{ "/assets/images/StrainGaugeResults.jpg" | relative_url }}){: .inline-image-r}

In the image of the results, the strain in the Normal X-axis is given by 1101.3 microstrain which is consistent with the matLAB value of 1119 microstrain

Using the strain obtained from the FEM analysis, the torque-wrench sensitivity was calculated directly from the strain-gauge half-bridge relationship. The maximum normal strain in the gauge region was approximately 1101 microstrain. Applying the half-bridge output equation Vout/Vin = (GF/2)ϵ with a gauge factor of 2.0 gives a predicted sensitivity of 1.10 mV/V. This value exceeds the required minimum of 1.0 mV/V and closely matches the analytical prediction of 1.119 mV/V, confirming that the final geometry provides sufficient strain for accurate torque measurement.

Here is the strain gauge that I found that would fit within my design:

![Strain Gauge]({{ "/assets/images/straingaugeproduct.jpg" | relative_url }}){: .inline-image-r}
![Strain Gauge Dim]({{ "/assets/images/SGdimensions.jpg" | relative_url }}){: .inline-image-r}




