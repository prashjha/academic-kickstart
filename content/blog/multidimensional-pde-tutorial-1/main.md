---
title: "Python solvers for the multi-dimensional PDEs - Part 1"
author: "Prashant K. Jha"
summary: "Python solvers for 3D-1D coupled flow models"
date: 2021-01-17
bibliography: "bibliography.bib"
link-citations: true
featured: true
slug: multidimensional-pde-tutorial-1
reading_time: true
categories: ["Tutorial", "Coding", "Python", "PETSc"]
tags: ["Multidimensional PDEs", "Python", "PETSc", "3D-1D"]
header:
  caption: ''
  image: ''
#projects: [tumor-modeling]
links:
 - name: code
   url: https://github.com/prashjha
   icon_pack: fab
   icon: github
 - name: tumor modeling
   #url: {{< relref "publication/lipton-2018-free" >}}
   icon_pack: fa
   icon: fab fa-project-diagram

header-includes: |
    \usepackage[papersize={4.5in,6in},margin=0.5cm]{geometry}
    \setlength{\parskip}{2pt}
    \usepackage{fourier-orns}
    \newcommand\textbreak{%
    \begin{center}%
    \decothreeleft \aldineleft \decosix \aldineright \decothreeright%
    \end{center}}
    \pagestyle{empty}
---

# Model

hhid @key_name

{{% alert note %}}
Let $\Lambda = \cup_{i=1}^N \Lambda_i$ is the union of the centerlines of piecewise straight cylinders in the vessel network $V = \cup_{i=1}^N V_i$. Here each $V_i \subset \mathbb{R}^3$ are cylinders of radius $R_i$ and centerline $\Lambda_i$ from point $x_{i,1}\in \mathbb{R}^3$ to $x_{i,2}\in \mathbb{R}^3$. 
{{% /alert %}}  

Let $V$ is embedded in 3D tissue domain $\Omega = [0,1]^3 \subset \mathbb{R}^3$. 

{{% alert warning %}}
We consider following fields in the tissue domain

- $p = p(t,x)$, $x\in \Omega$, $t\in [0,T]$, pressure in tissue domain
- $\phi_T = \phi_T(t,x) \in [0,1]$, $x\in \Omega$, $t\in [0,T]$, total tumor species
- $\phi_\sigma = \phi_\sigma(t,x) \in [0,1]$, $x\in \Omega$, $t\in [0,T]$, nutrients in tissue

> dfhsiuefheuhrgdbfhugeruhertojeg ssifghug hsdfidhrgiu sdhdirhg
{{% /alert %}} 

and in the vascular domain

- $p_v = p_v(t,x)$, $x\in V$, $t\in [0,T]$, pressure in vessels
- $\phi_{\sigma v} = \phi_{\sigma v}(t,x) \in [0,1]$, $x\in V$, $t\in [0,T]$, nutrients transport in vessels.

## Flow in the tissue and vascular network

Pressures in the tissue and vascular network satisfy the following PDEs:

\begin{align}\label{eq:3D1Dflow}
-\nabla \cdot (K \nabla p_t) &= J_b(p_t, p_v), \qquad \text{in }\Omega, \notag \\
-\pi R_i^2\partial_s (K_v\partial_s p_v) &= -J_{bv}(p_t, p_v) , \qquad \text{in } \Lambda_i, i = 1,2, .., N,
\end{align}

where $K$ is the permeability constant of the tissue, $K_v = \frac{R_i^2}{8 \mu_{bl}}$ permeability constant, $\mu_{bl}$ dynamic viscosity of the blood, $J_{bv}$ is the source in the vessel and $J_b$ is the source in the tissue. Following \cite{koppl20203d, fritz2020analysis}, we have

\begin{align}\label{eq:flowCoup}
J_b(p_t, p_v) = L_b (\Pi(p_v) - p_t) \delta_{\Gamma}, \qquad J_{bv}(p_t, p_v) = -2\pi R L_b( p_v - \bar{p}_t),
\end{align}

where $\Gamma = \cup_{i=1}^N \Gamma_i$ is the union of surface of cylinders $V_i, i=1,..,N$, $\delta_A = \delta_A(x)$ is the delta function that is 1 if $x \in A$ and zero otherwise, $\Pi(p_v)$ is an extension of the 1D field $p_v$ by a constant value in the cross-section of the vessel, and $\bar{p}_t$ is the average tissue pressure at the circumference of the cross-section:

\begin{align}\label{eq:avgpt}
\bar{p}_t(s)\vert_{\Lambda_i} = \frac{1}{2\pi R_i} \int_{\partial D_i(s)} p_t dS, \qquad \forall s \in [0,1].
\end{align}

