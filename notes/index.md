---
layout: default
title: Notes
---

# Notes

{% assign raw_pages = site.pages | sort: "date" | reverse %}

{% for p in raw_pages %}
  {% if p.path contains 'notes/' and p.url != '/notes/' %}
- [{{ p.title }}]({{ p.url | relative_url }}) - *{{ p.date | date: "%B %d, %Y" }}*
  {% endif %}
{% endfor %}