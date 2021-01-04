+++
# Project title.
title = "Signal recovery from MRI"

# Date this page was created.
date = 2020-07-18T00:00:00

# Project summary to display on homepage.
summary = "Development of models for improved signal recovery and image reconstruction, and developement and application of new methods for optimal data acquisition with uncertain model parameters"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["computational oncology", "model inference", "MRI data", "HP MRI"]

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
  #caption = "Tumor growth towards nutrient supplying vessel and angiogenesis"
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Smart"
+++


# Activities

## 1. A mechanistic tumor growth model for HP MRI

This project aims to propose a PDE-based model for recovery of a parameter such as *pyruvate to lactate transfer rate* from the Hyperpolarized (HP) MR imaging data. HP MRI is a state of art imaging technique and provides a means to identify the tumor regions. Pyruvate to lactate conversion naturally occurs in tissue; however, this conversion is typically more substantial in the presence of cancerous cells. HP MRI provides the intensity of pyruvate and lactate produced from polarized pyruvate. The region with high lactate indicates the presence of cancerous cells. Postprocessing of HP MRI data involves the calculation of *pyruvate to lactate transfer rate*. Current models are based on spatially invariant compartmental models. Our objective is to propose a PDE-based model coupled with the vascular flow to describe pyruvate and lactate evolution. The vasculature will be based on real data. We believe that such a high-fidelity model will result in a more accurate recovery of parameters. 

Recently, Oden Institute, MD Anderson Cancer Center, and TACC signed an MOU to advance cancer research. Our HP MRI project was selected as one of the five pilot projects under the joint initiative and will be effective from 09/01/2020 - 08/31/2021.




