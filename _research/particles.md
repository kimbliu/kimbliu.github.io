---
layout: page
title: Separation of Inertial Particles
description:
img: assets/img/project_preview/particles_preview.png
importance: 2
category: Research
---

This project studies the segregation of inertial particles of different size in spatially and temporally varying flows. The clustering or mixing behavior of particles in these flows is strongly governed by particle density and size. We target the regime where Stokes number is order 1, and the difference between clustering and separation occurs over a highly narrow band.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/particle_path.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Displacement of two particles with 2% difference in particle relaxation time.
</div>

<br/>

The mixing behavior can be characterized by a Lyapunov exponent, measured by an exponential envelope fitted to particle displacement over time. Positive Lyapunov exponents represent separation and negative Lyapunov exponents represent clustering.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/lambda_map.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Lyapunov exponent map as a function of particle relaxation time and flow amplitude.
</div>

<br/>

We can then choose flow amplitudes such that a specific particle will behave differently from other particles present in the system, effectively separating different types of particles over sufficiently long time scales. Notably, the separated particle does not need to have the largest or smallest particle relaxation time because the bands of our Lyapunov exponent map are very narrow. In the video below, the blue particles are filtered from the red and green particles after approximately ten periods of temporal variation.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="assets/video/particle_sep.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Separation of particles. The blue particles have a particle relaxation time that lies between that of the red and the green particles.
</div>

<br/>

<p style="text-align:center;"><a href="https://kimbliu.github.io/research/">Back to Research</a></p>

#### References

Esmaily M, Mani A. "Modal analysis of the behavior of inertial particles in turbulence subjected to Stokes drag." <i>Physical Review Fluids</i>, 5(8): 084303, 2020.
