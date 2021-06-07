---
layout: page
title: Portfolio
permalink: /portfolio/
---

{% for piece in site.portfolio-pieces reversed %}

 {% if piece.categories contains 'piece' %}

  <img src = "{{ piece.img }}" alt = "{{ piece.imgalt }}" class="img-responsive" style="height: 60%; float: right; margin-right: 10px;" />

  <h2>{{ piece.title }} </h2>
  <a href="../current_projects.md"> version one</a>
  {% raw %}
  Read more [version 2](./visualizer.md)

  {% endraw %}
  
  <p><b>Technology used: </b>{{piece.tech}} / <a href= "{{ piece.codeurl }}/">code</a></p>  
  
  <p><b>My Contribution: </b>{{piece.contribution}} {{piece.type}}</p>
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  {% endif %}
{% endfor %}

