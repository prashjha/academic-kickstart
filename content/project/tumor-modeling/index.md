+++
# Project title.
title = "Modeling tumor growth, angiogenesis, drug-therapy, metastasis"

# Date this page was created.
date = 2020-07-18T00:00:00

# Project summary to display on homepage.
summary = "Development and analysis of models of tumor growth, angiogenesis, drug therapy, and metastasis"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["tumor model", "angiogenesis", "modeling", "computational oncology"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references 
#   `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides = "example-slides"

# Links (optional).
url_pdf = ""
url_slides = ""
url_video = ""
url_code = ""


# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
[image]
  # Caption (optional)
  caption = "Top: Progression of tumor towards artery. Bottom: Angiogenesis and tumor growth"
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Smart"
+++

# Activity

## Analysis of a new multispecies tumor growth model coupling 3D phase-fields with a 1D vascular network

This is a joint work with Dr. J. T. Oden at UT Austin and colleagues at Technical University of Munich. In this work, we study the 3D-1D model of tumor growth that couples the flow and transport of nutrient in the vessel network with the transport of nutrient and tumor evolution in the tissue domain. In particular, we looked at the problem of well-posedness of resulting highly coupled multi-dimension nonlinear model. See the [preprint]( {{< relref "publication/fritz-2020-analysis" >}}).

## Modeling and simulation of vascular tumors embedded in dynamically evolving capillary networks

This work takes the work in paper above to one step further. In this work, we add the angiogenesis effect to the model. Angiogenesis is a phenomena through which nutrient starved tumor cells release special molecules collectively called TAF (Tumor Angiogenesis Factor) which co-opt the blood vessels in the vicinity to grow towards the tumor colony and supply nutrient. This work is under preparation and soon preprint will be available.

## 3D1D model of drug therapy and metastasis

In this work, we propse a 3D-1D model for drug therapy and metastasis. This work is in early stage.
