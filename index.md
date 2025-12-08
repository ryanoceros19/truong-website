---
layout: home
title: "Ryan Truong"
header:
  show_navigation: true
---

{% for project in site.projects %}
  <h2>
    <a href="{{ project.url }}">
      {{ project.title }} - {{ project.date }}
    </a>
  </h2>
  <p>{{ project.content | markdownify }}</p>
{% endfor %}
