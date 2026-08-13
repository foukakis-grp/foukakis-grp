---
title: "Foukakis Lab - Publications"
layout: gridlay
excerpt: "Foukakis Lab -- Publications."
sitemap: false
years: [2026, 2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010]
permalink: /publications/
---
<!-- _pages/publications.md -->


# Publications
## Group highlights

For the complete publication list, jump to the [full list below](#full-list-of-publications). You can also visit our [team page]({{ site.baseurl }}/team) for individual members’ profiles and their publications.

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
  <p><strong><a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a></strong></p>
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

<!-- Recent Publications -->

## Recent Publications

<div class="recent-publications">

{% bibliography -f publications --max 6 -T bib_recent %}

</div>

<p>&nbsp;</p>

## Full List of publications

<div class="publications">

{%- for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f publications -q @*[year={{y}}]* %}
{% endfor %}

</div>
