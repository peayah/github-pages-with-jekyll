---
layout: page
title: Observations
permalink: /observations/

---
{% for post in site.posts %} 

  {% if post.categories contains 'piece' %}
  {{post.title}}
  {% endif %}
{% endfor %}

