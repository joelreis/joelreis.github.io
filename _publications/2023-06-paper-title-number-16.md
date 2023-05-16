---
title: "Comprehensive nonlinear control strategy for VTOL-UAVs with windowed output constraints"
collection: publications
permalink: /publication/2023-06-paper-title-number-16
excerpt: 'In this paper we develop a methodology for trajectory tracking control of a vertical take-off and landing unmanned aerial vehicle in the presence of unknown mass and time-varying external disturbances.'
date: 2023-06-01
venue: tcst
type: 'journal'
number: 16
authors: [linghuan, reis, weihe, silvestre]
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2023_TCST_Comprehensive_nonlinear_control_strategy_for_VTOL_UAVs_with_windowed_output_constraints.pdf'
citation: 'Linghuan Kong, Joel Reis, Wei He, Carlos Silvestre, "Comprehensive nonlinear control strategy for
VTOL-UAVs with windowed output constraints," IEEE Transactions on Control Systems Technology, 2023. (in press)'
bibtex: '@ARTICLE{2023_Kong_TCST,<br />
  title = {Comprehensive nonlinear control strategy for VTOL-UAVs with windowed output constraints},<br />
  journal   = "Transactions on Control Systems Technology",<br />
  publisher = "IEEE",<br />
  volume = {},<br />
  pages = {},<br />
  year = {2023},<br />
  issn = {},<br />
  doi = {},<br />
  author = {Linghuan Kong and Joel Reis and Wei He and Carlos Silvestre}'
---
**Abstract**
---
In this paper we develop a methodology for trajectory tracking control of a vertical take-off and landing (VTOL) unmanned aerial vehicle (UAV) in the presence of unknown mass and time-varying external disturbances.
A novel time-dependent shift function is first introduced which, alongside a set of barrier vector functions, enables a finite period of constrained outputs, namely the position and velocity errors.
The proposed controller also features two stable observers to estimate: i) the mass of the UAV; and ii) a parameter relating to the bound of the external disturbances.
The total closed-loop system error is shown to be ultimately uniformly bounded.
This proposed strategy, which requires only the first derivative of the reference trajectory and features an implicit saturation of the thrust force, is especially apt to handle three stages of flight: vertical take-off, constrained trajectory tracking, and landing.
Simulation results are presented to validate the proposed solution.
Experimental results are also included to showcase the performance of our controller in a realworld application using a quadrotor vehicle.