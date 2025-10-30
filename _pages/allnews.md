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
<div style="margin-left: 2em; overflow: auto;" markdown="0">
  {% if article.image %}
  <img src="{{ article.image }}" class="img-responsive" style="max-height: 400px; width: auto; float: right; margin-left: 15px; margin-bottom: 10px;">
  {% endif %}
  {% if article.description %}
  <div markdown="1">{{ article.description | markdownify }}</div>
  {% endif %}
</div>
{% endif %}
{% endfor %}
