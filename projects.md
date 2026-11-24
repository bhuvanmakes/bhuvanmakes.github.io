---
layout: page
title: Projects
permalink: /projects/
lede: Featured hardware I design, build and document.
---

{% assign projects = site.projects | sort: "order" %}
<ul class="project-list">
{% for project in projects %}
  <li>
    {% if project.status %}<p class="badge">{{ project.status }}</p>{% endif %}
    <a class="title" href="{{ project.url | relative_url }}">{{ project.title }}</a>
    <p class="meta">{{ project.summary }}</p>
  </li>
{% endfor %}
</ul>
