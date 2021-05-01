---
layout: page
title: Observations
permalink: /observations/

---


{% for observation in site.observations reversed %}
  {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
  <span class="post-meta">{{ observation.date | date: date_format }}</span>
  <h2>{{ observation.title }}</h2>
  <p>{{ observation.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  
{% endfor %}
