---
layout: project
title: Simulating a MEMS actuator
permalink: /simulation/onmemsactuator/
image: ../../assets/images/mems+actuator.png
---
At the Center for Bits and Atoms (CBA), I worked with Dr. Prashant Patil who was designing microscale lego pieces made of various semiconductor materials that could click together to form transistors and other components of circuits that were reusable and redistributable – components could be taken apart and reconfigured into other types of components reducing material cost, and increasing recyclability thereby reducing waste. In other aspects of my life, I was coordinating efforts to reduce waste across campus through UA Sustainability and this research allowed me to attack this issue through a different angle: electronic waste. Electronic components are notoriously difficult to recycle, requiring special equipment and extra labor for full recyclability; this means most old electronics go straight to landfill due to the high investment required to properly extract and reuse the materials that construct them. If electronics were designed from the outset to be recyclable and reusable, resources could be saved in material extraction and less waste could also be produced – a circular manufacturing cycle from the outset.

To support the construction of these components, I designed and simulated a microelectromechanical system (MEMS) actuator that could function as a stage atop which the microscale lego pieces could be assembled. The actuator relied on electrostatic comb drives for mechanical motion – when voltage is applied between fixed and movable comb features, electrostatic attraction is generated and the comb fingers draw together connected by spring flexures, moving the stage along with them; other sets of comb drives cause movement in other directions. I designed this actuator using SolidWorks and then used both SolidWorks and COMSOL Multiphysics to simulate mechanical deformation and electrostatic behavior. This required me to learn how to use COMSOL from scratch, a simulation tool that no one else in the research group had experience with. Through consulting documentation in detail and many rounds of trial and error, I was able to use COMSOL to model MEMS stage mechanical deformation and electrostatic effects due to voltage application, confirm stage actuation, and ensure mechanical stress on the spring flexure system was not above the material’s yield strength. After confirmation that this design would meet desired actuation parameters, Dr. Patil manufactured and tested the MEMS stage using deposition, spinning and etching techniques. This device became a part of Dr. Patil’s novel array of techniques, featured in his dissertation, for designing reconfigurable MEMS devices and electronics.

<div class="img-with-caption">
  <img src="{{ '/assets/images/mems+actuator.png' | relative_url }}" alt="top view of designed mems actuator"/>
  <p class="caption">
    Top view of designed MEMS actuator.
  </p>
</div>

<div class="img-with-caption">
  <div class="gallery two">
    <img src="{{ '/assets/images/memsmodelling1.png' | relative_url }}" alt="1 view of modelling motion of MEMS actuator"/>
    <img src="{{ '/assets/images/memsmodelling2.png' | relative_url }}" alt="another view of modelling motion of MEMS actuator"/>
  </div>
  <p class="caption">
    Modelling movement of MEMS actuator in COMSOL Multiphysics.
  </p>
</div>