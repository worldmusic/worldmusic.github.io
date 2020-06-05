---
layout: default
title: Resources
description: Other useful resources from across the internet
permalink: /resources/
---

One of our goals is to provide links to some of the many open and online resources available online that are related to the teaching and study of world music. These are not exhaustive, but may provide starting points for research or reading. If you would like to add any resources or suggest a bibliography, please email [Christopher Witulski][email].

{% for bib in site.resources %}
{% include resource.html bib=bib %}
{% endfor %}

[email]: mailto:cwituls@bgsu.edu
