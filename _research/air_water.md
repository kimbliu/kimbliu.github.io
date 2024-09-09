---
layout: page
title: Modeling of Dynamic Air-Water Interfaces for Drag Reduction
description:
img: assets/img/project_preview/air_water_preview.png
importance: 1
category: Research
---

This project is motivated by a series of experiments carried out at Caltech by [Cong Wang](https://engineering.uiowa.edu/directory/cong-wang) and [Mory Gharib](https://www.gharib.caltech.edu) on superhydrophobic surfaces. These experiments were able to maintain stable oscillating air films in a turbulent boundary layer, and achieved up to 30% drag reduction in certain cases. The goal of this work is to use direct numerical simulation to develop quantitative understanding of the role of bubble oscillation in modifying drag.

We introduce a single-phase bubble model to perform computationally intensive simulations in a turbulent periodic channel. Shear-free boundary conditions in the wall-tangential directions are applied on the air-water interface. In the wall-normal direction, we apply a linearized velocity boundary condition calculated from experimental height measurements. 

In quiescent flow, this bubble model accurately captures the wall normal velocity field far from the interface.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bubble_model.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/far_field.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Schematic of single-phase bubble model. Right: Far field velocity profiles from experiments and simulations.
</div>

<br/>

We further validate our single-phase model by comparing the drag reduction of a single bubble in laminar boundary layer flow to analogous results from multiphase simulations.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include video.liquid path="assets/video/bub_profile.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Oscillating dynamic air-water interface from multiphase diffuse interface simulation.
</div>


<!--
<video autoplay="autoplay" loop="loop" width="768" height="512">
  <source src="/assets/video/bub_profile.mp4" type="video/mp4">
</video>
-->

