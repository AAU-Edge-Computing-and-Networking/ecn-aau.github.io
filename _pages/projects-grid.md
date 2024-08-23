---
title: "ECN AAU - Projects"
layout: gridlay
excerpt: "ECN AAU -- Projects."
sitemap: false
permalink: /projects-grid/
---


# Projects

## Group highlights

{% assign number_printed = 0 %}
{% for proj in site.data.projlist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if proj.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ proj.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ proj.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ proj.description }}</p>
  <p>People involved: <em>{{ proj.people }}</em><br>
  Funding: {{ proj.funding }}<br>
  Budget: {{ proj.budget }}<br>
  Duration: {{ proj.duration }}</p>
  <p><strong><a href="{{ proj.link.url }}">{{ proj.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ proj.news1 }}</strong></p>
  <p> {{ proj.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Patents
<em>Milan P Allan, S Gröblacher, RA Norte, M Leeuwenhoek</em><br />Novel atomic force microscopy probes with phononic crystals<br /> PCT/NL20-20/050797 (2020)

<em>Milan P Allan</em><br /> Methods of manufacturing superconductor and phononic elements <br /> <a href="https://patents.google.com/patent/US10439125B2/en?inventor=Milan+ALLAN&oq=inventor:(Milan+ALLAN)">US10439125B2 (2016)</a>

## Full List of publications

{% for proj in site.data.projlist %}

{{ proj.title }} <br />
<em>{{ proj.authors }} </em><br /><a href="{{ proj.link.url }}">{{ proj.link.display }}</a>

{% endfor %}
