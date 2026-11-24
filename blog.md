---
layout: page
title: Blog
permalink: /blog/
lede: Longer write-ups of projects, and later, YouTube videos.
---

{% if site.posts.size > 0 %}
<ul class="post-list">
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <p class="meta">
      <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: '%-d %B %Y' }}</time>
    </p>
    {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncate: 220 }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
<p>No posts published yet.</p>
{% endif %}
