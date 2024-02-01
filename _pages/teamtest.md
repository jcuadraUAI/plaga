---
title: "Plaga - Team"
layout: gridlay
excerpt: "Plaga: Team members"
sitemap: false
permalink: /teamtest/
---

# Group Members


Jump to [faculty and postdocs](#faculty-and-postdocs), [students](#students), [alumni](#alumni).

## Faculty and Postdocs
{% assign number_printed = 0 %}
{% for member in site.data.teamtest_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% if member.haswww == 1 %}
 <h4>[{{ member.name }}]({{ member.webpage }}){:target="_blank"}</h4>
  {% endif %}
  {% if member.haswww == 0 %}
 <h4>{{ member.name }}</h4>
  {% endif %}
<{{ member.email }}> <br>
 <i>{{ member.role }}</i><br>	
 <i> {{ member.education }}</i><br>
  {{member.area}} <br>
  	{% for lab in z.labels %}
	    {% if lab.type == "email" %}<a href="mailto:{{lab.email}}"><span style="font-size: 25px; color: Black;"><i class="fas fa-envelope"></i></span> </a> {% endif %}
	    {% if lab.type == "website" %}<a href="{{lab.website}}"><span style="font-size: 25px; color: Black;"><i class="fas fa-globe"></i></span> </a> {% endif %}
	    {% if lab.type == "twitter" %}<a href="{{lab.twitter}}"><span style="font-size: 25px; color: Black;"><i class="fab fa-twitter"></i></span></a> {% endif %} 
	    {% if lab.type == "github" %}<a href="{{lab.github}}"><span style="font-size: 25px; color: Black;"><i class="fab fa-github"></i></span></a> {% endif %} 
	    {% if lab.type == "cv" %}<a href="/resources/cvs/{{lab.cv}}"><span style="font-size: 25px; color: Black;"><i class="ai ai-cv"></i></span></a> {% endif %} 
	    {% if lab.type == "orcid" %}<a href="{{lab.orcid}}"><span style="font-size: 25px; color: Black;"><i class="fab fa-orcid"></i></span></a> {% endif %} 
  	    {% if lab.type == "googlescholar" %}<a href="{{lab.googlescholar}}"><span style="font-size: 25px; color: Black;"><i class="ai ai-google-scholar"></i></span></a> {% endif %} 
{% endfor %}

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




## Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% if member.haswww == 1 %}
 <h4>[{{ member.name }}]({{ member.webpage }}){:target="_blank"}</h4>
  {% endif %}
  {% if member.haswww == 0 %}
 <h4>{{ member.name }}</h4>
  {% endif %}
<{{ member.email }}> <br>
 <i>{{ member.role }}</i><br>	
 <i> {{ member.education }}</i><br>
  {{member.area}}
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


## Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% if member.haswww == 1 %}
 <h4>[{{ member.name }}]({{ member.webpage }}){:target="_blank"}</h4>
  {% endif %}
  {% if member.haswww == 0 %}
 <h4>{{ member.name }}</h4>
  {% endif %}
  <i>{{ member.duration }} <br></i>
  {{ member.info }}
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

## Former visitors, part-time or Summer students
(not including students who later did their thesis with us)

<div class="row">

<div class="col-sm-4 clearfix">
<h4>Long-term visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Graduate students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Undergrads</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>


<link rel="stylesheet" href="/resources/icons/fontawesome-free-5.14.0-web/css/all.css" />
<link rel="stylesheet" href="/resources/icons/academicons-1.9.0/css/academicons.css" />

