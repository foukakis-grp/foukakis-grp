---
title: "Foukakis Lab - Research"
layout: gridlay
excerpt: "Foukakis Lab -- Research"
sitemap: false
tags: [10001, 10002,10003]
permalink: /research/
---

# Our Research
<img src="{{ site.url }}{{ site.baseurl }}/favicon.ico" class="img-responsive" width="15%" style="float: left"/>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam risus enim, volutpat in lobortis vel, consectetur id nisl. Aenean non velit pellentesque turpis sollicitudin sodales. Nullam in erat ac nisl porta luctus. Maecenas hendrerit suscipit mauris sed vestibulum. Quisque nisi dolor, lobortis non viverra id, dignissim nec felis. Morbi posuere orci et turpis convallis congue. Nullam viverra pharetra purus, eget ultrices urna facilisis at. Etiam ac sapien sit amet erat efficitur finibus. Pellentesque vitae lorem ante.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam risus enim, volutpat in lobortis vel, consectetur id nisl. Aenean non velit pellentesque turpis sollicitudin sodales. Nullam in erat ac nisl porta luctus. Maecenas hendrerit suscipit mauris sed vestibulum. Quisque nisi dolor, lobortis non viverra id, dignissim nec felis. Morbi posuere orci et turpis convallis congue. Nullam viverra pharetra purus, eget ultrices urna facilisis at. Etiam ac sapien sit amet erat efficitur finibus. Pellentesque vitae lorem ante.


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
  <p>Team members: <em>{{ theme-item.authors }}</em></p>
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
  {{ theme-item.description }}
  <p>Team members: <em>{{ theme-item.authors }}</em></p>
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
