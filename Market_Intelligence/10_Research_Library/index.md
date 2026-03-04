---
title: Research Library
permalink: /Market_Intelligence/10_Research_Library/
---

# Research Library

{% assign pages_sorted = site.pages | sort: "path" %}
{% for p in pages_sorted %}
  {% assign ext = p.path | slice: -3, 3 %}
  {% assign prefix = p.path | slice: 0, 30 %}
  {% if prefix == "Market_Intelligence/10_Research_Library/" and ext == ".md" and p.path != "Market_Intelligence/10_Research_Library/index.md" %}
- [{{ p.title | default: p.path }}]({{ p.url | relative_url }})
  {% endif %}
{% endfor %}

