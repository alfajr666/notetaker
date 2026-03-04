---
title: Creative Writing
permalink: /Creative%20Writing/
---

# Creative Writing

## Posts

{% assign pages_sorted = site.pages | sort: "path" %}
{% for p in pages_sorted %}
  {% assign ext = p.path | slice: -3, 3 %}
  {% assign prefix = p.path | slice: 0, 21 %}
  {% if prefix == "Creative Writing/Post/" and ext == ".md" %}
- [{{ p.title | default: p.path }}]({{ p.url | relative_url }})
  {% endif %}
{% endfor %}

