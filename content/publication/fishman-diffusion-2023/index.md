---
title: "Diffusion Models for Constrained Domains"
date: 2023-05-11
publishDate: 2023-05-11
authors: ["Nic Fishman*", "Leo Klarner*", "Valentin De Bortoli", "Emile Mathieu", "**Michael Hutchinson**"]
publication_types: ["2"]
abstract: "Denoising diffusion models are a recent class of generative models which achieve state-of-the-art results in many domains such as unconditional image generation and text-to-speech tasks. They consist of a noising process destroying the data and a backward stage defined as the time-reversal of the noising diffusion. Building on their success, diffusion models have recently been extended to the Riemannian manifold setting. Yet, these Riemannian diffusion models require geodesics to be defined for all times. While this setting encompasses many important applications, it does not include manifolds defined via a set of inequality constraints, which are ubiquitous in many scientific domains such as robotics and protein design. In this work, we introduce two methods to bridge this gap. First, we design a noising process based on the logarithmic barrier metric induced by the inequality constraints. Second, we introduce a noising process based on the reflected Brownian motion. As existing diffusion model techniques cannot be applied in this setting, we derive new tools to define such models in our framework. We empirically demonstrate the applicability of our methods to a number of synthetic and real-world tasks, including the constrained conformational modelling of protein backbones and robotic arms."
featured: false
publication: "_TMLR 2023_, code available at request."

url_pdf: "https://openreview.net/forum?id=xuWTFQ4VGO"
# url_code: "https://github.com/MJHutchinson/SteerableCNP"
# url_poster: "files/equiv-cnp/equiv-cnp-poster.pdf"
# url_talk: "https://icml.cc/virtual/2021/poster/9935"
# url_slides: "https://docs.google.com/presentation/d/1kJymV1kVOEpiInL5TrZX8MFZi94n0f0Ei-4XRmvAKGQ/edit?usp=sharing"
# external_link: 

image:
  caption: ""
  focal_point: ""
  preview_only: false
---

