---
title: "Kalman Filter Cascade for Attitude Estimation on Rotating Earth"
collection: publications
permalink: /publication/2020-02-paper-title-number-6
excerpt: 'This article presents a discrete-time attitude estimation solution based on a cascade of two linear time-varying Kalman filters.'
date: 2020-02-01
venue: tmech
publisher: ieee
type: 'journal'
number: 6
authors: [reis,batista,oliveira,silvestre]
publisherurl: 'https://ieeexplore.ieee.org/document/8931000'
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2020_TMECH_Kalman_Filter_Cascade_for_Attitude_Estimation_on_Rotating_Earth.pdf'
citation: 'J. Reis, P. Batista, P. Oliveira, and C. Silvestre, “Kalman Filter Cascade for Attitude Estimation on Rotating Earth,” IEEE/ASME Transactions on Mechatronics, vol. 25, no. 1. Institute of Electrical and Electronics Engineers (IEEE), pp. 327–338, Feb. 2020.'
bibtex: '@article{2020_Reis_TMECH,<br />
  doi = {10.1109/tmech.2019.2959080},<br />
  url = {https://doi.org/10.1109/tmech.2019.2959080},<br />
  year = {2020},<br />
  month = feb,<br />
  publisher = {Institute of Electrical and Electronics Engineers ({IEEE})},<br />
  volume = {25},<br />
  number = {1},<br />
  pages = {327--338},<br />
  author = {Joel Reis and Pedro Batista and Paulo Oliveira and Carlos Silvestre},<br />
  title = {Kalman Filter Cascade for Attitude Estimation on Rotating Earth},<br />
  journal = {{IEEE}/{ASME} Transactions on Mechatronics}<br />
}'
---
**Abstract**
---
This paper presents a discrete-time attitude estimation solution based on a cascade of two linear time-varying Kalman filters (KFs).
Under mild assumptions, the cascade's first KF resorts to body-fixed measurements of angular velocity and of a constant inertial vector to yield an estimate of Earth's angular velocity.
The latter, in addition to all previous measurements, is fed to the second KF to obtain an estimate of the rotation matrix.
Although topological constructions are lifted, a last-step projection operator is employed that maps the final rotation matrix estimate onto SO(3).
Briefly, two linear time-varying systems are designed, with no linearisations whatsoever, that are shown to be uniformly completely observable, thus rendering the overall solution globally exponentially stable.
Simulation results are presented that allow to assess the performance of the cascaded KF duo.
A set of experimental results is also presented that validates the efficiency of the proposed solution and deems it a suitable attitude estimation choice for applications where only one body-vector measurement is available.
