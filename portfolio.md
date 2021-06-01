---
layout: page
title: Portfolio
permalink: /portfolio/
---

{% for post in site.categories.visualizer %} 
  <a href="{{ post.url }}">{{post.title}}</a>
{% endfor %}

{% for post in site.categories.piece %} 
  <a href="{{ post.url }}">{{post.title}}</a>
{% endfor %}

{% for piece in site.portfolio-pieces reversed %}


  <img src = "{{ piece.img }}" alt = "{{ piece.imgalt }}" class="img-responsive" style="height: 60%; float: right; margin-right: 10px;" />

  <h2>{{ piece.title }} </h2>

  <p><b>Technology used: </b>{{piece.tech}} / <a href= "{{ piece.codeurl }}">code</a></p>
  
  
  
  <p><b>My Contribution: </b>{{piece.contribution}} {{piece.type}}</p>
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
{% endfor %}

