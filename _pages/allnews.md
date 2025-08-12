---
title: "News"
layout: textlay
excerpt: "Roy Lab at West Texas A&M University"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news -%}
{{ article.date }} {{ article.headline | markdownify }}
{%- endfor %}
