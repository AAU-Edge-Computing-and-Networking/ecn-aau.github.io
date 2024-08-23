---
title: "ECN AAU - Publications"
layout: gridlay
excerpt: "ECN AAU -- Publications."
sitemap: false
permalink: /publications/
---

## Publications from primary affiliated members

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

## Publications from secondary affiliated members
