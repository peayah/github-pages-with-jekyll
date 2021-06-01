---
layout: page
title: Portfolio
permalink: /portfolio/
---
{% for piece in site.portfolio-pieces reversed%}
  <img src = "{{ piece.img }}" alt = "{{ piece.imgalt }}" class="img-responsive" style="height: 60%; float: right; margin-right: 10px;" />
  <h2>{{ piece.title }} </h2>
  <p><b>Technology used: </b>{{piece.tech}} / <a href="../_code-samples/{{ piece.code }}">code</a></p>
  See my [About](../_code-samples/visualizer) page for details.

  <p><b>My Contribution: </b>{{piece.contribution}} {{piece.type}}</p>
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  
{% endfor %}
