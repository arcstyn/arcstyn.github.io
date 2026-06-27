---
layout: default
title: Microblog
---

# Microblog

{% assign entries = site.pages | sort: "date" | reverse %}

{% for p in entries %}
  {% if p.path contains 'microblog/' and p.url != '/microblog/' %}
<article class="stream-entry">
  <small style="color: #666;">{{ p.date | date: "%B %d, %Y — %I:%M %p" }}</small>
  
  {{ p.content }}
</article>
<hr style="border: 0; border-top: 1px dashed #333; margin: 30px 0;">
  {% endif %}
{% endfor %}