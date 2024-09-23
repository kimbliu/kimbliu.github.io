---
layout: page
title: Application of Lagrangian Dynamic SGS in Wall-Modeled LES
description: Final project for ME461 (Advanced Topics in Turbulence)
img:
importance: 2
category: Classes
---

The goal of this project was to follow the procedures described in [A Lagrangian dynamic subgrid-scale model of turbulence](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/lagrangian-dynamic-subgridscale-model-of-turbulence/783398B2D0BE53C120151E4E911CA833) and evaluate the model performance for fully developed channel flow. A Lagrangian time averaging method is applied to the dynamic Smagorinsky model to eliminate negative eddy viscosities in flows with inhomogeneity. The original paper tested this method for isotropic turbulence and channel flow simulated with wall-resolved LES. In this project, we evaluate the method's applicability to wall-modeled LES (WMLES).

Embedded in the dynamic Smagorinsky model are two main assumptions: that the Smagorinsky coefficient $$c_s$$ does not vary significantly in space and that $$c_s$$ does not change with different filter size. In practice, these two assumptions are not always true; consequently, $$c_s$$ coefficients can be highly oscillatory and often negative, which can lead to numerical instability.

We motivate the time averaging method by first examining the variation in $$c_s$$ for forced HIT data from Shirian et al. 2022. In the figure below, the model coefficients are computed from instantaneous fields, and then averaged in two homogeneous directions. The $$c_s$$ values clearly vary in space, show low correlation between two filter sizes, and are negative in multiple locations.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/men_hit_local.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/hit_cs_local.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Model coefficient computed from instantaneous fields. Left: Meneveau et al. Right: Our analysis.
</div>

<br/>

An Eulerian time averaging decreases spatial variation and improves correlation between filter widths, however the issue of negative $$c_s$$ persists.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/hit_rms.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Root mean square values of the model coefficient, as a function of time. With Eulerian averaging, the RMS values converge quickly.
</div>

<br/>

A pre-existing WMLES code for channel flow ($$Re_\tau = 180$$) was modified to include the Lagrangian dynamic model. Mean velocity and RMS velocity profiles in the Lagrangian averaged framework match well with expected channel statistics.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/vel_profile.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/rms_legend.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Mean velocity profile of fully developed turbulent channel flow. Right: RMS velocities from plane averaging and Lagrangian averaging.
</div>

<br/>

Unfortunately, our implementation of the Lagrangian model in WMLES is highly numerically unstable. The coarse grid that we are allowed with wall modeling is in conflict with the multilinear interpolation required at each time step for the Lagrangian time averaging method, and thus requires a prohibitively small timestep. For complex geometries, this is not a sustainable way of maintaining the linear approximation assumption.

<br/>

<p style="text-align:center;"><a href="https://kimbliu.github.io/projects/">Back to Projects</a></p>

#### References

Meneveau C, Lund TS, Cabot WH. "A Lagrangian dynamic subgrid-scale model of turbulence." <i>Journal of Fluid Mechanics</i>, 319: 353-385, 1996.

Shirian Y, Mani A. "Eddy diffusivity operator in homogeneous isotropic turbulence." <i>Physical Review Fluids</i>, 7(5): L052601, 2022.

Bae HJ, Lozano-Duran A, Bose ST, Moin P. "Dynamic slip wall model for large-eddy simulation." <i>Journal of Fluid Mechanics</i>, 859: 400-432, 2019.
