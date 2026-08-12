---
layout: page
title: projects
permalink: /projects/
description: Selected research systems, benchmarks, and clinical machine-learning projects.
nav: true
nav_order: 3
display_categories:
  - key: systems
    title: Research systems and benchmarks
  - key: clinical-ml
    title: Clinical machine learning
horizontal: true
---

For papers and venue status, see [publications](/publications/).

<div class="projects">
  {% for section in page.display_categories %}
  <a id="{{ section.key }}" href="#{{ section.key }}">
    <h2 class="category">{{ section.title }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", section.key %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
      {% endfor %}
    </div>
  </div>
  {% endfor %}
</div>
