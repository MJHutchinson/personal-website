---
title: "Federeated Functional Variational Inference"
date: 2021-11-27
publishDate: 2021-1-27T00:00:00
authors: ["**Michael Hutchinson**", "Matthias Reisser", "Christos Louizos"]
publication_types: ["2"]
abstract: "Traditional federated learning involves optimizing point estimates for the parameters of the server model, via a maximum likelihood objective. Models trained with
such objectives show competitive predictive accuracy, however they are poorly calibrated and provide no reliable uncertainty estimates. These, however, are particularly important in safety critical applications of federated learning, such as self-driving cars and healthcare. In this work, we propose FSVI, a method to train Bayesian neural networks in the federated setting. Bayesian neural networks provide a distribution over the model parameters, which allows to obtain uncertainty estimates. Instead of employing prior distributions and doing inference over the model parameters, FSVI builds upon recent advances in functional variational inference and posits prior distributions directly in the function space of the network. We discuss two different approaches to federated FSVI, based on FedAvg and model distillation respectively, and show its benefits compared to traditional weight-space inference methods."
featured: true
publication: "*Workshop on Bayesian Deep Learning, Neurips 2021*"

url_pdf: "http://bayesiandeeplearning.org/2021/papers/71.pdf"
# url_code: "https://github.com/MJHutchinson/ExtrinsicGaugeIndependantVectorGPs"
# url_poster: "files/gauge-kernels/poster.pdf"
# url_talk: "https://www.youtube.com/watch?v=mbDabDd8Dxg"
# url_slides: "https://docs.google.com/presentation/d/1gZ8li3dJymo-sRVnFCxxJDRxKQoH5GumzflN8Cg82DE/edit?usp=sharing"
# external_link: 

image:
  caption: ""
  focal_point: ""
  preview_only: false
---

