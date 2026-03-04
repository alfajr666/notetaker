---
title: BrainDump
permalink: /BrainDump/
---

# BrainDump

{% assign pages_sorted = site.pages | sort: "path" %}
{% for p in pages_sorted %}
  {% assign ext = p.path | slice: -3, 3 %}
  {% assign prefix = p.path | slice: 0, 9 %}
  {% if prefix == "BrainDump/" and ext == ".md" and p.path != "BrainDump/index.md" %}
- [{{ p.title | default: p.path }}]({{ p.url | relative_url }})
  {% endif %}
{% endfor %}

