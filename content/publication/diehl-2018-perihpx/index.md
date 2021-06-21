---
title: "An asynchronous and task-based implementation of peridynamics utilizing HPX—the C++ standard library for parallelism and concurrency"
date: 2018-12-04
publishDate: 2020-12-04
authors: ["Patrick Diehl", "Prashant K Jha", "Hartmut Kaiser", "Robert Lipton", "Martin Levesque"]
publication_types: ["2"]
abstract: "On modern supercomputers, asynchronous many task systems are emerging to address the new architecture of computational nodes. Through this shift of increasing cores per node, a new programming model with focus on handling of the fine-grain parallelism with increasing amount of cores per computational node is needed. Asynchronous Many Task (AMT) run time systems represent a paradigm for addressing the fine-grain parallelism. They handle the increasing amount of threads per node and concurrency. HPX, a open source C++ standard library for parallelism and concurrency, is one AMT which is conforming to the C++ standard. Motivated by the impressive performance of asynchronous task-based parallelism through HPX to N-body problem and astrophysics simulation, in this work, we consider its application to the Peridynamics theory. Peridynamics is a non-local generalization of continuum mechanics tailored to address discontinuous displacement fields arising in fracture mechanics. Peridynamics requires considerable computing resources, owing to its non-local nature of formulation, offering a scope for improved computing performance via asynchronous task-based parallelism. Our results show that HPX-based peridynamic computation is scalable, and the scalability is in agreement with the theory. In addition to the scalability, we also show the validation results and the mesh convergence results. For the validation, we consider implicit time integration and compare the result with the classical continuum mechanics (CCM) (peridynamics under small deformation should give similar results as CCM). For the mesh convergence, we consider explicit time integration and show that the results are in agreement with theoretical claims in previous works."
featured: false
publication: "*SN Applied Sciences*"
url_source: "https://doi.org/10.1007/s42452-020-03784-x"
doi: "10.1007/s42452-020-03784-x"
---

