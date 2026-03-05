---
title: "Foukakis Lab - Research"
layout: gridlay
excerpt: "Foukakis Lab -- Research"
sitemap: false
tags: [10001, 10002, 10003, 10004, 10005]
permalink: /research/
---

# Our Research
Our projects span the translational spectrum — from patient care to molecular discovery and computational innovation — all centered around improving outcomes for individuals with breast cancer. By combining clinical insights with data-driven methodologies, we explore how tumors evolve, resist treatment, and respond to new therapeutic strategies.

Each project is shaped by collaboration — across disciplines within the lab and with external partners in academia, healthcare, and industry. Together, we aim to translate biological understanding into real-world clinical benefit. To learn more about our ongoing projects or to explore collaborative opportunities, please get in touch with us. We welcome new ideas, partnerships, and perspectives that can drive innovation in breast cancer research.

## Research themes
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
  <div class="theme-desc">
  {{ theme-item.description | markdownify }}
  </div>

  {% if theme-item.key == "projtheme1" and theme-item.trials %}
  <ul>
  {%- for t in theme-item.trials -%}
    <li><a href="{{ site.baseurl }}/trials/{{ t.slug }}/">{{ t.name }}</a></li>
  {%- endfor -%}
  </ul>
  {% endif %}

  {% if theme-item.contact %}
  <p><b>Contact person:</b> <em>{{ theme-item.contact }}</em></p>
  {% endif %}

  {% if theme-item.members and theme-item.key != "projtheme1" %}
  <p><b>Associated members:</b> <em>{{ theme-item.members }}</em></p>
  {% endif %}

  {% if theme-item.news1 %}
  <p class="text-danger"><strong>{{ theme-item.news1 }}</strong></p>
  {% endif %}
  {% if theme-item.news2 %}
  <p>{{ theme-item.news2 }}</p>
  {% endif %}

  {% unless theme-item.key == "projtheme1" %}
  <a data-toggle="collapse" href="#{{theme-item.key}}-bib" class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">Selected papers</a>
  <div class="collapse" id="{{theme-item.key}}-bib"><div class="well-abs"><div class="publications">
  {%- for y in page.tags -%}
    {%- if y == theme-item.tag -%}
      {% bibliography -f publications -q @*[tag={{y}}]* --template bib_trial %}
    {%- endif -%}
  {%- endfor -%}
  </div></div></div>
  {% endunless %}

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
  <div class="theme-desc">
  {{ theme-item.description | markdownify }}
  </div>

  {% if theme-item.key == "projtheme1" and theme-item.trials %}
  <ul>
  {%- for t in theme-item.trials -%}
    <li><a href="{{ site.baseurl }}/trials/{{ t.slug }}/">{{ t.name }}</a></li>
  {%- endfor -%}
  </ul>
  {% endif %}

  {% if theme-item.contact %}
  <p><b>Contact person:</b> <em>{{ theme-item.contact }}</em></p>
  {% endif %}

  {% if theme-item.members and theme-item.key != "projtheme1" %}
  <p><b>Associated members:</b> <em>{{ theme-item.members }}</em></p>
  {% endif %}

  {% if theme-item.news1 %}
  <p class="text-danger"><strong>{{ theme-item.news1 }}</strong></p>
  {% endif %}
  {% if theme-item.news2 %}
  <p>{{ theme-item.news2 }}</p>
  {% endif %}

  {% unless theme-item.key == "projtheme1" %}
  <a data-toggle="collapse" href="#{{theme-item.key}}-bib" class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">Selected papers</a>
  <div class="collapse" id="{{theme-item.key}}-bib"><div class="well-abs"><div class="publications">
  {%- for y in page.tags -%}
    {%- if y == theme-item.tag or y == theme-item.taga -%}
      {% bibliography -f publications -q @*[tag={{y}}]* --template bib_trial %}
    {%- endif -%}
  {%- endfor -%}
  </div></div></div>
  {% endunless %}

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