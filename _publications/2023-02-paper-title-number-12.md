---
title: "Quadrotor Neural Network Adaptive Control: Design and Experimental Validation"
collection: publications
permalink: /publication/2023-02-paper-title-number-12
excerpt: 'In this letter, we present the design and experimental study of an adaptive nonlinear controller for Unmanned Aerial Vehicles (UAVs) in the presence of unknown time-varying disturbances, and model parametric uncertainty.'
date: 2023-02-01
venue: ral
type: 'journal'
number: 12
authors: [yugan, reis, silvestre]
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2023_RAL_Quadrotor_Neural_Network_Adaptive_Control_Design_and_Experimental_Validation.pdf'
citation: 'G. Yu, J. Reis and C. Silvestre, "Quadrotor Neural Network Adaptive Control: Design and Experimental Validation," in IEEE Robotics and Automation Letters, vol. 8, no. 5, pp. 2574-2581, May 2023, doi: 10.1109/LRA.2023.3254450.'
bibtex: '@ARTICLE{2023_Yu_RAL,<br />
  author={Yu, Gan and Reis, Joel and Silvestre, Carlos},<br />
  journal={IEEE Robotics and Automation Letters},<br />
  title={Quadrotor Neural Network Adaptive Control: Design and Experimental Validation},<br />
  year={2023},<br />
  volume={8},<br />
  number={5},<br />
  pages={2574-2581},<br />
  doi={10.1109/LRA.2023.3254450}}'
---
**Abstract**
---
This letter presents the design and experimental study of an adaptive nonlinear controller for Unmanned Aerial Vehicles (UAVs) in the presence of unknown time-varying disturbances, and model parametric uncertainty.
We employ an adaptive Neural Network (NN), used to approximate the partially unknown system, in tandem with a simple controller designed for trajectory tracking, not of the center of mass, but of a point located along the UAV’s vertical body axis.
This strategy allows: (i) to avoid the two-subsystems control paradigm generally adopted by conventional UAV controllers; (ii) all control inputs to be defined at once; and (iii) to lump all unknown dynamics from both translational and rotational levels into a single vector term.
The weights of the NN are determined online by an adaptive law based on the Lyapunov synthesis method.
The tracking and adaptation errors are shown to be uniformly ultimately bounded.
Simulation and experimental results, including comparison data, are provided to validate and assess the proposed control solution.


