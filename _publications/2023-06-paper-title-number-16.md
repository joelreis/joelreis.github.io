---
title: "Comprehensive nonlinear control strategy for VTOL-UAVs with windowed output constraints"
collection: publications
permalink: /publication/2023-06-paper-title-number-16
excerpt: 'In this paper we develop a methodology for trajectory tracking control of a vertical take-off and landing unmanned aerial vehicle in the presence of unknown mass and time-varying external disturbances.'
date: 2023-06-01
venue: tcst
publisher: ieee
type: 'journal'
number: 16
authors: [linghuan, reis, weihe, silvestre]
publisherurl: 'https://ieeexplore.ieee.org/document/10197442'
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2023_TCST_Comprehensive_nonlinear_control_strategy_for_VTOL_UAVs_with_windowed_output_constraints.pdf'
citation: 'L. Kong, J. Reis, W. He, and C. Silvestre, “Comprehensive Nonlinear Control Strategy for VTOL-UAVs With Windowed Output Constraints,” IEEE Transactions on Control Systems Technology, vol. 31, no. 6. Institute of Electrical and Electronics Engineers (IEEE), pp. 2673–2684, Nov. 2023.'
bibtex: '@article{2023_Kong_TCST,<br />
  doi = {10.1109/tcst.2023.3286044},<br />
  url = {https://doi.org/10.1109/tcst.2023.3286044},<br />
  year = {2023},<br />
  month = nov,<br />
  publisher = {Institute of Electrical and Electronics Engineers ({IEEE})},<br />
  volume = {31},<br />
  number = {6},<br />
  pages = {2673--2684},<br />
  author = {Linghuan Kong and Joel Reis and Wei He and Carlos Silvestre},<br />
  title = {Comprehensive Nonlinear Control Strategy for {VTOL}-{UAVs} With Windowed Output Constraints},<br />
  journal = {{IEEE} Transactions on Control Systems Technology}<br />
}'
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