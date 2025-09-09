---
layout: default
title: Blog
permalink: /blog/
---

# Blog

<div class="project-list">
  {% for post in site.posts %}
  <div class="project-item">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.date | date: "%B %d, %Y" }} - {{ post.excerpt | strip_html | truncatewords: 30 }}</p>
  </div>
  {% endfor %}
</div>

{% if site.posts.size == 0 %}
<p>No posts yet. Check back soon for market hypothesis and insights!</p>
{% endif %}
