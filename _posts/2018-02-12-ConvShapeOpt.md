---
layout: post
title: "Shape Optimization using Geodesic Convolutional Networks"
description: "Shape Optimization using Geodesic Convolutional Networks"
comments: true
categories: Research
keywords: "dummy content, lorem ipsum"
---

### Shape Optimization using Geodesic Convolutional Networks

We published on Arxiv a paper about a new approach to Aerodynamic shape optimization. It improves upon previously used Kriging-based surrogate models for CFD optimization. This new contribution uses the Geometric Deep Learning methods that recently appeared in computer vision. 

[Arxiv Paper](https://arxiv.org/pdf/1802.04016.pdf). 

![]({{site.url}}/img/ShapeOpt.png)

##### Showcase

![Pressure prediction on TEST set.]({{site.url}}/img/reg0.png)
![Pressure prediction on TEST set.]({{site.url}}/img/reg1.png)
![Pressure prediction on CARS-TEST set.]({{site.url}}/img/reg2.png)



<div class="row text-center">

<p>
<video width="640" controls> <source src="{{site.url}}/vids/output_cars.mp4" type="video/mp4">
</video>
</p>
<p class="text-muted">Online Pressure and Drag prediction with GCNN.</p>
</div>


<h5 class="jumbotron-heading">Optimization Results</h5>


<div class="row text-center">
<p>
<video width="640" controls> <source src="{{site.url}}/vids/opti.mp4" type="video/mp4">
</video>
</p>
<p class="text-muted">Optimization of a foil with control points.</p>
</div>

<div class="row text-center">
<p>
<video width="640" controls> <source src="{{site.url}}/vids/output_bike.mp4" type="video/mp4">
</video>
</p>
<p class="text-muted">Optimization of a bicycle shell in 3D.</p>
</div>

<div class="row text-center">
<p>
<video width="640" controls> <source src="{{site.url}}/vids/output_foils.mp4" type="video/mp4">
</video>
</p>
<p class="text-muted">Optimization of a Foil in 3D.</p>
</div>

<div class="row text-center">
<p>
<video width="640" controls> <source src="{{site.url}}/vids/output_3D.mp4" type="video/mp4">
</video>
</p>
<p class="text-muted">Finding the most aerodynamic shape around a sphere.</p>
</div>

