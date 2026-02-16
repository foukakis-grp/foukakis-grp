---
title: "Foukakis Lab - Team"
layout: gridlay
excerpt: "Foukakis Lab -- Team"
sitemap: false
permalink: /team/
---

# Group Members

Meet the people behind the Foukakis Lab! We’re a team of researchers, students, and collaborators who work together to explore new ideas and push our projects forward.  

Click on each member’s name to learn more about their background, research interests, and what they’re working on.

<!-- **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!** -->

Jump to [PI](#principal-investigator), [Senior Researchers](#affiliated-to-research), [Postdocs](#postdocs), [PhD Students](#phd-students), [Master and Bachelor Students](#master-and-bachelor-students), [Admins](#administration), [Alumni](#alumni).

## Principal Investigator
{% assign number_printed = 0 %}
{% for member in site.data.team_pi %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix alumni-block">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  <h4><a data-toggle="collapse" href="#{{member.id}}-pi">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i> <!--<i><br>email: <{{ member.email }}></i> -->
  
  <div class="social-links">
  {% if member.email %}
  <a href="mailto:{{ member.email }}" title="email"><i class="fa-solid fa-envelope"></i></a>
  {% endif %}
  {% if member.website %}
  <a href="{{ member.website }}" title="Website" target="_blank" rel="noopener noreferrer"><i class="fa fa-globe"></i></a>
  {% endif %}
  {% if member.orcid_id %}
  <a href="https://orcid.org/{{ member.orcid_id }}" title="ORCID" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-orcid"></i></a>
  {% endif %}
  {% if member.scholar_userid %}
  <a href="https://scholar.google.com/citations?user={{ member.scholar_userid }}" title="Google Scholar" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-google-scholar"></i></a>
  {% endif %}
  {% if member.research_gate_profile %}
  <a href="https://www.researchgate.net/profile/{{member.research_gate_profile}}/" title="ResearchGate" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-researchgate"></i></a>
  {% endif %}
  {% if member.linkedin_username %}
  <a href="https://www.linkedin.com/in/{{ member.linkedin_username }}" title="LinkedIn" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-linkedin"></i></a>
  {% endif %}
  {% if member.x_username %}
  <a href="https://twitter.com/{{ member.x_username }}" title="X" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-x-twitter"></i></a>
  {% endif %}
  {% if member.github_username %}
  <a href="https://github.com/{{ member.github_username }}" title="GitHub" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github"></i></a>
  {% endif %}
  </div>

  <div class="collapse" id="{{member.id}}-pi" style="text-align: left; clear: both;">
  {{ member.text | newline_to_br }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}




## Senior Researchers
{% assign number_printed = 0 %}
{% for member in site.data.team_affiliated %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a data-toggle="collapse" href="#{{member.id}}-affiliated">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i> <!--<i><br>email: <{{ member.email }}></i> -->
  
  <div class="social-links">
  {% if member.email %}
  <a href="mailto:{{ member.email }}" title="email"><i class="fa-solid fa-envelope"></i></a>
  {% endif %}
  {% if member.website %}
  <a href="{{ member.website }}" title="Website" target="_blank" rel="noopener noreferrer"><i class="fa fa-globe"></i></a>
  {% endif %}
  {% if member.orcid_id %}
  <a href="https://orcid.org/{{ member.orcid_id }}" title="ORCID" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-orcid"></i></a>
  {% endif %}
  {% if member.scholar_userid %}
  <a href="https://scholar.google.com/citations?user={{ member.scholar_userid }}" title="Google Scholar" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-google-scholar"></i></a>
  {% endif %}
  {% if member.research_gate_profile %}
  <a href="https://www.researchgate.net/profile/{{member.research_gate_profile}}/" title="ResearchGate" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-researchgate"></i></a>
  {% endif %}
  {% if member.linkedin_username %}
  <a href="https://www.linkedin.com/in/{{ member.linkedin_username }}" title="LinkedIn" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-linkedin"></i></a>
  {% endif %}
  {% if member.x_username %}
  <a href="https://twitter.com/{{ member.x_username }}" title="X" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-x-twitter"></i></a>
  {% endif %}
  {% if member.github_username %}
  <a href="https://github.com/{{ member.github_username }}" title="GitHub" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github"></i></a>
  {% endif %}
  </div>

  <div class="collapse" id="{{member.id}}-affiliated" style="text-align: left;">
  {{ member.text | newline_to_br }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}




## Postdocs
{% assign number_printed = 0 %}
{% for member in site.data.team_postdocs %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a data-toggle="collapse" href="#{{member.id}}-postdoc">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i> <!--<i><br>email: <{{ member.email }}></i> -->
  
  <div class="social-links">
  {% if member.email %}
  <a href="mailto:{{ member.email }}" title="email"><i class="fa-solid fa-envelope"></i></a>
  {% endif %}
  {% if member.website %}
  <a href="{{ member.website }}" title="Website" target="_blank" rel="noopener noreferrer"><i class="fa fa-globe"></i></a>
  {% endif %}
  {% if member.orcid_id %}
  <a href="https://orcid.org/{{ member.orcid_id }}" title="ORCID" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-orcid"></i></a>
  {% endif %}
  {% if member.scholar_userid %}
  <a href="https://scholar.google.com/citations?user={{ member.scholar_userid }}" title="Google Scholar" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-google-scholar"></i></a>
  {% endif %}
  {% if member.research_gate_profile %}
  <a href="https://www.researchgate.net/profile/{{member.research_gate_profile}}/" title="ResearchGate" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-researchgate"></i></a>
  {% endif %}
  {% if member.linkedin_username %}
  <a href="https://www.linkedin.com/in/{{ member.linkedin_username }}" title="LinkedIn" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-linkedin"></i></a>
  {% endif %}
  {% if member.x_username %}
  <a href="https://twitter.com/{{ member.x_username }}" title="X" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-x-twitter"></i></a>
  {% endif %}
  {% if member.github_username %}
  <a href="https://github.com/{{ member.github_username }}" title="GitHub" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github"></i></a>
  {% endif %}
  </div>

  <div class="collapse" id="{{member.id}}-postdoc" style="text-align: left; clear: both;">
  {{ member.text | newline_to_br }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}




## PhD Students
{% assign number_printed = 0 %}
{% for member in site.data.team_phd %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a data-toggle="collapse" href="#{{member.id}}-phd">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i> <!--<i><br>email: <{{ member.email }}></i> -->
  
  <div class="social-links">
  {% if member.email %}
  <a href="mailto:{{ member.email }}" title="email"><i class="fa-solid fa-envelope"></i></a>
  {% endif %}
  {% if member.website %}
  <a href="{{ member.website }}" title="Website" target="_blank" rel="noopener noreferrer"><i class="fa fa-globe"></i></a>
  {% endif %}
  {% if member.orcid_id %}
  <a href="https://orcid.org/{{ member.orcid_id }}" title="ORCID" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-orcid"></i></a>
  {% endif %}
  {% if member.scholar_userid %}
  <a href="https://scholar.google.com/citations?user={{ member.scholar_userid }}" title="Google Scholar" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-google-scholar"></i></a>
  {% endif %}
  {% if member.research_gate_profile %}
  <a href="https://www.researchgate.net/profile/{{member.research_gate_profile}}/" title="ResearchGate" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-researchgate"></i></a>
  {% endif %}
  {% if member.linkedin_username %}
  <a href="https://www.linkedin.com/in/{{ member.linkedin_username }}" title="LinkedIn" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-linkedin"></i></a>
  {% endif %}
  {% if member.x_username %}
  <a href="https://twitter.com/{{ member.x_username }}" title="X" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-x-twitter"></i></a>
  {% endif %}
  {% if member.github_username %}
  <a href="https://github.com/{{ member.github_username }}" title="GitHub" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github"></i></a>
  {% endif %}
  </div>

  <div class="collapse" id="{{member.id}}-phd" style="text-align: left; clear: both;">
  {{ member.text | newline_to_br }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}




## Master and Bachelor Students
{% assign number_printed = 0 %}
{% for member in site.data.team_students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a data-toggle="collapse" href="#{{member.id}}-student">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i> <!--<i><br>email: <{{ member.email }}></i> -->
  
  <div class="social-links">
  {% if member.email %}
  <a href="mailto:{{ member.email }}" title="email"><i class="fa-solid fa-envelope"></i></a>
  {% endif %}
  {% if member.website %}
  <a href="{{ member.website }}" title="Website" target="_blank" rel="noopener noreferrer"><i class="fa fa-globe"></i></a>
  {% endif %}
  {% if member.orcid_id %}
  <a href="https://orcid.org/{{ member.orcid_id }}" title="ORCID" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-orcid"></i></a>
  {% endif %}
  {% if member.scholar_userid %}
  <a href="https://scholar.google.com/citations?user={{ member.scholar_userid }}" title="Google Scholar" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-google-scholar"></i></a>
  {% endif %}
  {% if member.research_gate_profile %}
  <a href="https://www.researchgate.net/profile/{{member.research_gate_profile}}/" title="ResearchGate" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-researchgate"></i></a>
  {% endif %}
  {% if member.linkedin_username %}
  <a href="https://www.linkedin.com/in/{{ member.linkedin_username }}" title="LinkedIn" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-linkedin"></i></a>
  {% endif %}
  {% if member.x_username %}
  <a href="https://twitter.com/{{ member.x_username }}" title="X" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-x-twitter"></i></a>
  {% endif %}
  {% if member.github_username %}
  <a href="https://github.com/{{ member.github_username }}" title="GitHub" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github"></i></a>
  {% endif %}
  </div>

  <div class="collapse" id="{{member.id}}-student" style="text-align: left; clear: both;">
  {{ member.text | newline_to_br }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}




## Administration
{% assign number_printed = 0 %}
{% for member in site.data.team_admin %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a data-toggle="collapse" href="#{{member.id}}-admin">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i> <!--<i><br>email: <{{ member.email }}></i> -->
  
  <div class="social-links">
  {% if member.email %}
  <a href="mailto:{{ member.email }}" title="email"><i class="fa-solid fa-envelope"></i></a>
  {% endif %}
  {% if member.website %}
  <a href="{{ member.website }}" title="Website" target="_blank" rel="noopener noreferrer"><i class="fa fa-globe"></i></a>
  {% endif %}
  {% if member.orcid_id %}
  <a href="https://orcid.org/{{ member.orcid_id }}" title="ORCID" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-orcid"></i></a>
  {% endif %}
  {% if member.scholar_userid %}
  <a href="https://scholar.google.com/citations?user={{ member.scholar_userid }}" title="Google Scholar" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-google-scholar"></i></a>
  {% endif %}
  {% if member.research_gate_profile %}
  <a href="https://www.researchgate.net/profile/{{member.research_gate_profile}}/" title="ResearchGate" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-researchgate"></i></a>
  {% endif %}
  {% if member.linkedin_username %}
  <a href="https://www.linkedin.com/in/{{ member.linkedin_username }}" title="LinkedIn" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-linkedin"></i></a>
  {% endif %}
  {% if member.x_username %}
  <a href="https://twitter.com/{{ member.x_username }}" title="X" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-x-twitter"></i></a>
  {% endif %}
  {% if member.github_username %}
  <a href="https://github.com/{{ member.github_username }}" title="GitHub" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github"></i></a>
  {% endif %}
  </div>

  <div class="collapse" id="{{member.id}}-admin" style="text-align: left; clear: both;">
  {{ member.text | newline_to_br }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}



 
<div class="alumni-section" id="alumni">
<h2>Alumni</h2>

{% for member in site.data.alumni_members %}
<b>{{ member.name }}</b>,&nbsp; <i>{{ member.role }}</i>,&nbsp; <i>{{ member.date }}</i> &nbsp;&nbsp; {% if member.thesis_url %}
    <i><a href="{{ member.thesis_url }}" target="_blank" rel="noopener noreferrer">“{{ member.thesis }}”</a></i>
  {% else %}
    <i>{{ member.thesis }}</i>
  {% endif %}
{% endfor %}

</div>
 
