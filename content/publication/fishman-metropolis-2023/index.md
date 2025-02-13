---
title: "Metropolis Sampling for Constrained Diffusion Models"
date: 2023-05-20
publishDate: 2023-05-20
authors: ["Nic Fishman*", "Leo Klarner*", "Emile Mathieu", "**Michael Hutchinson**", "Valentin De Bortoli"]
publication_types: ["2"]
abstract: "Denoising diffusion models have recently emerged as the predominant paradigm for generative modelling. Their extension to Riemannian manifolds has facilitated their application to an array of problems from the natural sciences. However, in many practical settings, such manifolds are defined by a set of constraints and are not covered by the existing (Riemannian) diffusion model methodology. Recent works have attempted to address this issue by employing novel noising processes based on logarithmic barrier methods or reflected Brownian motions. However, the associated samplers are computationally burdensome as the complexity of the constraints increases. In this paper, we introduce an alternative simple noising scheme based on rejection sampling that affords substantial gains in computational efficiency and empirical performance compared to the earlier samplers. Of independent interest, we prove that this new process corresponds to a valid discretisation of the reflected Brownian motion. We demonstrate the scalability and flexibility of our approach on a range of problem settings with convex and non-convex constraints, including applications from geospatial modelling, robotics and protein design."
featured: false
publication: "_Under review at Neurips 2023_, code available at request until publication."

url_pdf: "https://arxiv.org/abs/2307.05439"
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

