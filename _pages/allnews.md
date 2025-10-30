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
<div style="overflow: auto; margin-left: 2em;">
  {% if article.image %}
  <img src="{{ article.image }}" class="img-responsive" style="max-height: 215px max-width: auto; float: right; margin-left: 15px; margin-bottom: 10px;">
  {% endif %}
  {% if article.description %}
  <div>{{ article.description | markdownify }}</div>
  {% endif %}
</div>
{% endif %}
{% endfor %}
