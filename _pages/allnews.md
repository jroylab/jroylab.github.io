---
title: "News"
layout: textlay
excerpt: "Roy Lab at West Texas A&M University"
sitemap: false
permalink: /allnews.html
---

# News

{% assign news = site.data.news | sort: 'date' | reverse %}
{% for article in news -%}
{{ article.date }} {{ article.headline }}
{%- endfor %}
