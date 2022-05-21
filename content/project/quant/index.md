---
title: High Frequency Quant Trading Algorithm
summary: A full-stack project composed of data cleaning, signal prediction, and trading strategy back test for high frequency trading.
tags:
  - Machine Learning
date: '2021-06-11T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption:
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/jnieser/IntradayQuantitativeTradingAlgorithm
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
This project studies on using machine learning to predict high frequency stock movement, and profit from the prediction.

The function to be approximated by XGBoost model is a function that takes order book data and projects the VWAP change in the future 30 seconds.

After a successful approximation of the etf price movement, this project focuses on the challenge of beating the market by high frequency trading.

The back test shows a steady 5% return on a scale of 60 million fund from period 2021-02-01 to 2021-04-01.

Data is from an ETF in Shanghai Stock Exchange.
