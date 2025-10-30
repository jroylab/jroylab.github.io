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
{% if article.description %}
{{ article.description | markdownify }}
{% endif %}
{% if article.image %}
<img src="{{ article.image }}" class="img-responsive" style="max-width: 400px; margin-top: 10px;">
{% endif %}
{% endfor %}
