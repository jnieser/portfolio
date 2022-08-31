---
title: Video Game Detection by Audio Fingerprints
summary: An innovative and comprehensive model structure that detects change-of-point and classify sessions of fingerprints to a game label with Transformer, Approximate Nearest Neighbor, and XGBoost.
tags:
  - Machine Learning
date: '2022-08-31T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Detection Demo
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
# slides: example
---
As the revenue for selling hardware continuous to decline for smart TV companies, companies like Vizio are relying on analyzing users' engagement behaviors and advertisement revenue more than ever. One topic about analyzing users' engagement behaviors is to know what video games users are playing through the TV and how long the users are playing those games.

It appears that image recognition is not suitable for detecting video games because image contents in video games are too noisy. Therefore, in this report, I will present the state-of-the-art ways to detect video games with audio fingerprints collected from the users' end.

The contribution in this paper is that it gives a comprehensive model that detects the change-of-point, establishes sessions, and labels each session to a certain game.

The sections are arranged as follows: Section 2 gives an overview of the models used in this paper and the raw data, Section 3 explains how to detect games by similarity matches and how to smooth the decision boundaries, Section 4 briefly covers how to detect a game console sound, Section 5 covers how to detect whether a session of audio fingerprints belong to a game or tv contents, and Section 6 covers how to detect a change-of-point given that the previous three models do not capture such signal. Section 7 gives a summary of the comprehensive model that is based on the previous models, and show some examples.