---
layout: default
title: Projects
permalink: /projects/
tags: projects
---



{% assign project_count = (site.pages | size) %}
<h1>Projects</h1>


<div class="home projects">
  {% if project_count > 0 %}
    <div class="posts">
      {% for project in site.pages %}
        {% if project.page-category == "project" %}

        <div class="project post py3">
          <p class="post-meta">{{ project.date | date: site.date_format }}</p>
          <a href="{{ project.url | prepend: site.baseurl }}" class="post-link"><h3 class="h2 post-title">{{ project.title }}</h3></a>
          <p class="post-summary">
            {% if project.summary %}
              {{ project.summary }}
            {% else %}
              {{ project.excerpt }}
            {% endif %}
          </p>
         
        </div>
      {% endif %}
      {% endfor %}
    </div>
  {% else %}
    <h1 class='center'>{{ site.text.index.coming_soon }}</h3>
  {% endif %}
</div>
