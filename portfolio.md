---
layout: page
title: Portfolio
permalink: /portfolio/
---
{% for piece in site.portfolio-pieces %}
  <h2>{{ piece.title }}</h2>
  <code> has number {{piece.organization}}</code>
  <p><b>Technology used: </b>{{piece.tech}}
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  
{% endfor %}
