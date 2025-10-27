---
title: "Foukakis Group - Research"
layout: gridlay
excerpt: "Foukakis Group -- Research"
sitemap: false
tags: [10001, 10002,10003]
permalink: /research/
---

# Our Research
Our projects span the translational spectrum — from patient care to molecular discovery and computational innovation — all centered around improving outcomes for individuals with breast cancer. By combining clinical insights with data-driven methodologies, we explore how tumors evolve, resist treatment, and respond to new therapeutic strategies.

Current Research Areas:
- **Treatment resistance mechanisms:** Investigating how tumors adapt to endocrine and targeted therapies at the molecular and cellular levels.
- **Biomarker discovery and validation:** Identifying molecular signatures that can predict treatment response, relapse risk, or long-term outcome.
- **Liquid biopsy and minimal residual disease:** Developing methods for detecting circulating tumor DNA and other biomarkers to monitor disease non-invasively.
- **Digital and spatial pathology:** Leveraging spatial transcriptomics, multiplex imaging, and deep learning to map the tumor microenvironment and its prognostic impact.
- **AI and precision oncology:** Integrating genomics, imaging, and clinical data using artificial intelligence to guide personalized treatment strategies.

Each project is shaped by collaboration — across disciplines within the lab and with external partners in academia, healthcare, and industry. Together, we aim to translate biological understanding into real-world clinical benefit.

To learn more about our ongoing projects or to explore collaborative opportunities, please get in touch with us. We welcome new ideas, partnerships, and perspectives that can drive innovation in breast cancer research.


## Selected research themes
{% assign paper_show = true %}


{% assign number_printed = 0 %}
{% for theme-item in site.data.research_themes %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if theme-item.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}
{% if theme-item.long == 1 %}
<div class="col-sm-12 clearfix">
 <div class="well">
 {% if theme-item.hasimage == 1 %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/{{ theme-item.image }}" class="img-responsive" width="{{ theme-item.width }}" style="float: top"/>
  {% endif %}
  <h3><pubtit>{{ theme-item.title }}</pubtit></h3>
  <p>{{ theme-item.description }}</p>
  <p><b>Team members:</b> <em>{{ theme-item.authors }}</em></p>
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
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/{{ theme-item.image }}" class="img-responsive" width="{{ theme-item.width }}" style="float: top"/>
  {% endif %}
  <h3><pubtit>{{ theme-item.title }}</pubtit></h3>
  <p>{{ theme-item.description }}</p>
  <p><b>Team members:</b> <em>{{ theme-item.authors }}</em></p>
  <p class="text-danger"><strong> {{ theme-item.news1 }}</strong></p>
  <p> {{ theme-item.news2 }}</p>
  <a data-toggle="collapse" href="#{{theme-item.key}}-bib"  class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">Selected papers</a>
<div class="collapse" id="{{theme-item.key}}-bib"><div class="well-abs"><div class="publications">
{%- for y in page.tags %}
{%- if y == theme-item.tag or y == theme-item.taga -%}
{% bibliography -f publications -q @*[tag={{y}} || taga={{y}}]]* %}
{% endif %}
{% endfor %}
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

### and more...
