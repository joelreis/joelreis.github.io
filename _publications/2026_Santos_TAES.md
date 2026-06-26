---
title: "QuadRocket: An Aerial Robotic Testbed for Adaptive Thrust-Vector Control of Rocket-Like Vehicles"
collection: publications
permalink: /publication/2026_Santos_TAES
excerpt: 'We present QuadRocket, a quadrotor-based rocket prototype that provides a low-cost, low-risk platform for validating advanced thrust-vector control strategies for launch-vehicle–type systems..'
year: 2026
venue: taes
publisher: ieee
type: 'journal'
number: 30
authors: [santos,reis,oliveira,silvestre]
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2026_TAES_QuadRocket_An_Aerial_Robotic_Testbed_for_Adaptive_Thrust_Vector_Control_of_Rocket_Like_Vehicles.pdf'
publisherurl: 'https://ieeexplore.ieee.org/document/11578091'
citation: 'P. Santos, J. Reis, P. Oliveira, and C. Silvestre, "QuadRocket: An Aerial Robotic Testbed for Adaptive Thrust-Vector Control of Rocket-Like Vehicles," in IEEE Transactions on Aerospace and Electronic Systems, vol. xx, no. xx, pp. xx-xx, 2026 (in press).'
bibtex: '@article{2026_Santos_TAES,<br />
  url = {https://ieeexplore.ieee.org/document/11578091},<br />
  author = {Pedro Santos, Joel Reis, Paulo Oliveira, and Carlos Silvestre},<br />
  title = {QuadRocket: An Aerial Robotic Testbed for Adaptive Thrust-Vector Control of Rocket-Like Vehicles},<br />
  journal = {IEEE Transactions on Aerospace and Electronic Systems}<br />
  year={2026},<br />
  volume={xx},<br />
  pages={xx-xx},<br />
  doi = {10.1109/TAES.2026.3706328}<br />
}'
---
**Abstract**
---
This paper presents QuadRocket, a quadrotor-based rocket prototype that provides a low-cost, low-risk platform for validating advanced thrust-vector control strategies for launch-vehicle–type systems.
The prototype consists of a cylindrical main body mounted on top of a quadrotor through a universal joint, forming a flying inverted pendulum with non-negligible inertia.
For control design, the coupled system is modeled as a single axisymmetric rigid body actuated by a vectored force applied along its longitudinal axis.
A reduced-attitude representation on the two-sphere is adopted to explicitly exploit the vehicle’s axial symmetry and to decouple yaw from the thrust-vector direction.
On this model, we derive an adaptive backstepping controller that achieves almost-global trajectory tracking in the presence of unknown constant disturbances, while a control-point transformation mitigates non-minimum-phase behavior.
The quadrotor is then treated as a thrust-vector actuator, and a dynamic-surface-based attitude controller is designed to track the desired thrust vector, accounting for actuation dynamics and avoiding explicit differentiation of virtual control signals.
The complete architecture is evaluated in simulation and validated experimentally in an indoor motion-capture arena.
Results demonstrate accurate trajectory tracking, effective disturbance compensation, and confirm the suitability of the QuadRocket as a versatile testbed for thrust-vector-controlled robotic vehicles.
