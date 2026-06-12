---
title: "Hybrid triggering adaptive prescribed performance control of underactuated UAVs"
collection: publications
permalink: /publication/2025_Kong_TIE
excerpt: 'We present a novel hybrid triggering framework for trajectory tracking of underactuated unmanned aerial vehicles (UAVs), incorporating adaptive prescribed performance specifications on the position error.'
year: 2026
venue: tie
publisher: ieee
type: 'journal'
number: 25
authors: [linghuan, reis, weihe, silvestre]
paperurl: 'http://web.tecnico.ulisboa.pt/ist164985/publications/2025_TIE_Hybrid_triggering_adaptive_prescribed_performance_control_of_underactuated_UAVs.pdf'
citation: 'L. Kong, J. Reis, W. He and C. Silvestre, "Hybrid Triggering Adaptive Prescribed Performance Control of Underactuated UAVs," in IEEE Transactions on Industrial Electronics, vol. 73, no. 7, pp. 10242-10253, July 2026'
bibtex: '@article{2025_Kong_TIE,<br />
  doi = {10.1109/TIE.2026.3658643},<br />
  year = {2026},<br />
  month = jul,<br />
  publisher = {IEEE},<br />
  volume = {73},<br />
  number = {7},<br />
  pages = {10242--10253},<br />
  author = {Linghuan Kong and Joel Reis and Wei He and Carlos Silvestre},<br />
  title = {Hybrid triggering adaptive prescribed performance control of underactuated UAVs},<br />
  journal = {IEEE Transactions on Industrial Electronics}<br />
}'
---
**Abstract**
---
This paper presents a novel hybrid triggering framework for trajectory tracking of underactuated unmanned aerial vehicles (UAVs), incorporating adaptive prescribed performance specifications on the position error.
Unlike traditional bounds that decay exponentially over time, we design less conservative performance bounds that evolve with the converging error, providing a tighter constraint.
To address bandwidth limitations and enhance tracking accuracy, we introduce a novel hybrid triggering mechanism that fully fuses the advantages of both traditional continuous-time implementations and event-triggered methods and effectively responds to the varying sampling requirements in different control phases.
This approach allows discrete control input updates within intervals of arbitrary duration, thereby avoiding Zeno behavior.
The uncertain and potentially time-varying vehicle mass is estimated using an adaptive law derived through backstepping.
We demonstrate that the closedloop system is uniformly ultimately bounded, thus ensuring that the performance bounds are enforced.
The effectiveness and robustness of our approach are demonstrated through simulation and experimental results.
