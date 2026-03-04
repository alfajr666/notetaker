---
title: Research Library
permalink: /Market_Intelligence/10_Research_Library/
---

# Research Library

{% assign pages_sorted = site.pages | sort: "path" %}
{% assign count = 0 %}
{% for p in pages_sorted %}
  {% assign ext = p.path | slice: -3, 3 %}
  {% if p.path contains "Market_Intelligence/10_Research_Library/" and ext == ".md" and p.path != "Market_Intelligence/10_Research_Library/index.md" %}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

_Found {{ count }} notes._

{% for p in pages_sorted %}
  {% assign ext = p.path | slice: -3, 3 %}
  {% if p.path contains "Market_Intelligence/10_Research_Library/" and ext == ".md" and p.path != "Market_Intelligence/10_Research_Library/index.md" %}
- [{{ p.title | default: p.path }}]({{ p.url | relative_url }})
  {% endif %}
{% endfor %}
