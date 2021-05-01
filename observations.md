---
title: Observations
permalink: /observations/
layout: page
---

{% for observation in site.observations %}
  <h2>{{ observation.title }}</h2>
  <p><i>{{observation.date}}</i></p>
  <p>{{ observation.content | markdownify }}</p>
  <hl>
{% endfor %}
