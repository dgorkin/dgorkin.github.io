---
layout: page
title: people
permalink: /people/
description: Members of the Gorkin Lab, past and present.
nav: true
nav_order: 2
---

<div class="row row-cols-1 row-cols-md-3 g-4 my-4">
{% assign current = site.data.people | where: "status", "current" %}
{% for person in current %}
  <div class="col">
    <div class="card h-100 shadow-sm">
      {% if person.photo %}
        <img src="{{ '/assets/img/people/' | append: person.photo | relative_url }}" class="card-img-top" alt="{{ person.name }}" style="object-fit: cover; aspect-ratio: 1/1;">
      {% endif %}
      <div class="card-body">
        <h5 class="card-title mb-1">{{ person.name }}</h5>
        <p class="text-muted small mb-2">{{ person.role }}</p>
        {% if person.email %}<p class="small mb-1"><i class="fa-solid fa-envelope"></i> {{ person.email }}</p>{% endif %}
        {% if person.links %}
          <p class="small mb-0">
          {% for link in person.links %}<a href="{{ link.url }}" class="me-2">{{ link.label }}</a>{% endfor %}
          </p>
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>

## Lab alumni

<ul>
{% assign alumni = site.data.people | where: "status", "alumni" %}
{% for person in alumni %}
  <li><strong>{{ person.name }}.</strong> {{ person.role }}{% if person.years %} {{ person.years }}{% endif %}.</li>
{% endfor %}
</ul>

## Group photos & fun

<div class="row row-cols-1 row-cols-md-2 g-3 my-3">
{% for photo in site.data.group_photos %}
  <div class="col">
    <figure class="figure">
      <img src="{{ '/assets/img/group/' | append: photo.file | relative_url }}" class="figure-img img-fluid rounded" alt="{{ photo.caption }}">
      <figcaption class="figure-caption text-center">{{ photo.caption }}</figcaption>
    </figure>
  </div>
{% endfor %}
</div>
