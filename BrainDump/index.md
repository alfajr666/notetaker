---
title: BrainDump
permalink: /BrainDump/
---

# BrainDump

{% assign pages_sorted = site.pages | sort: "path" %}
{% assign count = 0 %}
{% for p in pages_sorted %}
  {% assign ext = p.path | slice: -3, 3 %}
  {% if p.path contains "BrainDump/" and ext == ".md" and p.path != "BrainDump/index.md" %}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

_Found {{ count }} notes._

{% for p in pages_sorted %}
  {% assign ext = p.path | slice: -3, 3 %}
  {% if p.path contains "BrainDump/" and ext == ".md" and p.path != "BrainDump/index.md" %}
- [{{ p.title | default: p.path }}]({{ p.url | relative_url }})
  {% endif %}
{% endfor %}
