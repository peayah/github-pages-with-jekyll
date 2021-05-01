---
title: Observations
permalink: /observations/
layout: page
---

{% for observation in site.observations %}
  <h2>{{ observation.title }}</h2>
  
  {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
  <span class="post-meta">{{ observation.date | date: date_format }}</span>
  <p>{{ observation.content | markdownify }}</p>
  <hl>
{% endfor %}
