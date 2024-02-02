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

{% for z in site.data.teamtest_members %} {% include person.html %} {% endfor %}

## Students

{% for z in site.data.students_test %} {% include person.html %} {% endfor %}
