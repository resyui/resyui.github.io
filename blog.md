---
layout: default
title: Blog
permalink: /blog/
---

# Blog

<ul class="project-list">
{% assign posts_sorted = site.posts | sort: 'date' | reverse %}
{% for post in posts_sorted %}
  <li class="project-item">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p><small>{{ post.date | date: "%Y-%m-%d" }}</small></p>
    {% if post.description %}
      <p>{{ post.description }}</p>
    {% else %}
      {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
      {% endif %}
    {% endif %}
  </li>
{% endfor %}
</ul>