The velocity in the tissue domain is given by (Darcy's law):

\begin{align}\label{eq:vel}
v = -K \nabla p_t.
\end{align}

The velocity of flow in the vessel is 

\begin{align}\label{eq:velVes}
v_v = -K_v \partial_s p_v.
\end{align}


## Transport of nutrient in the vessel network

Transport of nutrients $\phi_{\sigma v}$ is modeled via the advection-diffusion equation with filtration law to account for exchange of nutrient through the walls of the vessel. We have

\begin{align}\label{eq:nut1D}
\partial_t \phi_{\sigma v} + \partial_s (v_v \partial_s \phi_{\sigma v}) = \partial_s (D_{\sigma v} \partial_s\phi_{\sigma v}) + J_{\sigma v}(\phi_l, \phi_{\sigma v}),
\end{align}

where $v_v$ is the flow speed in vessels, $D_{\sigma v}$ is the diffusion constant, $J_{\sigma v}$ the 3D1D mass exchange.

Exchange of nutrients between tissue and vessel is based on the filtration law. It consists of two terms: diffusive flux due to difference in nutrient concentration in tissue and vessel and advective flux due to difference in pressure in tissue and vessel. These fluxes are defined as follows:

\begin{align}\label{eq:nutCoup}
J_\sigma(\phi_\sigma, \phi_{\sigma v}, p_t, p_v) &= \left[ L_\sigma  (\phi_{\sigma v} - \phi_\sigma) + (1 - \sigma_v) L_b (p_v - \bar{p}_t) \hat{\phi}_\sigma \right]\delta_{\Gamma}, \notag \\
J_{\sigma v}(\phi_\sigma, \phi_{\sigma v}, p_t, p_v) &= -2\pi R_i \left[ L_\sigma( \phi_{\sigma v} - \bar{\phi}_\sigma) + (1-\sigma_v) L_b(p_v - \bar{p}_t) \right], \qquad \forall \Lambda_i \in \Lambda,
\end{align}

where $L_\sigma$ is the permeability of vessel walls for nutrient exchange, $\sigma_v$ is the reflection coefficient, $L_b$ as introduced before is the permeability coefficient for fluid exchange. $\bar{p}_t$ and  $\bar{\phi}_\sigma$ are the average tissue pressure and average nutrients at the circumference of the cross-section. Finally, $\hat{\phi}_\sigma$ is the advected nutrient due to differences in pressure between tissue and vessel, and is given by

\begin{align}
	\hat{\phi}_\sigma = \begin{cases}
		&\phi_{\sigma v}, \qquad \text{ if } p_v > \bar{p}_t,\\
		&\bar{\phi}_\sigma, \qquad \text{ otherwise}. 
	\end{cases}
\end{align}


## Nutrient in the tissue

Nutrients $\phi_\sigma$ is governed by

\begin{align}\label{eq:nut3D}
\frac{\partial \phi_\sigma}{\partial t} + \nabla \cdot(v \phi_\sigma) &= \nabla \cdot (D_\sigma \nabla \phi_\sigma)  + S_\sigma(\phi) + J_{\sigma}(\phi_\sigma, \phi_{\sigma v}, p_t, p_v),
\end{align}

where $D_\sigma$ the diffusivity constant of nutrients, $S_\sigma$ is the source terms for nutrient, $J_{\sigma}$ is the exchange of nutrient with vessels, and $v$ is the velocity in tissue. Nutrient source $S_\sigma$ includes the consumption of nutrient by tumor cells and nutrient increase due to cell death. We consider

\begin{align}\label{eq:Ssig}
S_\sigma(\phi) = -\lambda_P \phi_T \phi_\sigma + \lambda_A \phi_T.
\end{align}

where $\lambda_P$ is the rate of proliferation of tumor cells and $\lambda_A$ is the apoptosis rate. 

## Tumor evolution via Allen--Cahn type equation

We consider 2nd order PDE for $\phi_T$ based on Allen-Cahn phase-field equation

\begin{align}\label{eq:tumAC3D}
\frac{\partial \phi_T}{\partial t} + \nabla \cdot(v \phi_T) &= \epsilon_T^2 \Delta \phi_T - \Psi'(\phi_T) + S_T(\phi), 
\end{align}

where $\Psi$ is the double-well potential, $\epsilon_T$ the interfacial length scale, and $S_T$ is the source terms for tumor. We consider

\begin{align}\label{eq:doubleWell}
\Psi(\phi_T) &= E_T \phi_T^2 (1 - \phi_T)^2,
\end{align}

where $E_T>0$ is the energy scale associated to the double well potential. Rate of proliferation of tumor cells is proportional to the nutrient concentration. We consider

\begin{align}\label{eq:ST}
S_T(\phi) = \lambda_P \phi_T(1- \phi_T) \phi_\sigma - \lambda_A \phi_T,
\end{align}

where $\lambda_P$ is the rate of proliferation of tumor cells and $\lambda_A$ is the apoptosis rate. 
