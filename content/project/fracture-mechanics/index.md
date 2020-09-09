+++
# Project title.
title = "Analysis and application of peridynamics"

# Date this page was created.
date = 2020-07-18T00:00:00

# Project summary to display on homepage.
summary = "Analysis and application of peridynamics"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["peridynamics", "nonlocal", "fracture mechanics", "computational"]

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
  caption = "Crack speed profile and plot of damage for Mode-I crack propagation (Int J Fra (2020) Jha and Lipton)"
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Smart"
+++


# Activity

## Kinetic relations and local energy balance for LEFM from a nonlocal peridynamic model

In this work, we carefully looked at the peridynamic energy associated to process zone and recover the kinetic relation for crack tip velocity for simple mode-I crack problem. It is based on more theoretical work, see [arXiv preprint](https://arxiv.org/abs/2001.00313). This is a joint work with Dr. Lipton.

Article recently published in International Journal of Fracture, see more [details](https://link.springer.com/article/10.1007/s10704-020-00480-0).

## A priori error analysis and well-posedness of nonlinear peridynamic models

At Louisiana State University, I had spent good amount of time working on a-priori error estimates for finite-difference and finite-element discretization of and well-posedness of nonlinear peridynamic models. This was under the guidance of my adviser Dr. Lipton. On this topic we have published several journal articles and few book chapters, see [publication page]( {{< relref "publication" >}}). 

## Model development

In this [paper]( {{< relref "publication/lipton-2018-free" >}}), we proposed a bond-based peridynamic model with memory effect. Material subjected to cyclic loading with each cycle deforming the material beyond some critical strain would lose stiffness. The proposed model incorporates this effect at the level pairwise interaction. Numerical results demonstrate this effect. 
