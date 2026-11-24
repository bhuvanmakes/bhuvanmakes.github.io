---
layout: page
title: Projects
permalink: /projects/
lede: Things I design, build and write about.
---

{% assign projects = site.projects | sort: "order" %}
<ul class="project-rows">
{% for project in projects %}
  {% include project-card.html project=project %}
{% endfor %}
</ul>
