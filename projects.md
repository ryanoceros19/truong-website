---
layout: collection
title: "Projects"
collection: projects
entries_layout: grid
---


{% for project in site.projects %}
  <h2>
    <a href="{{ project.url }}">
      {{ project.title }} - {{ project.date }}
    </a>
  </h2>
  <p>{{ project.content | markdownify }}</p>
{% endfor %}
