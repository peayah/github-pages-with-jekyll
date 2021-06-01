---
layout: page
title: Portfolio
permalink: /portfolio/
---
{% for piece in site.portfolio-pieces reversed%}

  <img src = "{{ piece.img }}" alt = "{{ piece.imgalt }}" class="img-responsive" style="height: 60%; float: right; margin-right: 10px;" />

  <h2>{{ piece.title }} </h2>

  <p><b>Technology used: </b>{{piece.tech}} / <a href= "{{ piece.codeurl }}">code</a></p>
  
  {% raw %}
  My favorite search engine is [Duck Duck ().
  [Link title](site.code-samples.visualizer)
  [Link title](site.code-samples.visualizer.md)

  {% endraw %}

  <p><b>My Contribution: </b>{{piece.contribution}} {{piece.type}}</p>
  <p>{{ piece.content | markdownify }}</p>
  <br/>
  <hr>
  <br/>
  
{% endfor %}

{% for pong in site.code-samples reversed%}
<p>{{ pong.content | markdownify }}</p>
{% endfor %}
