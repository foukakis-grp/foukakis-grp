---
title: "Foukakis Lab - Datasets"
layout: textlay
excerpt: "Foukakis Lab -- Datasets"
sitemap: false
permalink: /data/
---

# Datasets

Our research builds on rich, high-quality data collected from retrospective databases and prospective clinical trials of breast cancer. Over the years, we have generated and curated a range of datasets that reflect our multidisciplinary focus — integrating clinical, molecular, imaging, and computational perspectives to better understand breast cancer, treatment pathways and improve patient outcomes.

These datasets span:

- Clinical cohorts with comprehensive treatment and outcome information
- Molecular profiling data, including genomics, transcriptomics, and proteomics
- Digital pathology images and annotations
- Longitudinal and real-world data linking molecular features with clinical courses
- AI-ready multimodal datasets for integrative model development and validation

We value collaboration and believe data sharing accelerates discovery. While some datasets are already available through public repositories, others can be shared upon request in accordance with ethical and legal requirements governing patient data.

If you are interested in accessing or collaborating around any of our datasets, please contact us — we are always open to partnerships that advance cancer research and improve patient care.


{% assign number_printed = 0 %}
{% for theme-item in site.data.datasets %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if theme-item.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}
{% if theme-item.long == 1 %}
<div class="col-sm-12 clearfix">
 <div class="well">
 {% if theme-item.hasimage == 1 %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/datapic/{{ theme-item.image }}" class="img-responsive" width="{{ theme-item.width }}" style="float: top"/>
  {% endif %}
  <h3><pubtit>{{ theme-item.title }}</pubtit></h3>
  <p>{{ theme-item.description }}</p>
  <p><b>Modalities:</b> <em>{{ theme-item.modalities }}</em></p>
  <p><b>Contacts:</b> <em>{{ theme-item.authors }}</em></p>
  <p class="text-danger"><strong> {{ theme-item.news1 }}</strong></p>
  <p> {{ theme-item.news2 }}</p>
  <a data-toggle="collapse" href="#{{theme-item.key}}-bib"  class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">Selected papers</a>
<div class="collapse" id="{{theme-item.key}}-bib"><div class="well-abs"><div class="publications">
{%- for y in page.tags %}
{%- if y == theme-item.tag -%}
{% bibliography -f publications -q @*[tag={{y}}]* %}
{% endif %}
{% endfor %}
</div></div></div>
 </div>
</div>
</div>
{% else %}
<div class="col-sm-6 clearfix">
 <div class="well">
 {% if theme-item.hasimage == 1 %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/datapic/{{ theme-item.image }}" class="img-responsive" width="{{ theme-item.width }}" style="float: top"/>
  {% endif %}
  <h3><pubtit>{{ theme-item.title }}</pubtit></h3>
  <h5>{{ theme-item.small-description }}</h5>
  <p><b>Modalities:</b> <em>{{ theme-item.modalities }}</em></p>
  <p><b>Contacts:</b> <em>{{ theme-item.authors }}</em></p>
  <p class="text-danger"><strong> {{ theme-item.news1 }}</strong></p>
  <p> {{ theme-item.news2 }}</p>
  <a data-toggle="collapse" href="#{{theme-item.key}}-bib"  class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">View more</a>
<div class="collapse" id="{{theme-item.key}}-bib"><div class="well-abs"><div class="publications">
<p>{{ theme-item.description }}</p>
</div></div></div>
 </div>
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>
