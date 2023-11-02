---
title: "Kalman-based velocity-free trajectory tracking control of an underactuated aerial vehicle with unknown system dynamics"
collection: publications
permalink: /publication/2023-06-paper-title-number-15
excerpt: 'In this paper we solve the problem of trajectory tracking control of an underactuated autonomous aerial vehicle in the presence of unknown time-varying dynamics.'
date: 2023-06-01
venue: automatica
publisher: elsevier
type: 'journal'
number: 15
authors: [reis, yugan, silvestre]
publisherurl: 'https://www.sciencedirect.com/science/article/pii/S0005109823003084'
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2023_Automatica_Kalman_based_velocity_free_trajectory_tracking_control_of_an_underactuated_aerial_vehicle_with_unknown_system_dynamics.pdf'
citation: 'J. Reis, G. Yu, and C. Silvestre, “Kalman-based velocity-free trajectory tracking control of an underactuated aerial vehicle with unknown system dynamics,” Automatica, vol. 155. Elsevier BV, p. 111148, Sep. 2023.'
bibtex: '@article{2023_Reis_Automatica,<br />
  doi = {10.1016/j.automatica.2023.111148},<br />
  url = {https://doi.org/10.1016/j.automatica.2023.111148},<br />
  year = {2023},<br />
  month = sep,<br />
  publisher = {Elsevier {BV}},<br />
  volume = {155},<br />
  pages = {111148},<br />
  author = {Joel Reis and Gan Yu and Carlos Silvestre},<br />
  title = {Kalman-based velocity-free trajectory tracking control of an underactuated aerial vehicle with unknown system dynamics},<br />
  journal = {Automatica}<br />
}'
---
**Abstract**
---
In this paper we solve the problem of trajectory tracking control of an underactuated autonomous aerial vehicle in the presence of unknown time-varying dynamics.
We begin our approach with the design of a Kalman filter for the linear motion subsystem under non-vanishing perturbations.
The filter attenuates the noise of position measurements, and simultaneously estimates the linear velocity of the vehicle as well as an unknown term of lumped dynamics, which includes model parametric uncertainty and exogenous perturbations.
The output and residual of the filter are then fed to a nonlinear controller whose thrust actuation is bounded with respect to the position and velocity errors.
The total error stemming from the closed-loop system is shown to be uniformly ultimately bounded.
Experimental results and comparison data are presented to showcase the performance of our strategy in different real-world applications using a quadrotor vehicle.
