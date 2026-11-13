---
layout: page
title: Teaching
permalink: /teaching/
description:
nav: true
nav_order: 3
horizontal: false
---

<!-- Display only the two teaching courses -->

{% assign sorted_projects = site.projects | sort: "importance" %}

<div class="projects">
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% assign filename = project.path | split: "/" | last %}
      {% if filename == "FLI_SCI.md" or filename == "ISS_325.md" %}
        {% include projects.liquid %}
      {% endif %}
    {% endfor %}
  </div>
</div>
