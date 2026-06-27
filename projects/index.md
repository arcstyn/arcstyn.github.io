---
layout: default
title: Projects
---

# Projects

{% assign projects = site.pages | sort: "date" | reverse %}

{% for p in projects %}
  {% if p.path contains 'projects/' and p.url != '/projects/' %}
<article class="project-entry">
  <h2>{{ p.title }}</h2>
  <small style="color: #666;">Updated: {{ p.date | date: "%B %d, %Y" }}</small>

  {{ p.content }}
</article>
<hr style="border: 0; border-top: 1px dashed #333; margin: 40px 0;">
  {% endif %}
{% endfor %}