---
layout: default
title: Projects
permalink: /projects/
---

# Projects

<ul class="project-list">
{% assign items = site.projects | sort: 'date' | reverse %}
{% for p in items %}
  <li class="project-item">
    <h2><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h2>
    {% if p.description %}<p>{{ p.description }}</p>{% endif %}
    {% if p.tech %}<p><strong>Stack:</strong> {{ p.tech }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
