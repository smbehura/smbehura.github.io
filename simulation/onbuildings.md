---
layout: project
title: 'Simulating building energy and lighting to evaluate alternative, sustainable materials'
permalink: /simulation/onbuildings/
image: /assets/images/selco_buildingview1.png
---
While my experiences at MIT through both coursework and research taught me a lot about the fundamentals of materials, the process of research, and allowed me to gain confidence in developing and using new technical skills, I had less opportunity to work on projects that were then implemented at scale and used by real users. To take those skills to the real world, I started a technology and design fellowship at the SELCO Foundation in Bangalore, India, supported by MIT’s MISTI program which connects and funds students for international internships and fellowship programs. I chose SELCO Foundation because it worked on addressing rural India gaps in services including electricity and healthcare by designing low-cost, decentralized technological solutions. Over the seven months I worked at SELCO Foundation, I had the opportunity to work on several technology and design projects ranging from a solar-powered neonatal care unit designed for rural healthcare centers to solar-powered, portable water pumps to building energy and light simulations. Many projects centered on rethinking the design and structure of an existing solution to be more mobile, lightweight or otherwise fit for rural conditions. For example, my work on a portable, solar-powered water pump involved designing ways for solar panels to be cheaply reconfigurable to make them both easy to transport over rough terrain when moving between agricultural fields and easy to deploy when powering the water pump.

<div class="img-with-caption">
  <div class="gallery two">
    <img src="{{ '/assets/images/solarpump1.png' | relative_url }}" alt="isometric view of solar water pump solution"/>
    <img src="{{ '/assets/images/solarpump2.png' | relative_url }}" alt="top view of solar water pump solution"/>
  </div>
  <p class="caption">
    Example views of portable structure developed for solar water pump (works in progress)
  </p>
</div>

Another key project in collaboration with the Built Environment team was developing a simulation tool that was able to take as input a building design, the materials used to construct the building and the location of the building and predict living environment conditions like radiant temperature, illumination levels and relative humidity for different activities. The team was focused on using locally-sourced, sustainable materials to build rural infrastructure related to government services and livelihoods, both to reduce carbon emissions in construction and institute cheaper and more sustainable maintenance cycles. There were many uncertainties in how locally-sourced materials would compare to more conventional materials in creating comfortable living and working environments so the simulation tool served as a first step in affirming these materials were viable alternatives to the more carbon-intensive default options. To set up this tool, I used Rhino to construct building architectures, Grasshopper to apply different conditions on the architecture including material properties and integrated Honeybee (an open source Grasshopper integration) to connect Grasshopper to simulation engines like EnergyPlus/OpenStudio (used for building energy and thermal comfort) and Radiance (used for daylighting simulation). Finally, I used Ladybug (another Grasshopper integration and part of the Honeybee suite of tools) to visualize and apply location-specific weather data to my Grasshopper simulation. Using this tool, I was able to determine the amount of dehumidification needed in a Gudalur, Tamil Nadu-based storage facility dedicated to the drying of coffee cherries based on information like facility architecture, temperature and relative humidity. In another application, I was able to recommend better materials and efficient lighting requirements for the design and construction of two rural healthcare centers in Keba, Arunachal Pradesh and Gumballi, Karnataka by constructing the suggested centers in Rhino and performing temperature and daylighting simulations. Specifically, incorporating an air gap and bison board as roofing insulation dropped indoor and outdoor temperatures by as much as 10℃. These differences seen in simulation were later confirmed by construction and testing at the actual sites themselves. I developed a simulation workflow template, documented it in detail and trained the Built Environment team on the use of the tools and workflow for future built environment projects that would benefit from prior simulation analysis.

<div class="img-with-caption">
  <div class="gallery two">
    <img src="{{ '/assets/images/selco_buildingview1.png' | relative_url }}" alt="view 1 of rural healthcare center constructed in rhino" width="900"/>
    <img src="{{ '/assets/images/selco_buildingview2.png' | relative_url }}" alt="view 2 of rural healthcare center constructed in rhino" width="900"/>
  </div>
  <p class="caption">
    Views of rural healthcare center constructed in Rhino.
  </p>
</div>


<div class="img-with-caption image-combo">
  <div class="image-combo-main">
    <img src="{{ '/assets/images/selco_coffeecherrystoragefacility.png' | relative_url }}" 
         alt="humidity simulation of coffee cherry storage facility">
  </div>

  <div class="image-combo-grid">
    <img src="{{ '/assets/images/selco_consultwallsurface0.png' | relative_url }}" alt="surface temperature simulation of consult wall surface 0">
    <img src="{{ '/assets/images/selco_consultwallsurface1.png' | relative_url }}" alt="surface temperature simulation of consult wall surface 1">
    <img src="{{ '/assets/images/selco_consultwallsurface2.png' | relative_url }}" alt="surface temperature simulation of consult wall surface 2">
    <img src="{{ '/assets/images/selco_consultwallsurface3.png' | relative_url }}" alt="surface temperature simulation of consult wall surface 3">
  </div>

  <p class="caption">
    (left to right) Relative humidity comparison of Gudalur, Tamil Nadu-based storage facility; temperature simulation of rural healthcare center.
  </p>
</div>