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
<div style="overflow: auto; margin-left: 2em; display: flex; align-items: flex-start;">
  {% if article.description %}
  <div style="flex: 1; margin-right: 15px;">{{ article.description | markdownify }}</div>
  {% endif %}
  {% if article.image %}
  <img src="{{ article.image }}" class="img-responsive" style="width: 400px; height: auto; flex-shrink: 0;">
  {% endif %}
</div>
{% endif %}
{% endfor %}
