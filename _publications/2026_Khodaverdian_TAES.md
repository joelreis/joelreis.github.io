---
title: "Koopman-Based Discrete-Time Controller Design for Nonlinear Flexible Spacecraft Dynamics"
collection: publications
permalink: /publication/2026_Khodaverdian_TAES
excerpt: 'To address the challenges of controlling flexible spacecraft with nonlinear dynamics, this paper proposes a Koopman-based approach that represents these dynamics in a space of an infinite-dimensional observable that facilitates analysis and control design.'
year: 2026
venue: taes
publisher: ieee
type: 'journal'
number: 27
authors: [khodaverdian,reis,silvestre]
publisherurl: 'https://doi.org/10.1109/TAES.2026.3671765'
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2026_TAES_Koopman_Based_Discrete_Time_Controller_Design_for_Nonlinear_Flexible_Spacecraft_Dynamics.pdf'
citation: 'M. Khodaverdian, J. Reis, and C. Silvestre, ‘Koopman-based discrete-time controller design for nonlinear flexible spacecraft dynamics’, IEEE Trans. Aerosp. Electron. Syst., pp. 1–16, 2026.'
bibtex: '@article{2026_Khodaverdian_TAES,<br />
  doi = {10.1109/TAES.2026.3671765},<br />
  url = {https://doi.org/10.1109/taes.2018.2831118},<br />
  year = {2026},<br />
  month = ,<br />
  publisher = {Institute of Electrical and Electronics Engineers ({IEEE})},<br />
  volume = {},<br />
  number = {},<br />
  pages = {1-16},<br />
  author = {Maria Khodaverdian, Joel Reis, and Carlos Silvestre},<br />
  title = {Koopman-Based Discrete-Time Controller Design for Nonlinear Flexible Spacecraft Dynamics},<br />
  journal = {{IEEE} Transactions on Aerospace and Electronic Systems}<br />
}'
---
**Abstract**
---
To address the challenges of controlling flexible spacecraft with nonlinear dynamics, we propose a Koopman-based approach that represents these dynamics in a space of an infinite-dimensional observable that facilitates analysis and control design.
Unlike conventional data-driven techniques, which often struggle to identify suitable observables, our method systematically derives tailored observables specifically designed for flexible spacecraft dynamics.
We prove that the proposed sequence of observables tends to zero pointwise, enabling a finite subset to accurately approximate the lifted space. 
Numerical simulations validate the agreement between the lifted dynamics and the original nonlinear spacecraft model.
By leveraging this Koopman-based approximation, we enable the design of Model Predictive Control (MPC) and linear quadratic regulator controllers for nonlinear dynamics, effectively simplifying discrete control synthesis.
We benchmark our method against both nonlinear MPC and linear MPC applied directly to the nonlinear system, demonstrating the effectiveness of our proposed framework.
