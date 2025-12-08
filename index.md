---
layout: home
title: "Ryan Truong"
header:
  show_navigation: true
---
Welcome to my website! Feel free to explore my website and check out my projects!

{% for project in site.projects %}
  <h2>
    <a href="{{ project.url }}">
      {{ project.title }} - {{ project.date }}
    </a>
  </h2>
  <p>{{ project.content | markdownify }}</p>
{% endfor %}
