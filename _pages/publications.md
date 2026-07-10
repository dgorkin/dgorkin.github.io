---
layout: page
permalink: /publications/
title: publications
description: Publications from the Gorkin Lab, sourced from PubMed.
nav: true
nav_order: 5
years: [2026, 2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010, 2009]
---

<div class="publications">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
</div>

<hr>

<p class="text-muted small">
Publication list is auto-generated from a BibTeX file (<code>_bibliography/papers.bib</code>) and mirrors <a href="https://pubmed.ncbi.nlm.nih.gov/?term=Gorkin+D%5BAuthor%5D">PubMed's Gorkin D[Author] index</a>. Author corrections and errata are excluded by design. To flag a missing publication, please email Dr. Gorkin.
</p>
