---
title: "News"
layout: textlay
excerpt: "Roy Lab at West Texas A&M University"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<div class="news-item">
  <div class="news-date">{{ article.date }}</div>
  <div class="news-headline">{{ article.headline | markdownify }}</div>
</div>
{% endfor %}

<style>
.news-item {
  margin-bottom: 1.5rem;
}
.news-date {
  font-weight: bold;
  margin-bottom: 0.2rem;
}
.news-headline p {
  margin: 0; /* Removes paragraph spacing */
  display: inline; /* Keeps content inline */
}
</style>