---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 5

title: Experience
subtitle:

# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
experience:
  - title: Research Intern, Machine Learning
    company: Guotai Junan Securities
    company_url: 'https://www.gtja.com/'
    company_logo: gtja
    location: Shanghai, China
    date_start: '2019-12-01'
    date_end: '2020-09-01'
    description: |2-
        Responsibilities include:
    
        * Applied Machine Learning on stock dataset to extract signals and designed algorithms to profit by trading on signals.
        * Cleaned 151 Mb raw csv data, design features and coded a systematic algorithm to obtain signals to maximize correlation with price change, such correlation coefficient reached around 50% with XGBoost model.
        * Achieved 10% 4-month return in tested sample in ETF through developing an algorithm to process the signal collected.
        * Improved the speed for searching optimal parameters by over 50% through rewriting algorithms in Numba package.
        * Optimized the cost function of a genetic algorithm method to include rank correlation and information ratio and yield 100% profit return in training set after applying the modified genetic algorithm.

  - title: Computer Vision Research Intern
    company: Tencent
    company_url: 'https://www.tencent.com/en-us/'
    company_logo: tencent
    location: Shanghai, China
    date_start: '2019-06-01'
    date_end: '2019-09-01'
    description: |2-
        Responsibilities include:
    
        * Researched on the architecture of Neural Network and applied to detect facial log-in attacks like using a picture to log in.
        * Improved the original classification framework by reapplying ResNet through pyTorch and trained on GPU through Cuda.

design:
  columns: '2'
---
