---
layout: page
title: travel
permalink: /travel/
description: Pictures from my travels.
nav: false
nav_order: 7
images:
  venobox: true
trips:
  - id: japan-2025-08
    title: Japan — August 2025
    photos:
      - path: assets/img/1.jpg
        title: mountains
      - path: assets/img/3.jpg
        title: cityscape
  - id: california-2025-03
    title: California — March 2025
    photos:
      - path: assets/img/5.jpg
        title: ocean
  - id: boston-2024
    title: Boston — 2024
    photos:
      - path: assets/img/11.jpg
        title: forest
---

Here are a few travel photos. Replace these with your own by adding images under `assets/img/travel/` and updating the `trips` list in this page’s front matter.

{% for trip in page.trips %}
<h2>{{ trip.title }}</h2>
<div class="row">
  {% for photo in trip.photos %}
  <div class="col-sm mt-3 mt-md-0">
    <a class="venobox" data-gall="{{ trip.id }}" href="{{ photo.path | relative_url }}" data-title="{{ photo.title }}">
      {% include figure.liquid path=photo.path title=photo.title class="img-fluid rounded z-depth-1" %}
    </a>
  </div>
  {% endfor %}
</div>
{% endfor %}
