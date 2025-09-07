---
layout: default
title: Blog
permalink: /blog/
---

# Blog

<ul class="project-list">
{% assign items = site.articles | sort: 'date' | reverse %}
{% for a in items %}
  <li class="project-item">
    <h2><a href="{{ a.url | relative_url }}">{{ a.title }}</a></h2>
    <p><small>{{ a.date | date: "%Y-%m-%d" }}</small></p>
    {% if a.description %}
      <p>{{ a.description }}</p>
    {% else %}
      {% if a.excerpt %}
        <p>{{ a.excerpt | strip_html | truncate: 160 }}</p>
      {% endif %}
    {% endif %}
  </li>
{% endfor %}
</ul>
