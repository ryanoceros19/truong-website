---
title: "Projects"
layout: collection
permalink: /projects/
collection: projects
entries_layout: grid
classes: wide
---
{% for project in site.projects %}
  <h2>
    <a href="{{ project.url }}">
      {{ project.title }} - {{ project.date }}
    </a>
  </h2>
  <p>{{ project.content | markdownify }}</p>
{% endfor %}
