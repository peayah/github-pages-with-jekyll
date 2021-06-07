---
layout: page
title: Portfolio
permalink: /portfolio/
---

{% for piece in site.portfolio-pieces reversed %}

 {% if piece.categories contains 'piece' %}

  <img src = "{{ piece.img }}" alt = "{{ piece.imgalt }}" class="img-responsive" style="height: 60%; float: right; margin-right: 10px;" />

  <h2>{{ piece.title }} </h2>
  <a href="./{{piece.code | relative_url}}"> version two</a>
  <a href="{{piece.code | relative_url}}"> version three</a>

  Read more [version 4](./visualizer.md?raw=1)


  
  <p><b>Technology used: </b>{{piece.tech}} / <a href= "{{ piece.codeurl }}/">code</a></p>  
  
  <p><b>My Contribution: </b>{{piece.contribution}} {{piece.type}}</p>
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  {% endif %}
{% endfor %}

