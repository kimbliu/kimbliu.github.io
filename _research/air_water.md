---
layout: page
title: Modeling of Dynamic Air-Water Interfaces for Drag Reduction
description:
img: assets/img/bubble_model.png
importance: 1
category: Research
related_publications: true
---

This project is motivated by a series of experiments carried out at Caltech by [Cong Wang](https://engineering.uiowa.edu/directory/cong-wang) and [Mory Gharib](https://www.gharib.caltech.edu) on superhydrophobic surfaces. These experiments were able to maintain stable oscillating air films in a turbulent boundary layer, and achieved up to 30% drag reduction in certain cases. The goal of this work is to use direct numerical simulation to develop quantitative understanding of the role of bubble oscillation in modifying drag.

We introduce a single-phase bubble model to perform computationally intensive simulations in a turbulent periodic channel. Shear-free boundary conditions in the wall-tangential directions are applied on the air-water interface. In the wall-normal direction, we apply a linearized velocity boundary condition calculated from experimental height measurements. 

In quiescent flow, this bubble model accurately captures the wall normal velocity field far from the interface.

<div class="row">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bubble_model.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/far_field.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>

We further validate our single-phase model by comparing the drag reduction of a single bubble in laminar boundary layer flow to analogous results from multiphase simulations.

<!--
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid loading="eager" path="assets/video/bub_profile.mp4" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>
-->

<video autoplay="autoplay" loop="loop" width="768" height="512">
  <source src="/assets/video/bub_profile.mp4" type="video/mp4">
</video>

