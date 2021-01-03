---
title: "NIP Gravity Group -- Alumni"
layout: gridlay
excerpt: "NIP Gravity Alumni"
sitemap: false
permalink: /alumni/
---

# Gravity Alumni

Membership to the Gravity Group is contingent on a selective and rigorous apprenticeship program that strengthens mathematical methods (dimensional analysis, dynamical systems, special functions, and differential geometry) and soft research skills (writing, LaTeX). All members are required to take General Relativity as one of their electives. Students work on research projects that develop strong proficiency in Mathematica and/or Python, and are expected to subject their research work to peer review by submitting to the annual SPP (Philippine Physics Society) conference proceedings. 

We conduct a lively <b> Monday Journal Club </b> that keeps us abreast on the latest research developments, and also improves students' critical thinking, public speaking, and their ability to think on their feet. To foster imagination and cultivate broad interest in physics, we also host our informal <b>Crazy Gravity Fridays</b>, in which we critically discuss physics topics outside our areas of expertise, usually starting with popular science articles from <i> Physics Today </i> or <i> Quanta Magazine </i>. Finally, we organize an intense and highly interactive <b>Annual Gravity Workshop</b> that runs for two weeks in the midyear/summer term, in which professors and students take turns lecturing, calculating, and coding, on various topics in gravity and geometry. 

These activities help ensure success in a wide variety of careers. We are proud of our alumni who have brought their skills to different sectors of society in different parts of the world.



{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  {{ member.duration }} <br> <i> -- {{ member.info }}</i>
  <ul style="overflow: hidden">

  </ul>
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

<!--
## Former visitors, BSc/ MSc students
<div class="row">

<div class="col-sm-4 clearfix">
<h4>Visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Master students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Bachelor Students</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>
-->
