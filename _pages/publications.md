---
layout: page
permalink: /publications/
title: publications
description: Publications from the Gorkin Lab, sourced from PubMed.
nav: true
nav_order: 5
years: [2035, 2034, 2033, 2032, 2031, 2030, 2029, 2028, 2027, 2026, 2025, 2024, 2023, 2022, 2021]
---

<div class="publications">
{%- comment -%} Recent years: one heading per year, skipping any year with no publications. {%- endcomment -%}
{% for y in page.years %}
  {% capture entries %}{% bibliography -f papers -q @*[year={{ y }}]* %}{% endcapture %}
  {% assign has_entries = entries | strip_html | strip %}
  {% unless has_entries == "" %}
  <h2 class="year">{{ y }}</h2>
  {{ entries }}
  {% endunless %}
{% endfor %}

{%- comment -%} Everything before 2021 collapsed into a single "Before 2021" category, newest first. {%- endcomment -%}
{% capture older %}{% for y in (2000..2020) reversed %}{% bibliography -f papers -q @*[year={{ y }}]* %}{% endfor %}{% endcapture %}
{% assign older_has = older | strip_html | strip %}
{% unless older_has == "" %}

  <h2 class="year">Before 2021</h2>
  {{ older }}
{% endunless %}
</div>

<hr>

<p class="text-muted small">
Publication list is auto-generated from a BibTeX file (<code>_bibliography/papers.bib</code>) and mirrors <a href="https://pubmed.ncbi.nlm.nih.gov/?term=Gorkin+D%5BAuthor%5D">PubMed's Gorkin D[Author] index</a>. Author corrections and errata are excluded by design. To flag a missing publication, please email Dr. Gorkin.
</p>
