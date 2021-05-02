---
layout: page
title: Portfolio
permalink: /portfolio/
---
{% for piece in site.portfolio-pieces %}
  <h2>{{ piece.title }}</h2>
  <p><em>Technology used:</em>{{piece.tech}}
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  
{% endfor %}
