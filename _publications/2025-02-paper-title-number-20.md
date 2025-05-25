---
title: "Kinematics-informed neural network control on SO(3)"
collection: publications
permalink: /publication/2025-02-paper-title-number-20
excerpt: 'We present an adaptive geometric control method for dynamic-model-free attitude tracking on the manifold of 3D rotations (SO(3)).'
date: 2025-02-01
venue: automatica
publisher: elsevier
type: 'journal'
number: 20
authors: [reis, silvestre]
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2025_AUTOMATICA_Kinematics_informed_neural_network_control_on_SO3.pdf'
citation: 'J. Reis, and C. Silvestre, “Kinematics-informed neural network control on SO(3),” Automatica, vol. 174. Elsevier BV, p. 112172, Apr. 2025.'
bibtex: '@article{2025_Reis_Automatica,<br />
  doi = {10.1016/j.automatica.2025.112172},<br />
  url = {https://doi.org/10.1016/j.automatica.2025.112172},<br />
  year = {2025},<br />
  month = apr,<br />
  publisher = {Elsevier {BV}},<br />
  volume = {174},<br />
  pages = {112172},<br />
  author = {Joel Reis and Carlos Silvestre},<br />
  title = {Kinematics-informed neural network control on SO(3)},<br />
  journal = {Automatica}<br />
}'
---
**Abstract**
---
This paper presents an adaptive geometric control method for dynamic-model-free attitude tracking on the manifold of 3D rotations (SO(3)).
Utilizing well-established definitions of attitude errors on SO(3), we develop a general control-affine linear error system.
The input to this system is implicitly approximated by a kinematics-informed neural network (NN), which serves as the controller.
The weights of this NN, designed to be inherently bounded, are adjusted online using a modified gradient descent strategy that relies solely on system kinematics.
We demonstrate the effectiveness and online learning capability of our proposed method through comprehensive simulation results, using a satellite attitude control system as an example.
A comparative analysis is also provided to validate our approach.
