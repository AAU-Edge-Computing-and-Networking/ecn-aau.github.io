---
title: "News"
layout: gridlay
excerpt: "ECN AAU -- News"
sitemap: false
permalink: /allnews.html
---

# News

{% for news in site.data.news %}

<div class="col-sm-12 clearfix">

 <div class="well">
  <a href="{{ news.url }}"><img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{% if news.image %}{{news.image}}{% else %}default3.png{% endif %}" class="img-responsive" width="100%" style="border-radius: 0; max" /></a>
  <h3><a href="{{ news.url }}" style="color: inherit;">{{ news.title }}</a></h3>
  <p><i>{{news.date}}, by {{ news.author }}</i></p>
  <p>{{ news.excerpt }}</p>
 </div>
</div>
{% endfor %}

