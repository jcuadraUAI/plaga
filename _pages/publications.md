---
title: "PLAGA - Publications"
layout: gridlay
excerpt: "PLAGA group -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

For a full list see [below](#full-list), or follow this [ADS link](https://ui.adsabs.harvard.edu/search/filter_database_fq_database=OR&filter_database_fq_database=database%3A%22astronomy%22&filter_property_fq_property=AND&filter_property_fq_property=property%3A%22refereed%22&format=SHORT&fq=%7B!type%3Daqp%20v%3D%24fq_database%7D&fq=%7B!type%3Daqp%20v%3D%24fq_property%7D&fq_database=(database%3A%22astronomy%22)&fq_property=(property%3A%22refereed%22)&q=author%3A(%22Cuadra%2C%20Jorge%22%20or%20%22Montesinos%2C%20M%22%20or%20%22Dunhill%2C%20A%22%20or%20%22Faramaz%2C%20V%22%20or%20%22Chen%2C%20X%22%20or%20%22Russell%2C%20C%22%20or%20%22Cuello%2C%20N%22%20or%20%22Ronco%22%20or%20%22Guilera%2C%20O%22%20or%20%22del%20Valle%2C%20L%22%20or%20%22Castillo%2C%20F%22%20or%20%22Becerra%2C%20L%22%20or%20%22Sucerquia%2C%20M%22%20or%20%22Stammler%2C%20S%22%20or%20%22Calder%C3%B3n%2C%20D%22%20or%20%22Goicovic%22%20or%20%22Garate%2C%20M%22%20or%20%22Fontecilla%2C%20C%22%20)%20aff%3A(%22catolica%22%20or%20%22adolfo%22)%20%20year%3A2015-2020&sort=date%20desc%2C%20bibcode%20desc&unprocessed_parameter=qform&p_=0) (may contain false positives).

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List
 (since 2015)
 
{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
