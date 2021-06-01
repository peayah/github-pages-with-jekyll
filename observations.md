---
layout: page
title: Observations
permalink: /observations/

---
{% for piece in site.portfolio-pieces reversed %}

  {% if post.categories contains 'piece' %}
  {{post.title}}
  {% endif %}
{% endfor %}

