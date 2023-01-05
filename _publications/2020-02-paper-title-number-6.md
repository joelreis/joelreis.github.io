---
title: "Kalman Filter Cascade for Attitude Estimation on Rotating Earth"
collection: publications
permalink: /publication/2020-02-paper-title-number-6
excerpt: 'This article presents a discrete-time attitude estimation solution based on a cascade of two linear time-varying Kalman filters.'
date: 2020-02-01
venue: tmech
type: 'journal'
number: 6
authors: [reis,batista,oliveira,silvestre]
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2020_TMECH_Kalman_Filter_Cascade_for_Attitude_Estimation_on_Rotating_Earth.pdf'
citation: 'Joel Reis, Pedro Batista, Paulo Oliveira and Carlos Silvestre, "Kalman Filter Cascade for Attitude Estimation on Rotating Earth," IEEE-ASME Transactions on Mechatronics, vol. 25, no. 1, pp. 327-338, Feb. 2020, doi:10.1109/TMECH.2019.2959080.'
bibtex: '@ARTICLE{Reis2020-no,<br />
  title     = "Kalman filter cascade for attitude estimation on rotating earth",<br />
  author    = "Reis, Joel and Batista, Pedro and Oliveira, Paulo and Silvestre, Carlos",<br />
  journal   = "IEEE ASME Trans. Mechatron.",<br />
  publisher = "Institute of Electrical and Electronics Engineers (IEEE)",<br />
  volume    =  25,<br />
  number    =  1,<br />
  pages     = "327--338",<br />
  month     =  feb,<br />
  year      =  2020}'
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
