---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* B.S. in Aerospace Engineering, Instituto Superior Técnico, Lisbon, 2011
* M.S. in Aerospace Engineering, Instituto Superior Técnico, Lisbon, 2013
* Ph.D in Electrical and Computer Engineering, University of Macau, 2019

Awards
======

* 2022 FDCT Funding Scheme for Postdoctoral Researchers of Higher Education Institutions
  * Macau, China
  * Awarded a post-doctoral fellowship for a period of 24 months.

* 2020 First Zhuhai Wanshan International Intelligent Vessel Competition
  * Zhuhai, China
  * Winner of Sailing Race Project - Development of a path following controller for an unmanned surface vessel.

* 2020 Macau Science and Technology Development Fund (FDCT)
  * Macau, China
  * Recipient of Scientific and Technological R&D Award for Postgraduates.

Work experience
======
* 2022–2024 University of Macau: Post-doctoral Fellow
  * Funded by the FDCT Funding Scheme for Postdoctoral Researchers of Higher Education Institutions of the UM
Macao Talent Programme.
  * Period of two years dedicated to the practical development and testing of prototypes for autonomous aerial
and underwater vehicles.

* 2019–2021 Faculty of Science and Technology, University of Macau: Research Assistant
  * Involved in UM Funded projects STEALTH (STate EstimAtion in Large neTworks with Heterogenous agents) and SECANTS (Self-triggered and Event-triggered Control of Autonomous NeTworked Systems, and in FDCT funded project SLOTMAV (Slung Load Transportation by Multiple Aerial Vehicles).

* 2012–2014 Institute for Systems and Robotics, Lisbon: Fellow Researcher
  * Worked in the Project MAST/AM: Advanced Tracking and Telemetry Methodologies to Study Marine Animals, which was funded by FCT —Fundação para a Ciência e Tecnologia. Main work consisted in programming a Digital Signal Processor C6713 from Texas Instruments that served as the backbone of an ultra-short baseline acoustic positioning system.
  
Skills
======
* Matlab
* Python
* C/C++,
* ROS
* Git
* Linux
* SolidWorks
* LATEX

Professional service
======
* Journal Reviewer
  * IEEE Transactions on Automatic Control
  * IEEE Transactions on Cybernetics
  * IEEE Transactions on Systems, Man, and Cybernetics
  * IEEE/ASME Transactions on Mechatronics
  * IEEE Transactions on Aerospace and Electronic Systems
  * IEEE Transactions on Cognitive and Developmental Systems
  * IEEE Sensors Journal
  * IEEE Transactions on Instrumentation and Measurement
  * Automatica
  * Asian Journal of Control
  * The International Journal of Robotic Research
  * Ocean Engineering
* Conference Reviewer
  * IEEE Conference on Decision and Control (CDC)
  * IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)
  * The International Conference on Unmanned Aircraft Systems (ICUAS)

Publications
======

in Journals
------

  {% for post in site.publications reversed %}
    {% if post.type == 'journal' %}
      {% include archive-single-cv.html %}
    {% endif %}
  {% endfor %}

in Conferences
------

  {% for post in site.publications reversed %}
    {% if post.type == 'conference' %}
      {% include archive-single-cv.html %}
    {% endif %}
  {% endfor %}
  