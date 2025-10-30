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
<div style="margin-left: 2em;">
  {% if article.image %}
  <div style="text-align: center; margin-bottom: 10px;">
    <img src="{{ article.image }}" class="img-responsive" style="max-height: 400px; width: auto; display: inline-block;">
  </div>
  {% endif %}
  {% if article.description %}
  <div>{{ article.description | markdownify }}</div>
  {% endif %}
</div>
{% endif %}
{% endfor %}
