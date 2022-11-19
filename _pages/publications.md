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
  journal0
  {{ post.venue }}
  {% if post.collection == 'journals' %}
    journal1
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

Publications in Conferences
------

{% for post in site.publications reversed %}
  conf0
  {% if post.collection == 'conferences' %}
    conf1
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
