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
citation: 'Gan Yu, Joel Reis and Carlos Silvestre, "Quadrotor Neural Network Adaptive Control: Design and Experimental Validation," IEEE Robotics and Automation Letters, 2023.'
bibtex: '@ARTICLE{yu2023-ral,<br />
  title     = "Quadrotor Neural Network Adaptive Control: Design and Experimental Validation",<br />
  author    = "Yu, Gan and Reis, Joel and Silvestre, Carlos",<br />
  journal   = "IEEE Robotics and Automation Letters",<br />
  publisher = "Institute of Electrical and Electronics Engineers (IEEE)",<br />
  pages     = "1--8",<br />
  year      =  2023}'
---
**Abstract**
---
This letter presents the design and experimental study of an adaptive nonlinear controller for Unmanned Aerial Vehicles (UAVs) in the presence of unknown time-varying disturbances, and model parametric uncertainty.
We employ an adaptive Neural Network (NN), used to approximate the partially unknown system, in tandem with a simple controller designed for trajectory tracking, not of the center of mass, but of a point located along the UAV’s vertical body axis.
This strategy allows: (i) to avoid the two-subsystems control paradigm generally adopted by conventional UAV controllers; (ii) all control inputs to be defined at once; and (iii) to lump all unknown dynamics from both translational and rotational levels into a single vector term.
The weights of the NN are determined online by an adaptive law based on the Lyapunov synthesis method.
The tracking and adaptation errors are shown to be uniformly ultimately bounded.
Simulation and experimental results, including comparison data, are provided to validate and assess the proposed control solution.


