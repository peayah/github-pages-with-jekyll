---
layout: page
title: Portfolio
permalink: /portfolio/
---
{% for piece in site.portfolio-pieces reversed%}
  <h2>{{ piece.title }} </h2>
  

  <p><b>Technology used: </b>{{piece.tech}} / <a href="{{ piece.code }}"> code</a></p>
  <p><b>My Contribution: </b>{{piece.contribution}} {{piece.type}}</p>
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  
{% endfor %}
