---
title: "NIP Gravity Group -- Alumni"
layout: gridlay
excerpt: "NIP Gravity Alumni"
sitemap: false
permalink: /alumni/
---

# Gravity Alumni

Membership to the Gravity Group is contingent on a selective and rigorous apprenticeship program designed to strengthen mathematical methods (dimensional analysis, dynamical systems, special functions, and differential geometry) and to teach soft research skills (writing, LaTeX) that are essential to scholarly work in physics. All Gravity members are required to take General Relativity as one of their electives. Students work on research projects that build strong proficiency in Mathematica and/or Python, and are expected to subject their research writing to rigorous peer review by submitting to the annual [SPP <i>Samahang Pisika ng Pilipinas</i> (Philippine Physics Society) conference proceedings](https://proceedings.spp-online.org/).

We hold a weekly <b> Monday Journal Club</b> that keeps us up-to-date on the latest research developments, and also strengthens students' critical thinking and public speaking. To foster imagination and cultivate wide interest in physics, we meet through our informal <b>Crazy Gravity Fridays</b>, during which we critically discuss physics topics outside our areas of expertise, usually starting with popular science articles from <i> Physics Today </i> or <i> Quanta Magazine.</i> These informal discussions are opportunities for us to interrogate unfamiliar topics, helping us become fluent with many ideas, while also reminding us of the underlying disciplinary unity of physics. Finally, we organize a highly interactive <b>Annual Gravity Workshop</b> that runs for two weeks in the midyear/summer term, in which faculty and students take turns lecturing, calculating, and coding, on various planned topics in gravity and geometry. These activities serve as good foundations for success in a wide variety of careers. 

We are proud of our alumni who have brought their skills to different sectors of society in different parts of the world.



{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  {{ member.duration }} <br>  After Gravity: {{ member.info }}
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
