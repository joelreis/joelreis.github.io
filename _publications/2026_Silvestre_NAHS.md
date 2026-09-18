---
title: "Event-Triggered Neural Network Adaptive Hybrid Attitude Control"
collection: publications
permalink: /publication/2026_Silvestre_NAHS
excerpt: 'We develop an adaptive controller for rigid-body attitude tracking systems that combines a neural network architecture with an event-triggered mechanism.'
year: 2026
venue: nahs
publisher: elsevier
type: 'journal'
number: 31
authors: [joaosilvestre,reis,casau,oliveira]
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2026_NAHS_Event_Triggered_Neural_Network_Adaptive_Hybrid_Attitude_Control.pdf'
publisherurl: 'https://www.sciencedirect.com/science/article/pii/S1751570X2600138X'
citation: 'J. Silvestre, J. Reis, P. Casau, and P. Oliveira, "Event-Triggered Neural Network Adaptive Hybrid Attitude Control," in Nonlinear Analysis: Hybrid Systems, vol. xx, no. xx, pp. xx-xx, 2026 (in press).'
bibtex: '@article{2026_Silvestre_NAHS,<br />
  author = {João Silvestre, Joel Reis, Pedro Casau, and Paulo Oliveira},<br />
  title = {Event-Triggered Neural Network Adaptive Hybrid Attitude Control},<br />
  journal = {Nonlinear Analysis: Hybrid Systems}<br />
  year={2026},<br />
  volume={63},<br />
  pages={101812},<br />
  doi = {10.1016/j.nahs.2026.101812}<br />
}'
---
**Abstract**
---
In this paper, we develop an adaptive controller for rigid-body attitude tracking systems that combines a neural network architecture with an event-triggered mechanism. 
We design a quaternion-based nonlinear controller that employs a neural network to compensate for state-based disturbances and/or modeling errors.
The attitude tracking error can be made arbitrarily small by appropriate tuning of the controller parameters.
Using well-posed hybrid systems theory, we show that the proposed controller is robust to noise and does not suffer from chattering or unwinding phenomena.
Afterward, we extend our design to accommodate an event-triggered mechanism featuring a sample-and-hold of the state signal, which lowers the required number of controller updates sent to the actuators, and therefore reduces wear on moving mechanical parts.
The proposed design renders a compact neighborhood of the null error set semi-globally asymptotically stable for the closed-loop system.
Simulation results are presented to assess and illustrate the performance attained by our solution.
