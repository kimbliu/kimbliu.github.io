---
layout: page
title: Macroscopic Forcing Method for Superhydrophobic Surfaces
description:
img: assets/img/project_preview/mfm_preview.png
importance: 1
category: Research
---

Superhydrophobic surfaces (SHS) are textured hydrophobic surfaces which have the ability to trap air pockets when immersed in water. This can result in significant drag reduction, due to the substantial effective slip velocity which forms at the surface. We seek to understand the difference in using a homogenized slip (Navier slip length) boundary condition and pattern-resolved slip boundary condition in the context of momentum mixing.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/shs.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Superhydrophobic surface geometries with streamwise-aligned ridges and square posts.
</div>

<br/>

The macroscopic forcing method (MFM) is a statistical technique that allows for direct measurement of the nonlocal eddy viscosity operator from DNS data. We use MFM to compare the eddy viscosity operators of a turbulent channel over patterned SHS of both boundary conditions in the limit of large pattern wavelength.

We futher extend the evaluation of nonlocal eddy viscosity to consideration of a nonlocal slip length operator. Though the slip length boundary condition has, in the past, been limited to dependence on local velocity gradients at the surface, we show that it can also depend on velocity gradients in a layer with finite thickness.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/eddy_viscosity.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/slip_kernel.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Nonlocal eddy viscosity. Right: Nonlocal slip length kernel.
</div>

<br/>


The usage of our measured nonlocal eddy viscosity and slip length operators significantly improves solutions to the Reynolds-averaged Navier Stokes (RANS) equations.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/rans.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    DNS mean velocity (Pattern-Resolved Slip) and solutions to the RANS equations with local and nonlocal operators.
</div>

<br/>

#### References

Seo J, Garcia-Mayoral R, Mani A. "Pressure fluctuations and interfacial robustness in turbulent flows over superhydrophobic surfaces." <i>Journal of Fluid Mechanics</i>, 783: 448-473, 2015.

Seo J, Mani A. "On the scaling of the slip velocity in turbulent flows over superhydrophobic surfaces." <i>Physics of Fluids</i>, 28(2): 025110, 2016.

Park D, Mani A. "Macroscopic forcing method: a tool for turbulence modeling and analysis of closures." <i>Physical Review Fluids</i>, 6(5): 054607, 2021.
