---
title: "Geometric Neural Diffusion Processes"
date: 2023-06-01
publishDate: 2023-06-01
authors: ["Emile Mathieu*", "Vincent Dutordoir*", "**Michael John Hutchinson***", "Valentin De Bortoli", "Yee Whye Teh", "Richard E Turner"]
publication_types: ["2"]
abstract: "Denoising diffusion models have proven to be a flexible and effective paradigm for generative modelling. Their recent extension to infinite dimensional Euclidean spaces has allowed for the modelling of stochastic processes. However, many problems in the natural sciences incorporate symmetries and involve data living in non-Euclidean spaces. In this work, we extend the framework of diffusion models to incorporate a series of geometric priors in infinite-dimension modelling. We do so by a) constructing a noising process which admits, as limiting distribution, a geometric Gaussian process that transforms under the symmetry group of interest, and b) approximating the score with a neural network that is equivariant w.r.t. this group. We show that with these conditions, the generative functional model admits the same symmetry. We demonstrate scalability and capacity of the model, using a novel Langevin-based conditional sampler, to fit complex scalar and vector fields, with Euclidean and spherical codomain, on synthetic and real-world weather data."
featured: false
publication: "_Under review at Neurips 2023_"

url_pdf: "https://arxiv.org/abs/2307.05431"
url_code: "https://github.com/cambridge-mlg/neural_diffusion_processes"
# url_poster: "files/equiv-cnp/equiv-cnp-poster.pdf"
# url_talk: "https://icml.cc/virtual/2021/poster/9935"
# url_slides: "https://docs.google.com/presentation/d/1kJymV1kVOEpiInL5TrZX8MFZi94n0f0Ei-4XRmvAKGQ/edit?usp=sharing"
# external_link: 

image:
  caption: ""
  focal_point: ""
  preview_only: false
---

