---
layout: page
title: projects
permalink: /projects/
description: Robotics research, creative projects, and community work.
nav: true
nav_order: 2
display_categories: [research, entrepreneurship, service]
---

<link rel="stylesheet" href="{{ '/assets/css/projects.css' | relative_url }}">
<div class="project-gallery">
{% for category in page.display_categories %}
  <section class="project-category" aria-labelledby="{{ category }}">
    <h2 id="{{ category }}">{{ category | capitalize }}</h2>
    <div class="project-grid">
    {% assign projects = site.projects | where: "category", category | sort: "importance" %}
    {% for project in projects %}
      <a class="project-card" href="{{ project.url | relative_url }}">
        <div class="project-card-media">
          <img src="{{ project.img | relative_url }}" alt="{{ project.title | escape }}" loading="lazy">
        </div>
        <div class="project-card-content">
          <p class="project-card-period">{{ project.period }}</p>
          <h3>{{ project.title }}</h3>
          <p class="project-card-description">{{ project.description }}</p>
        </div>
      </a>
    {% endfor %}
    </div>
  </section>
{% endfor %}
</div>
