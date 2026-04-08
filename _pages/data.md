---
title: "Foukakis Lab - Datasets"
layout: textlay
excerpt: "Foukakis Lab -- Datasets"
sitemap: false
permalink: /data/
---

# Data

Our research builds on rich, high-quality data collected from retrospective databases and prospective clinical trials of breast cancer. Over the years, we have generated and curated a range of datasets that reflect our multidisciplinary focus, integrating clinical, molecular, imaging, and computational perspectives to better understand breast cancer, treatment pathways and improve patient outcomes.

These datasets span:

- Clinical cohorts with comprehensive treatment and outcome information
- Molecular profiling data, including genomics, transcriptomics, and proteomics
- Digital pathology images and annotations
- Longitudinal and real-world data linking molecular features with clinical courses
- AI-ready multimodal datasets for integrative model development and validation

We value collaboration and believe data sharing accelerates discovery. While some datasets are already available through public repositories, others can be shared upon request in accordance with ethical and legal requirements governing patient data.

If you are interested in accessing or collaborating around any of our datasets, please contact us, we are always open to partnerships that advance cancer research and improve patient care.

{% assign categories = "Clinical trials|Other datasets" | split: "|" %}

{% for cat in categories %}

### {{ cat }}

{% assign number_printed = 0 %}
{% for theme_item in site.data.datasets %}
{% if theme_item.highlight == 1 and theme_item.category == cat %}

{% if theme_item.trial_slug %}
{% assign target_url = '/trials/' | append: theme_item.trial_slug | append: '/' | relative_url %}
{% elsif theme_item.link %}
{% assign target_url = theme_item.link | relative_url %}
{% else %}
{% assign target_url = nil %}
{% endif %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
<div class="row">
{% endif %}

{% if theme_item.long == 1 %}
<div class="col-sm-12 clearfix">
<div class="well">

<h3>
{% if target_url %}
<a href="{{ target_url }}" style="text-decoration:none;">
<pubtit>{{ theme_item.title }}</pubtit>
</a>
{% else %}
<pubtit>{{ theme_item.title }}</pubtit>
{% endif %}
</h3>

<p>{{ theme_item.description }}</p>

{% if theme_item.modalities and theme_item.modalities != "" %}
<p><b>Available data:</b> <em>{{ theme_item.modalities }}</em></p>
{% endif %}

{% if theme_item.news1 and theme_item.news1 != "" %}
<p class="text-danger"><strong>{{ theme_item.news1 }}</strong></p>
{% endif %}
{% if theme_item.news2 and theme_item.news2 != "" %}
<p>{{ theme_item.news2 }}</p>
{% endif %}

</div>
</div>
</div>

{% else %}
<div class="col-sm-6 clearfix">
<div class="well">

<h3>
{% if target_url %}
<a href="{{ target_url }}" style="text-decoration:none;">
<pubtit>{{ theme_item.title }}</pubtit>
</a>
{% else %}
<pubtit>{{ theme_item.title }}</pubtit>
{% endif %}
</h3>

{% if theme_item.small-description %}
<h5>{{ theme_item.small-description }}</h5>
{% endif %}

{% if theme_item.modalities and theme_item.modalities != "" %}
<p><b>Modalities:</b> <em>{{ theme_item.modalities }}</em></p>
{% endif %}

{% if theme_item.news1 and theme_item.news1 != "" %}
<p class="text-danger"><strong>{{ theme_item.news1 }}</strong></p>
{% endif %}
{% if theme_item.news2 and theme_item.news2 != "" %}
<p>{{ theme_item.news2 }}</p>
{% endif %}

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

<p>&nbsp;</p>

{% endfor %}