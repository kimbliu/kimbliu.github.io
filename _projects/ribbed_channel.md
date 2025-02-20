---
layout: page
title: Conjugate Heat Transfer in a Ribbed Channel
description: Final project for ME469 (Computational Methods in Fluid Dynamics)
img:
importance: 3
category: Classes
---

This project was performed in collaboration with [Carlos Gonzalez](https://cagonzal.github.io). Following the work in [Conjugate heat transfer in a channel with staggered ribs](https://www.sciencedirect.com/science/article/pii/0017931085901425), we use Nalu, a second-order, unstructured, multiphysics flow solver from Sandia Labs, to perform conjugate heat transfer (CHT) simulations of fluid flow through a ribbed channel. We extend previous analysis by allowing the thermal conductivity ratio $$k_{solid}/k_{fluid}$$ and the channel wall thickness ($$B/D$$) to vary.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/bd05_mesh.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Mesh of ribbed channel geometry.
</div>

<br/>

Our Nalu simulations were validated by comparing velocity fields from to the original work. The recirculation zones behind the ribs are relatively small and the perturbation to the freestream in the wall-normal direction is limited.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/pv_streamlines.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Streamlines of velocity field.
</div>

<br/>

We find that increasing wall thickness decreases therib heat transfer. The thicker wall provides a larger "capacitance" that the applied heat flux boundary condition must overcome before being exposed to the convective heat transfer of the mean channel flow.

Decreasing the thermal conductivity ratio counterintuitively increases rib heat transfer. The rib heat transfer is measured at the base of the rib and not along the surface area. This increase in rib heat transfer is because, at very low thermal conducitvity ratios, the rib acts as more volume to "store" heat, rather than more surface area to convect heat. That is, more heat is transferred through the rib itself.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/Qr_vs_BD.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/Qr_vs_kr.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Variation of rib heat transfer with wall thickness. Right: Variation of rib heat transfer with thermal conductivity ratio.
</div>

<br/>

<p style="text-align:center;"><a href="https://kimbliu.github.io/projects/">Back to Projects</a></p>

#### References

Webb BW, Ramadhyani S. "Conjugate heat transfer in a channel with staggered ribs." <i>International Journal of Heat and Mass Transfer</i>, 28(9): 1679-1687, 1985.
