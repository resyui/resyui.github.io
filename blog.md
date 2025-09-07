---
layout: default
title: Blog
permalink: /blog/
---

# Blog

<ul class="project-list">
{% assign posts_sorted = site.posts %}
{% for post in posts_sorted %}
  <li class="project-item">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    {% if post.description %}<p>{{ post.description }}</p>{% endif %}
    <p><small>{{ post.date | date: "%Y-%m-%d" }}</small></p>
  </li>
{% endfor %}
</ul>
