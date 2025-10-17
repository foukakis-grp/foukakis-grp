---
title: "Foukakis Lab - Funding"
layout: textlay
excerpt: "Foukakis Lab -- Funding."
sitemap: false
permalink: /funding/
---

# Our Funding and Support
We are grateful to the following organizations that generously fund our activities:
- [Karolinska Institutet](http://ki.se)
- [Swedish Research Council](https://www.vr.se)
- [Cancerfonden](https://www.cancerfonden.se)
- [Radiumhemmets Forskningsfonder](https://www.rahfo.se)
- [Horizon Europe - European Commision](https://research-and-innovation.ec.europa.eu/funding/funding-opportunities/funding-programmes-and-open-calls/horizon-europe_en)

as well as those which support us with computational resources:
- [NAISS](http://naiss.se)
	- [Alvis @ Chalmers](https://www.c3se.chalmers.se/about/Alvis/)
	- [Biana @ UPPMAX](https://docs.uppmax.uu.se/cluster_guides/bianca/)

<div class="row">

<div class="col-sm-2 clearfix vcenter" style="margin: 0 50px 0 0;">
<img src="{{ site.url }}{{ site.baseurl }}/images/logopic/ki_logo_rgb.png" style="width: 180px;">
</div>

<div class="col-sm-2 clearfix vcenter" style="margin: 0 50px 0 0;">
<img src="{{ site.url }}{{ site.baseurl }}/images/logopic/rahfo.svg" style="width: 180px;">
</div>

<div class="col-sm-2 clearfix vcenter" style="margin: 0 50px 0 0;">
<img src="{{ site.url }}{{ site.baseurl }}/images/logopic/cancerfonden.webp" style="width: 180px;">
</div>

</div>


<div class="row">

<div class="col-sm-2 clearfix vcenter" style="margin: 0 50px 0 0px;">
<img src="{{ site.url }}{{ site.baseurl }}/images/logopic/european_commission.jpg" style="width: 180px">
</div>

<div class="col-sm-2 clearfix vcenter" style="margin: 0 50px 0 0;">
<img src="{{ site.url }}{{ site.baseurl }}/images/logopic/naiss.jpg" style="width: 180px;">
</div>

<div class="col-sm-2 clearfix vcenter" style="margin: 0 50px 0 0;">
<img src="{{ site.url }}{{ site.baseurl }}/images/logopic/alvis_logo.svg" style="width: 180px;">
</div>


</div>

Their funding supports our work in research, education, and outreach, not the least through our scientific projects.

### Ongoing projects

{% for project in site.data.project %}

{% if project.ongoing == 1 %}
<div class="row">
<div class="well">

#### {{ project.title }} ({{ project.period}})

**Call:** {{project.category}}, *funded by the* {{ project.agency}}

**Awarded to:** {{project.lead}}

**USLC Members:** {{project.member}}

<a data-toggle="collapse" href="#{{project.key}}-bib"  class="btn-abstract" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">**Popular Abstract**</a>
<div class="collapse" id="{{project.key}}-bib"><div class="well-abs">
{{ project.summary }}
</div></div>
</div>
</div>

{% endif %}

{% endfor %}


<h4><a href="{{ site.url }}{{ site.baseurl }}/allprojects.html">... see all Projects</a></h4>
