---
title: "News"
layout: textlay
excerpt: "Roy Lab at West Texas A&M University"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
**{{ article.date }}**
{{ article.headline | markdownify}}
{% if article.description or article.image %}
<div style="margin-left: 2em; display: flex; align-items: center; gap: 20px;" markdown="0">
  {% if article.description %}
  <div markdown="1" style="max-width: 400px;">{{ article.description | markdownify }}</div>
  {% endif %}
  {% if article.image %}
  <div style="flex-shrink: 0;">
    <img src="{{ article.image }}" class="img-responsive" style="max-width: 300px; height: auto;">
  </div>
  {% endif %}
</div>
{% endif %}
{% endfor %}
