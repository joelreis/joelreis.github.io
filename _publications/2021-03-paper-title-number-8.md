---
title: "Attitude, body-fixed Earth rotation rate, and sensor bias estimation using single observations of direction of gravitational field"
collection: publications
permalink: /publication/2021-03-paper-title-number-8
excerpt: 'This paper addresses the problem of estimating the attitude of a robotic platform using biased measurements of: (i) the direction of the gravitational field and (ii) angular velocity obtained from a set of high-grade gyroscopes sensitive to the Earth’s rotation.'
date: 2021-03-01
venue: automatica
publisher: elsevier
type: 'journal'
number: 8
authors: [reis,batista,oliveira,silvestre]
publisherurl: 'https://www.sciencedirect.com/science/article/pii/S0005109820306749'
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2021_AUTOMATICA_Attitude_body_fixed_Earth_rotation_rate_and_sensor_bias_estimation_using_single_observations_of_direction_of_gravitational_field.pdf'
citation: 'J. Reis, P. Batista, P. Oliveira, and C. Silvestre, “Attitude, body-fixed Earth rotation rate, and sensor bias estimation using single observations of direction of gravitational field,” Automatica, vol. 125. Elsevier BV, p. 109475, Mar. 2021.'
bibtex: '@article{2021_Reis_Automatica,<br />
  doi = {10.1016/j.automatica.2020.109475},<br />
  url = {https://doi.org/10.1016/j.automatica.2020.109475},<br />
  year = {2021},<br />
  month = mar,<br />
  publisher = {Elsevier {BV}},<br />
  volume = {125},<br />
  pages = {109475},<br />
  author = {Joel Reis and Pedro Batista and Paulo Oliveira and Carlos Silvestre},<br />
  title = {Attitude, body-fixed Earth rotation rate, and sensor bias estimation using single observations of direction of gravitational field},<br />
  journal = {Automatica}<br />
}'
---
**Abstract**
---
This paper addresses the problem of estimating the attitude of a robotic platform using biased measurements of: (i) the direction of the gravitational field and (ii) angular velocity obtained from a set of high-grade gyroscopes sensitive to the Earth’s rotation.
A cascade solution is proposed that features a Kalman filter (KF) tied to a rotation matrix observer built on the special orthogonal group of order 3. The KF, whose model stems from a uniformly observable linear time-varying system, yields estimates of: (i) the Earth’s total rotational rate; (ii) two sensor biases associated with the aforementioned measurements; and, (iii) noise-filtered and bias-corrected accelerometer data.
All estimates are expressed in the platform’s body-fixed frame.
In turn, the attitude observer put forward is shown to be almost globally asymptotically stable, in particular locally input-to-state stable with respect to the KF errors.
Experimental results are showcased that successfully demonstrate the efficiency of the proposed attitude estimation solution.
