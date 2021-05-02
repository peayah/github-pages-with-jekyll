---
layout: page
title: Portfolio
permalink: /portfolio/
---
{% for piece in site.portfolio-pieces reversed%}
  <h2>{{ piece.title }}</h2>
  

  <p><b>Technology used: </b>{{piece.tech}}
  <p><b>My Contribution: </b>{{piece.contribution}} {{piece.type}}
  <p>{{ piece.content | markdownify }} {{piece.type}}</p>
  <br/>
  <hr>
  <br/>
  
{% endfor %}
