---
title: "Foukakis Group - Publications"
layout: gridlay
excerpt: "Foukakis Group -- Publications."
sitemap: false
years: [2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010]
permalink: /publications/
---
<!-- _pages/publications.md -->


# Publications

(See also the personal webpage of our group members)

## Group highlights

(For a full list of publications, see [below](#full-list-of-publications), and see also the personal webpage of our group members)

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
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


<!-- ## Patents

{% for patent in site.data.patents %}

  <em>{{ patent.authors }}</em><br />{{ patent.title }}<br /> <a href="{{patent.url}}">{{ patent.identifier }} ({{patent.year}})</a>

{% endfor %} -->

## Full List of publications

<!-- ### Under Review
<div class="publications">
  
{% bibliography -f publications -q @*[published={{0}}]* %}

</div>

### Published -->
<div class="publications">

{%- for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f publications -q @*[year={{y}}]* %}
{% endfor %}

</div>
