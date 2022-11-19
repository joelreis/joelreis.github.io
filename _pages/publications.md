---
layout: archive
title: "List of Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

Publications in Journals
------

{% for post in site.publications reversed %}
  {% if post.type == 'journal' %}
    here
  {% endif %}
{% endfor %}

Publications in Conferences
------

