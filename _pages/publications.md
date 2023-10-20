---
layout: archive
title: "List of Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %} 
{% assign url = gsDataBaseUrl | append: "stats/data_shieldsio.json" %}

{% if site.author.googlescholar %}
  You may track the citations to my publications at <a href='https://scholar.google.com/citations?user=QIi3y4wAAAAJ&hl=en'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=Google Scholar"></a>
{% endif %}

Publications in Journals
------

{% for post in site.publications reversed %}
  {% if post.type == 'journal' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

Publications in Conferences
------

{% for post in site.publications reversed %}
  {% if post.type == 'conference' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}