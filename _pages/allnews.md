---
title: "News"
layout: textlay
excerpt: "ECN AAU at Leiden University."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p markdown="0">
{{ article.date }} <br> {{ article.headline | markdownify}}
</p>
{% endfor %}
