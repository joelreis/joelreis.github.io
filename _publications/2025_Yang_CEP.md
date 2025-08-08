---
title: "Output Feedback Control of an Underactuated Flying Inverted Pendulum"
collection: publications
permalink: /publication/2025_Yang_CEP
excerpt: 'We present a trajectory tracking controller for an inverted pendulum mounted on an underactuated unmanned aerial vehicle, operating under constant external disturbances.'
date: 2025-08-01
venue: cep
publisher: elsevier
type: 'journal'
number: 23
authors: [weiming, reis, yugan, silvestre]
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2025_CEP_Output_Feedback_Control_of_an_Underactuated_Flying_Inverted_Pendulum.pdf'
citation: 'W. Yang, J. Reis, G. Yu, and C. Silvestre, "Output feedback control of an underactuated flying inverted pendulum", Control Engineering Practice, vol. 164, lsevier BV, p. 106474, Nov. 2025.'
bibtex: '@article{2025_Yang_CEP,<br />
  doi = {10.1016/j.conengprac.2025.106474},<br />
  url = {https://doi.org/10.1016/j.conengprac.2025.106474},<br />
  year = {2025},<br />
  month = nov,<br />
  publisher = {Elsevier {BV}},<br />
  volume = {164},<br />
  pages = {106474},<br />
  author = {Weiming Yang and Joel Reis and Gan Yu and Carlos Silvestre},<br />
  title = {Output Feedback Control of an Underactuated Flying Inverted Pendulum},<br />
  journal = {Control Engineering Practice}<br />
}'
---
**Abstract**
---
This paper tackles the problem of trajectory tracking control for an inverted pendulum mounted on an underactuated unmanned aerial vehicle, operating under constant external disturbances.
To model the pendulum’s dynamics, a linear time-varying (LTV) system is first constructed.
Within a stochastic framework, a Kalman filter is applied to this LTV system, shown to be uniformly completely observable, to obtain: estimates of the pendulum’s angular velocity; estimates of the external disturbances; and noise-filtered measurements of the pendulum’s orientation.
A backstepping nonlinear controller is then designed, and it is analytically proven that the total error in the closed-loop system remains uniformly ultimately bounded.
The effectiveness of the proposed strategy is demonstrated through simulations, with additional experimental results further validating its performance.
