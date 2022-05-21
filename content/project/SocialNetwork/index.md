---
title: Experiment Under Social Network Spillover Effect
summary: A project reviews literatures about social network spillover effects and studies the situation under mis-specification of exposure mapping by simulation studies.
tags:
  - Causal Inference
date: '2022-05-11T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Image by Aronow and Samii
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/jnieser/ExperimentsUnderInterference
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---
This project studies the solutions for measuring average treatment effects for experiments under social network spillover effect.

There are two main solutions: 1. Using a social network based clustering and measures average treatment effects by eliminating spillover effects. 2. Using a different framework and solve problem by measuring main, exposure, and interaction effects separately.

This project focuses on the second framework. Some work on the first solution can be found in "AVERAGE TREATMENT EFFECTS IN THE PRESENCE
OF UNKNOWN INTERFERENCE" by FREDRIK SÄVJE et al.

In this project, we are mainly focusing on the inference tools and results from Estimating average causal effects under general interference, with application to a social network experiment by Aronow and Samii. We also make some connections with the factorial experiment paper \emph{Regression-based causal inference with factorial experiments: estimands, model specifications, and design-based properties} by Zhao and Ding. Firstly, we will briefly summarize their methodology and notations. In the second part, we retrieve the data they used and show the summary statistics of the data set. Throughout this report, we are using the field experiment in Aronow and Samii's paper as a showcase example. The paper mainly focuses on HT estimator, and we will justify the use of WLS estimator. Thirdly, we replicate the result with their methodology using weighted least square regression estimate and Horvitz-Thompson Estimator. Next, as the main part of this project, we focus on the consequences of exposure mapping being mis-specified and compare between the HT estimator and WLS estimator by simulation study. The contribution of this project is to explore the consequence of mis-specification, which is a minor gap in Aronow and Samii's original paper. Another contribution is that this project critically assess the use of HT estimator and WLS estimator. We also critically assess the interpretation of the estimates in the context of the field experiment under HT estimate and provide an alternative perspective from factorial regression.


