---
layout: page
permalink: /publications/
title: publications
description: publications in reversed chronological order.
years: [2025, 2024, 2023, 2022, 2021, 2020]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
