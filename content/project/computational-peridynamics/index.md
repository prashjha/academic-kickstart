+++
# Project title.
title = "Computational methods for nonlocal models"

# Date this page was created.
date = 2020-09-08T00:00:00

# Project summary to display on homepage.
summary = "Develop efficient and parallel computational methods for class of nonlocal models such as Peridynamics and nonlocal diffusion equations"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["peridyamics", "nonlocal", "computational mechanics", "programming"]

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
  caption = "NLMech library welcome page. https://github.com/nonlocalmodels/NLMech"
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Smart"
+++

Develop efficient and parallel computational methods for class of nonlocal models such as Peridynamics and nonlocal diffusion equations

# Activities

## 1. Google Summer of Code 2020
Towards the development of a massively parallel computational library for peridynamics and other nonlocal models, together with P. Diehl, we prepared a computational problem where the goal was to develop a massively parallel library for the simple 2D nonlocal heat equation. See the rough description of the [problem](https://github.com/nonlocalmodels/nonlocalheatequation/blob/master/description/problem_description.pdf). This project was sponsored by Google in Google Summer of Code 2020 and was assigned to student P. Gadikar (IIT Madras). Pranav's work is open source and can be found [here](https://github.com/nonlocalmodels/nonlocalheatequation). Conference paper on proposed load balancing algorithm is in this link [GSoC 2020 conference paper]( {{< relref "publication/gadikar-2021-nonlocal" >}}).

## 2. NLMech library
We have launched peridynamics code [NLMech](https://github.com/nonlocalmodels/NLMech) that utilizes [HPX](https://github.com/STEllAR-GROUP/hpx) library for efficient multi-threading computation. We aim to make the NLMech library more user-friendly and easily extensible in the coming days. Our future goals are to 

- develop a fully parallel library following some of the key ideas and algorithms from our GSoC 2020 work

- implement Quasistatic discretization

The paper with P. Diehl briefly describing the open-source library is currently under review in JOSS (Journal of Open Source Software). The review of the code and paper is open and can be seen live [here](https://github.com/openjournals/joss-reviews/issues/2898).
