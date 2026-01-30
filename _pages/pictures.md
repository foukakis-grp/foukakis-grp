---
title: "Foukakis Lab - Pictures"
layout: piclay
excerpt: "Foukakis Lab -- Pictures"
permalink: /pictures/
---

<h1>Gallery</h1>

{% assign grouped = site.data.pictures_foukakis_ki | group_by: "category" %}

<p><strong>Jump to:</strong>
{% for group in grouped %}
<a href="#{{ group.name | slugify }}">{{ group.name }}</a>{% unless forloop.last %} · {% endunless %}
{% endfor %}
</p>

{% for group in grouped %}
<h2 id="{{ group.name | slugify }}">{{ group.name }}</h2>

{% assign subgroups = group.items | group_by: "subcat" %}
{% for sub in subgroups %}

{% if sub.name and sub.name != "" %}
<h3>{{ sub.name }}</h3>
{% endif %}

<div class="row">
{% for pic in sub.items %}
<div class="col-sm-4">
<figure style="margin-bottom: 20px;">
<img src="{{ site.baseurl }}/images/gallery/{{ pic.image }}"
     class="img-responsive"
     style="width:100%; height:auto;" />
</figure>
</div>
{% endfor %}
</div>

{% endfor %}
{% endfor %}