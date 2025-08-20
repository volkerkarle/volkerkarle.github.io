---
layout: page
title: projects
permalink: /projects/
description: Research project pages linked to my publications.
nav: true
nav_order: 5
display_categories: [work, fun]
horizontal: false
---

<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
<a id="{{ page.display_categories[0] }}" href=".#{{ page.display_categories[0] }}"><h2 class="category">{{ page.display_categories[0] }}</h2></a>
{% assign categorized_projects = site.projects | where: "category", page.display_categories[0] %}
{% assign sorted_projects = categorized_projects | sort: "importance" %}
{% if page.horizontal %}
<div class="container"><div class="row row-cols-1 row-cols-md-2">
{% for project in sorted_projects %}{% include projects_horizontal.liquid %}{% endfor %}
</div></div>
{% else %}
<div class="row row-cols-1 row-cols-md-3">
{% for project in sorted_projects %}{% include projects.liquid %}{% endfor %}
</div>
{% endif %}
{% if page.display_categories.size > 1 %}
<a id="{{ page.display_categories[1] }}" href=".#{{ page.display_categories[1] }}"><h2 class="category">{{ page.display_categories[1] }}</h2></a>
{% endif %}
{% else %}
{% assign sorted_projects = site.projects | sort: "importance" %}
{% if page.horizontal %}
<div class="container"><div class="row row-cols-1 row-cols-md-2">
{% for project in sorted_projects %}{% include projects_horizontal.liquid %}{% endfor %}
</div></div>
{% else %}
<div class="row row-cols-1 row-cols-md-3">
{% for project in sorted_projects %}{% include projects.liquid %}{% endfor %}
</div>
{% endif %}
{% endif %}
</div>
