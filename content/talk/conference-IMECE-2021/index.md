+++
date = "2021-11-01"
title = "Model selection and optimal experiment design for HP MRI experiments"
abstract = "Hyperpolarized (HP) MR imaging provides enhanced insights into the tissue's metabolism and a new way to identify the tumor colony. In HP MRI, MR visible HP pyruvate is injected into the patient. It is observed that the cancerous cells promote higher production of lactate from pyruvate through Lactate dehydrogenase (LDH) compared to healthy cells; since the pyruvate is polarized, the product lactate is also polarized and visible in the MR scan. Therefore, the HP MRI experiment allows one to see HP pyruvate's distribution and the byproduct such as lactate. Higher conversion of pyruvate to lactate in the tissue may indicate the presence of an active tumor colony. Hence, the pyruvate-to-lactate conversion rate is a parameter of interest and must be inferred from the HP MR scan data. Mathematical models are required to recover the pyruvate-to-lactate conversion rate; the model needs to account for the natural decay of polarization in pyruvate and lactate, loss of polarization due to the interaction of MR signal and polarization, transient nature of vascular input of polarized pyruvate, and also the presence of endogenous pyruvate and lactate in the tissue. Additionally, the parameter's inference should also account for the signal-to-noise ratio and other uncertainties such as bolus arrival time. Unlike traditional MR, where the source does not change as many times the scan is taken, in HP MRI, there is polarization loss in every scan. This loss depends on the choice of flip angles and repetition times. There are two significant challenges associated with the HP MR experiment: 1) selecting the most plausible model among multiple models for the given data, 2) optimizing MR parameters such as repetition times and flip angles for the most accurate inference of pyruvate-to-lactate conversion rate. In this work, we apply the OPAL (the Occam Plausibility Algorithm) model selection method to find the most plausible model for the given data. For the second challenge, we consider the Bayesian-based optimal experimental design (OED); here, we formulate the mutual information for the design parameters taking the total signal as the data and ask for design parameters that maximize the mutual information. Our results show that the optimal parameters such as repetition time and flip angles are different from what is considered typically in the experiments. We also show that with optimal design parameters, the variation in pyruvate-to-lactate conversion rate is smaller. Future works include developing high-fidelity spatially varying models with explicit vessel-tissue flow coupling and the formulation of optimal experimental design using high-fidelity models."
abstract_short = ""
event = "IMECE 2021"
event_url = "https://event.asme.org/IMECE"
location = "Virtual Conference"

selected = true
math = false

#url_pdf = ""
#url_slides = ""
#url_video = ""

# Optional featured image (relative to `static/img/` folder).
#[header]
#image = ""
#caption = "My caption:"

+++

> Track: Mechanics of Solids, Structures and Fluids

> Topic 12-21: Data-Enabled Predictive Modeling, Machine Learning, and Uncertainty Quantification in Computational Mechanics
