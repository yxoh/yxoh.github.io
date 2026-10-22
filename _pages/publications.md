---
layout: page
permalink: /publications/
title: publications
description: Please see my full publication list at <a href='https://scholar.google.de/citations?user=NNnpxzAAAAAJ'><u>google scholar</u></a>.<br>* presents equal contribution.
years: [2026,2025,2024,2022,2021]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

<h2 class="bibliography">Preprints</h2>
{% bibliography -f papers -q @*[abbr=arxiv && year>=2025]* --group_by none %}

{%- for y in page.years %}
  {% if y >= 2025 %}
  {% bibliography -f papers -q @*[year={{y}} && abbr!=arxiv]* %}
  {% else %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
  {% endif %}
{% endfor %}

</div>
