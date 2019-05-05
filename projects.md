---
title: Projects
layout: page
---
{% for project in site.projects %}
* __[{{ project.title }}]({{ project.url }})__<br>
  {{ project.short }}
{% endfor %}
