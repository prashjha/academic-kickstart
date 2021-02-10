+++
# Project title.
title = "nonlocalheatequation"

# Date this page was created.
date = 2021-02-09T00:00:02

# Project summary to display on homepage.
summary = "Implementation of a distributed nonlocal heat equation solver with load balancing"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["nonlocal", "heat equation", "distributed computing", "GSoC"]

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
  caption = ""
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Smart"
+++

# Code information

Github link: [nonlocalheatequation](https://github.com/nonlocalmodels/nonlocalheatequation)

Documentation: [nonlocalheatequation documentation](https://nonlocalmodels.github.io/nonlocalheatequation/documentation/)

Contributors: 

- Pranav Gadikar (Indian Institute of Technology Madras)

- Patrick Diehl (Louisiana State University)

- Prashant K. Jha

# Notes

This is a **Google Summer of Code 2020** project. In this work, we carefully looked the challenges in development of distributed solvers for nonlocal interaction based models such as nonlocal diffusion equation and peridynamics. We propose methods to efficiently handle the increased data dependency (due to large-scale interaction) and balancing the load to minimize cpu idle time. For more details, see [arXiv preprint]({{< relref "publication/gadikar-2021-nonlocal" >}}). Lead developer of the project is Pranav Gadikar.
