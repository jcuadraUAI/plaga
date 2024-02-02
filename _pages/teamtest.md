---
title: "TEST Plaga Members"
layout: default
excerpt: "TEST Plaga Members"
sitemap: false
permalink: /teamtest/
---
# Group Members


Jump to [faculty and postdocs](#faculty-and-postdocs), [students](#students), [alumni](#alumni).

## Faculty and Postdocs

{% assign number_printed = 0 %}
{% for z in site.data.teamtest_members %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
<div class="row">
{% endif %}
{% include person.html %}
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}



## Students

{% assign number_printed = 0 %}
{% for z in site.data.students_test %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
<div class="row">
{% endif %}
{% include person.html %}
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
