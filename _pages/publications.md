---
layout: page
permalink: /publications/
title: publications
description: Please see my full publication list at <a href='https://scholar.google.de/citations?user=NNnpxzAAAAAJ'><u>google scholar</u></a>.<br>* presents equal contribution.
years: [2024,2023,2022,2021]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>