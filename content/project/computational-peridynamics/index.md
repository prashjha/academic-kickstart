+++
# Project title.
title = "Computational methods for nonlocal models"

# Date this page was created.
date = 2020-09-08T00:00:00

# Project summary to display on homepage.
summary = "Develop efficient and parallel computational methods for class of nonlocal models such as Peridynamics and nonlocal diffusion equations"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["peridyamics", "nonlocal", "computational"]

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
  caption = "Nonlocal heat equation parallel solver scaling (Credit P. Gadikar GSoC project)"
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Smart"
+++

Develop efficient and parallel computational methods for class of nonlocal models such as Peridynamics and nonlocal diffusion equations

# Activity

## Google Summer of Code 2020
Towards development of massively parallel computational library for peridynamics and other class of nonlocal models, together with P. Diehl, we prepared a computational problem where the goal was to develop a massively parallel library for simple 2D nonlocal heat equation. See the rough description of the problem [here](description.pdf). This project was selected as one of the many projects sponsered by Google in Google Summer of Code and was assigned to student P. Gayu (IIT Madras). Pranav's work is open source and can be found [here](https://github.com/nonlocalmodels/nonlocalheatequation). 

## NLMech library
With P. Diehl, we have launched our peridynamics code [NLMech](https://github.com/nonlocalmodels/NLMech) that utilizes [HPX](https://github.com/STEllAR-GROUP/hpx) library for efficient multi-threading computation. We aim to make NLMech library more user friendly and easily extensible in coming days. Our future goals are to 

- develop fully parallel library following some of the key ideas and algorithms froom work on [Google Summer of Code 2020](https://summerofcode.withgoogle.com/projects/#6693763189047296)

- implement Quasistatic discretization 
