---
title: Why does the degrees of freedom in Linear Regression equal n-p?
summary: Linear Regression
tags:
date: '2022-05-11T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: R
  focal_point: Smart

links:

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

If we run linear regression in R, then we will see a term in the report "degrees of freedom" and that value equals n-p where n is the number of observations (data points) and p is the number of parameters (including intercept).

But what does it mean? How is it useful? 

1. Answer: Measure $\sigma^2$

Under the Gauss-Markov model, which states $y_i = x_i^{T}\beta+\epsilon_i$ where $\epsilon$ are iid errors centered at zero with variance $\sigma$. Here, $x_i$ and $\beta$ are all assumed determined. $\epsilon_i$ are the randomness here, which cause y to be random.

With the widely known $(X^TX)^{-1}X^TY$ formula, one can derive the BLUE estimator $\hat{\beta}$ for $\beta$ and obtain estimated residual $\hat{\epsilon}$. Then, how can we estimate $\sigma$? We have RSS, which is the residual sum of squares but what's next?

A short answer is: $E(\frac{RSS}{n-p}) = \sigma^2$. Here, the denominator is the degree of freedom. Proof follows from the fact that $cov(\hat{\epsilon})=\sigma^2 (I_n-H)$ , where H is the projection matrix and error term centers at zero.

To make the proof easier, let us further assume error terms follow normality. Then, $RSS=\sum_{i=1}^{N}\hat{\epsilon^2}$ is similar to a chi-square distribution. Note, chi-square distribution with l degree of freedom means sum of l standard normal's square.

But they are not identically the same. Actually, $\frac{RSS}{\sigma^2} \sim \chi_{n-p}$ because the trace of (1-H) is n-p. $E(\chi_{n-p})=n-p$ so $E(\frac{RSS}{n-p}) = \sigma^2$

2. Answer: Hypothesis Testing for $\hat{\beta}$

$\frac{\hat{\beta} - \beta}{\sqrt{\hat{\sigma^2}}(X^TX)^{-1}} \sim t_{n-p}

n-p is also the degree of freedom of t distribution for testing whether $\beta$ is zero. Note, t distribution $t_{n-p}=\frac{N(0,1)}{\sqrt{\chi^2_{n-p}/(n-p)}}$. The n-p comes from the same chi-square distribution as we mentioned above.

But here, the assumption is that error term follows homoscedasticity. How do we estimate the standard error for $\hat{\beta}$ under heteroscedasticity? It will be in the future posts about EHW and WLS.
