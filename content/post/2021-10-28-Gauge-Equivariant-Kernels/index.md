---
title: "Vector valued Gaussian Processes on Riemannian Manifolds via Gauge Equivariant Projected Kernels"
# <!-- summary: "A collection of things related to me for, and things from, the 2020 Virtual MLSS" -->
authors: ["**Michael Hutchinson***", "Alexander Terenin*", "Viacheslav Borovitskiy*", "So Takao", "Yee Whye Teh", "Marc Peter Deisenroth"]
tags: []
categories: []
share: false
date: 2021-10-28
math: true
aliases:
    - /gauge-equivariant-kernels

url_pdf: "https://arxiv.org/pdf/2110.14423.pdf"
url_code: "https://github.com/MJHutchinson/ExtrinsicGaugeEquivariantVectorGPs"
url_talk: "https://www.youtube.com/watch?v=mbDabDd8Dxg"
url_slides: "https://docs.google.com/presentation/d/1gZ8li3dJymo-sRVnFCxxJDRxKQoH5GumzflN8Cg82DE/edit?usp=sharing"
# external_link: 

image:
  caption: "Example inference of a wind field from satellite observations."
  focal_point: ""
  preview_only: false

draft: true
---
# Abstract

Gaussian processes are machine learning models capable of learning unknown functions in a way that represents uncertainty, thereby facilitating construction of optimal decision-making systems.  Motivated by a desire to deploy Gaussian processes in novel areas of science, a rapidly-growing line of research has focused on constructively extending these models to handle non-Euclidean domains, including Riemannian manifolds, such as spheres and tori. We propose techniques that generalize this class to model vector fields on Riemannian manifolds, which are important in a number of application areas in the physical sciences.  To do so, we present a general recipe for constructing gauge equivariant kernels, which induce Gaussian vector fields, i.e. vector-valued Gaussian processes coherent with geometry, from scalar-valued Riemannian kernels. We extend standard Gaussian process training methods, such as variational inference, to this setting. This enables vector-valued Gaussian processes on Riemannian manifolds to be trained using standard methods and makes them accessible to machine learning practitioners.

# Vector-field Gaussian processes on Riemannian manifolds

Gaussian Processes are useful tools for non-parametrically modelling distributions over function, $f: X \to Y$, for example $f: \mathbb{R} \to \mathbb{R}$, the space of 1-D functions, or $f: \mathbb{R}^2 \to \mathbb{R}^2$, a vector field over the 2-D plane. These function spaces can be modelled with well known kernels such as squared exponential and Matérn class of kernels.

It is not necessary however for $X$ or $Y$ to be some Euclidean space. Previous works has focused on constructing kernels for working with Riemannian manfolds. Two particular cases have been investigated, the case of scalar functions on a manifold ($f:M \to \mathbb{R}$), and functions from the real line onto a manifold ($\mathbb{R} \to M$). 

In this paper we are interested in constructing Guassian processes over _tangential vector fields_ over manifolds. These are functions $M \to TM$, maps from the manifold into the _tangent space_ of the manifold.

The tangent space of a single point on a manifold is in intuitively all the directions one can move on the manifold from that point. The tangent space of a _single point_ will always be isomorphic to $\mathbb{R}^d$ for a $d$ dimensional manifold.
![Diagram of the tangent space of a point on the sphere >](/files/gauge-kernels/tangent_space.png)

<!-- <div class="figure", style="float: right;"> -->
<!-- <img src="/files/gauge-kernels/tangent_space.png" style="float: right;" alt="" /> -->
<!-- <p class="caption">A screenshot of the updated Hugo Tanka theme.</p>
</div> -->

Crucially though, there is no canonical basis on these tangent spaces. Taking the union of the tangent spaces of all the points on a manifold gives the manifold's tangent space.