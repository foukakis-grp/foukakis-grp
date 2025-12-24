---
title: "Foukakis Lab - News"
layout: textlay
excerpt: "Foukakis Lab -- News"
sitemap: false
permalink: /allnews.html
---

# News

<div class="news-archive">
{% for article in site.data.news %}
<div class="news-archive-entry">
  <p class="news-archive-date">{{ article.date }}</p>
  <div class="news-archive-body">{{ article.headline | markdownify }}</div>
  <hr>
</div>
{% endfor %}
</div>
