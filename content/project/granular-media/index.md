+++
# Project title.
title = "Study of granular media"

# Date this page was created.
date = 2020-07-18T00:00:00

# Project summary to display on homepage.
summary = "Study properties of granular media using computational methods"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["granular media", "DEM", "computational mechanics", "PeriDEM"]

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
  caption = "Damage plot at different times in a compressive test. Red indicates discretized nodes with damage."
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Smart"
+++

# Activities

## 1. Development of a high-fidelity model for granular media

Taking the earlier research on peridynamics for granular media forward, we have developed the Peridynamics-DEM high-fidelity model that can handle arbitrarily shaped particles and particle breakage. Traditional models based on DEM (Discrete Element Method) can not handle the particles with arbitrary shapes and deformation of individual particles. Extension of DEM based method to overcome these challenges is possible. However, it is not trivial. PeriDEM model proposed in [preprint: arXiv:2010.07218](https://arxiv.org/abs/2010.07218) uses peridynamics for deformation of individual particles. In the model, the contact forces between two particles act at the level of discretization. Because contact forces are applied to discretized nodes (within a small distance) of two particles, particles can see the local boundary; thus, the model can accurately simulate the locking effects.

| ![](files/two_p_wall_fracture_m1_all.png) | 
|:--:| 
| *Figure 1: Two-particle test. The top particle is given initial velocity. The plot shows the damage upon contact for different initial velocities—both particles made of the same materials. Damage above 1 indicates the onset of failure. From [preprint: arXiv:2010.07218](https://arxiv.org/abs/2010.07218)* |

| ![](files/two_p_wall_fracture_m12_all.png) | 
|:--:| 
| *Figure 2: Same as Figure 1, but now the particle on top is stronger than the bottom particle. We see that only the bottom particle has damage above 1.* |

| ![](files/compressive_test_t1_reaction_force.png) | 
|:--:| 
| *Figure 3: Compressive test using 25 particles of varying radius. The container's top wall is moving downwards. Left: Plot of reaction force on the container's top wall as a function of penetration downwards. Right: Damage on individual particles at different times. Damage on discretized nodes of particles is shown. Red indicates a node has damage one or above. From [preprint: arXiv:2010.07218](https://arxiv.org/abs/2010.07218)* |


| ![](files/m1_t5.gif) | ![](files/m1_t6.gif) |
| :---: |:---: |
| Two particles with same properties. $v_0 = 4$ m/s | Two particles with same properties. $v_0 = 5$ m/s |


| ![](files/m12_t5.gif) | ![](files/m12_t6.gif) |
| :---: |:---: |
| Top particle stronger than bottom. $v_0 = 4$ m/s | Top particle stronger than bottom. $v_0 = 5$ m/s |

| ![](files/t1.gif) | 
|:--:| 
| *Compressive test simulation* |
