---
title: Observations
permalink: /observations/
layout: observations
---

{% for observation in site.observations %}
  <h2>{{ observation.title }}</h2>
  <p><i>{{observation.date}}</i></p>
  <p>{{ observation.content | markdownify }}</p>
{% endfor %}
