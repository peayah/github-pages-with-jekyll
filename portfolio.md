---
layout: page
title: Portfolio
permalink: /portfolio/
---
{% for piece in site.portfolio-pieces reversed%}
  <h2>{{ piece.title }}</h2>

  <p><b>Technology used: </b>{{piece.tech}}
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  
{% endfor %}
