---
title: "Differential Privacy, Approximate Bayesian Inference and Distributed Learning"
summary: "Learning Private, Bayesian Machine Learning Models in the Federating Learning Context"
authors: [Michael Hutchinson]
tags: []
categories: []
share: false
date: 2019-09-28
math: true
---
Modern machine learning techniques are quickly being applied to a vast range of problems in the real world. However, most modern techniques are not well suited to handle a number of difficult situations. A recent piece of work we did aims to combine approaches for tackling three of these.

### Situations where we would like uncertainty estimates in our predictions
For tasks such as classifying each photo in you photo library into a number of categories, or tagging them each as a particular person, the downsides to getting the decision wrong are minimal, if annoying for the end user. There are many other settings where the downsides to making the incorrect choice could mean life or death, such as medical applications, or driverless cars.

In these situations, we would like to know exactly how confident our model is in its predictions or decisions, so that downstream systems can account for this when taking action. For example when a driverless car is planning how to turn right, we'd very much like to know if it's 99% sure that nothing is in its way, or if its a 50/50 toss up between that and a small child. 

This kind of problem can be solved with a more principled application of statistics to Machine Learning. When applied to deep learning this is often refereed to as _[Bayesian Deep Learning](http://bayesiandeeplearning.org/)_. 

There exists a large body of literature in this area. In this project we focused on Variational Inference (VI) techniques.[^1]  

### Situations where the data we wish to learn from isn't in one place
It is easy to imagine that for a number of reasons, the data we want our model to learn from cannot be bought to a single locations. Examples may include legal reasons (e.g. the recent [GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation) in Europe), or practical reasons (such as mobile phone/edge device data, or data that is too large to be efficiently transported).

In these situations, we would still like to be able to learn from this data, but many techniques cannot naively handle this. This area of work again has a large body of work, and is know as _Distributed or Federated Learning_.

### Situations where the data we are handling is privacy-sensitive
Much of the data that we would like to use to train Machine Learning models is sensitive to someone in some way. This could be medical data, browsing history, or financial data. Data sources (i.e. the individuals from whom this data is collected) are rightly skeptical about handing over their information to third parities.

Recent work showed that deep learning models have a tendency to memorise their input data, and using targeted attacks some input data can be recovered from them.[^2] In this case, the threat to a users sensitive data comes not just from people to whom they hand their data, but from anyone who has access to the models trained on their data.

_Differential Privacy_[^3] is the current gold standard in protecting the privacy of data while extracting information from it. By carefully processing updates, and in particular by adding noise, we can achieve a series of guarantees regarding information leakage, user utility loss, and more. 

### Differnetial Private Federated Variational Inference

Our recent work builds on the Partition Variational Inference[^4] framework, a Variational Inference framework that allows for easy distributed and continual learning, and extends this to include privacy preserving updates based on recent differential privacy literature. There will be an arxiv preprint available soon. In the meantime, check out the [code](github.com/MrinankSharma/DP-PVI), and feel free to get in touch with any questions!

UPDATE: This paper has been accepted to the [Privacy in Machine Learning workshop](https://priml-workshop.github.io/priml2019/) at Neurips 2019!

[^1]: Blei, David M., Alp Kucukelbir, and Jon D. McAuliffe. "Variational inference: A review for statisticians." Journal of the American statistical Association 112.518 (2017): 859-877. [arxiv](https://arxiv.org/abs/1601.00670)

[^2]: Carlini, Nicholas, et al. "The secret sharer: Measuring unintended neural network memorization & extracting secrets." arXiv preprint arXiv:1802.08232 (2018). [arxiv](https://arxiv.org/abs/1802.08232)

[^3]: Dwork, Cynthia, and Aaron Roth. "The algorithmic foundations of differential privacy." Foundations and Trends® in Theoretical Computer Science 9.3–4 (2014): 211-407. [website](https://www.cis.upenn.edu/~aaroth/privacybook.html)

[^4]: Bui, Thang D., et al. "Partitioned Variational Inference: A unified framework encompassing federated and continual learning." arXiv preprint arXiv:1811.11206 (2018). [arxiv](https://arxiv.org/abs/1811.11206)