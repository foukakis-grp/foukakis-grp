---
title: "News"
layout: textlay
excerpt: "Foukakis Lab @ Karolinska Institutet"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<div>
{{ article.date | markdownify }} {{ article.headline | markdownify}} <hr>
</div>
{% endfor %}
