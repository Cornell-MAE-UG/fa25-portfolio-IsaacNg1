---
layout: project
title: Modelling Washing Machine Shock Absorber
description: Dissection and Model of Shock Absorber
technologies: [System Modelling]
image: /assets/images/DissectedSA.jpg
---

This project focuses on modeling the behavior of a washing machine shock absorber using ordinary differential equations and state-space methods. While the system was studied at both the component and system level, my primary contribution was analyzing the shock absorber as part of the full washing machine under unbalanced excitation. This approach allowed me to study how the added mass of the drum, clothes, and water affects the overall vibration response and the role of the shock absorber in reducing those oscillations.

Components of a Washing Machine Suspension:
1. The effective mass from the drum and wet clothes
2. The Shock Absorbers acting as spring-damper with friction
    a. Spring force from the compressed foam expanding
    b. Coulomb friction force from the slider rubbing on the foam
3. Disturbance input from the unbalanced clothes or controller input from applied force

![Shock Absorber within Washing Machine]({{ "/assets/images/SAinWM.jpg" | relative_url }})

This is how I modeled the shock absorber within the washing machine

![Photo of ODE]({{ "/assets/images/SA-FinalODE.jpg" | relative_url }})

The two state-space models are also different because they come from different physical assumptions about the system. The standard form shown in the second section represents a classic SMD system with viscous damping.

My state space model is based on the washing machine shock absorber with friction and forcing from the unbalanced drum.

![Photo of State Space]({{ "/assets/images/SA-StateSpace.jpg" | relative_url }})
