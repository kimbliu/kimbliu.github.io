---
layout: page
title: Galilean Invariance Preserving Deep Learning for Canonical Fluid Flows
description: Final project for CS230 (Deep Learning)
img:
importance: 1
category: Classes
---

This project was performed in collaboration with [Carlos Gonzalez](https://cagonzal.github.io). The goal of the project was to use the Tensor Basis Neural Network (TBNN) to predict the Reynolds stress tensor for turbulent Couette flow and turbulent channel flow.

When using machine learning approaches for modeling physical problems, it is important that the output of the model obeys hte physical laws that are being analyzed. The TBNN preserves Galilean invariance, which states that the laws of physics do not change in different inertial frames of reference. Specifically, any scalar flow variable, such as pressure or velocity magnitude, should remain unchanged when the frame of reference is rotated, reflected, or translated.

Our dataset is periodic channel flow ($$Re_\tau \approx 180 - Re_\tau \approx 5200$$) and turbulent Couette flow ($$Re_\tau \approx 93 - Re_\tau \approx 500$$). from the UT Austin Oden Institute. We generated synthetic Reynolds-averaged Navier-Stokes (RANS) data by applying a moving average filter.

<br/>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/tbnn_couette.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/class_projects/tbnn_channel.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    TBNN results for flows trained and tested on same Reynolds number. Left: Couette flow. Right: Channel flow.
</div>

<br/>

We obtained excellent results from the neural network model for both channel and Couette flow models that were trained and tested on the same Reynolds number. Training a model on one Reynolds number and testing on another led to less satisfactory results. This is due tot he extreme nonlinearities present in turbulent flows and is most likely a result of overfitting. How to resolve this dilemma is an open research question in the field.

<br/>

<p style="text-align:center;"><a href="https://kimbliu.github.io/projects/">Back to Projects</a></p>

#### References

Ling J, Kurzawski A, Templeton J. "Reynolds averaged turbulence modelling using deep neural networks with embedded invariance." <i>Journal of Fluid Mechanics</i>, 807: 155-166, 2016.

Del Alamo JC, Jimenez J. "Direct numerical simulation of the very large anisotropic scales in turbulent channel." <i>Center for Turbulence Research Annual Research Briefs</i>, 2001.

Del Alamo JC, Jimenez J. "Spectra of the very large anisotropic scales in turbulent channels." <i>Physics of Fluids</i>, 15(6): L41-L44, 2003.

Del Alamo JC, Jimenez J, Zandonade P, Moser RD. "Scaling of the energy spectra of turbulent channels." <i>Journal of Fluid Mechanics</i>, 500:135, 2004.

Fang R, Sondak D, Protopapas P, Succi S. "Neural network models for the anisotropic Reynolds stress tensor in turbulent channel flow." <i>Journal of Turbulence</i>, 21(9-10): 525-543, 2003.
