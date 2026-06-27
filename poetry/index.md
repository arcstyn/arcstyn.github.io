---
layout: default
title: Poetry
---

# Poetry

{% assign raw_pages = site.pages | sort: "date" | reverse %}

{% for p in raw_pages %}
  {% if p.path contains 'poetry/' and p.url != '/poetry/' %}
- [{{ p.title }}]({{ p.url | relative_url }}) - *{{ p.date | date: "%B %d, %Y" }}*
  {% endif %}
{% endfor %}