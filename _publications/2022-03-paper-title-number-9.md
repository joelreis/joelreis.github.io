---
title: "Earth velocity and rigid-body attitude estimation on SO(3) using biased measurements"
collection: publications
permalink: /publication/2022-03-paper-title-number-9
excerpt: 'This article addresses the problem of simultaneously estimating: 1) the attitude of a rigid body on the special orthogonal group of order 3; 2) the Earth’s spin vector expressed in body-fixed coordinates; and 3) a pair of time-varying sensor measurement biases.'
date: 2022-03-01
venue: tmech
publisher: ieee
type: 'journal'
number: 9
authors: [reis,batista,oliveira,silvestre]
publisherurl: 'https://ieeexplore.ieee.org/document/9731767'
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2022_TMECH_Earth_Velocity_and_Rigid-Body_Attitude_Estimation_on_SO3_Using_Biased_Measurements.pdf'
citation: 'J. Reis, P. Batista, P. Oliveira, and C. Silvestre, “Earth Velocity and Rigid-Body Attitude Estimation on SO(3) Using Biased Measurements,” IEEE/ASME Transactions on Mechatronics, vol. 27, no. 6. Institute of Electrical and Electronics Engineers (IEEE), pp. 4246–4257, Dec. 2022.'
bibtex: '@article{2022_Reis_TMECH,<br />
  doi = {10.1109/tmech.2022.3152220},<br />
  url = {https://doi.org/10.1109/tmech.2022.3152220},<br />
  year = {2022},<br />
  month = dec,<br />
  publisher = {Institute of Electrical and Electronics Engineers ({IEEE})},<br />
  volume = {27},<br />
  number = {6},<br />
  pages = {4246--4257},<br />
  author = {Joel Reis and Pedro Batista and Paulo Oliveira and Carlos Silvestre},<br />
  title = {Earth Velocity and Rigid-Body Attitude Estimation on {SO}(3) Using Biased Measurements},<br />
  journal = {{IEEE}/{ASME} Transactions on Mechatronics}<br />
}'
---
**Abstract**
---
This article addresses the problem of simultaneously estimating: 1) the attitude of a rigid body on the special orthogonal group of order 3 ( $$\mathsf {SO}(3)$$ ); 2) the Earth’s spin vector expressed in body-fixed coordinates; and 3) a pair of time-varying sensor measurement biases.
The available sensor readings include biased angular velocity measurements collected from a set of high-grade rate gyros sensitive to the rotation of the planet and biased vector observations of some known inertial reference field.
The estimation solution consists of a Lagrangian-based pseudo Kalman filtering routine, which is partially constrained to $$\mathsf {SO}(3)$$ vis-á-vis the attitude.
Most noticeably, the geometric relationship between the Earth’s angular velocity and the inertial field is leveraged to relax common practical, as well as theoretical, demands closely linked to conventional attitude estimation solutions, namely, the need for explicit body-fixed measurements of two inertial vector fields.
The proposed algorithm is validated through a set of realistic simulations.
Experimental results are also included to further demonstrate the performance of this strategy in a real-world application.