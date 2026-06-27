---
layout: default
title: Essays
---

# Essays

{% assign raw_pages = site.pages | sort: "date" | reverse %}

{% for p in raw_pages %}
  {% if p.path contains 'essays/' and p.url != '/essays/' %}
- [{{ p.title }}]({{ p.url | relative_url }}) - *{{ p.date | date: "%B %d, %Y" }}*
  {% endif %}
{% endfor %}