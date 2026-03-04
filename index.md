---
title: Notes
---

# Notes

This is a published view of the notes in this repo.

## Browse

{% assign pages_sorted = site.pages | sort: "path" %}
{% for p in pages_sorted %}
{% assign ext = p.path | slice: -3, 3 %}
{% if p.path != "index.md" and ext == ".md" and p.url %}
- [{{ p.path }}]({{ p.url | relative_url }})
{% endif %}
{% endfor %}
