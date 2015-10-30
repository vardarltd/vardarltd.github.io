---
layout: page
title: Eğitimler
permalink: /training/
onMenu: true
order: 3
---
<ul >
  {% for page in site.pages %}
    {% if page.type == 'training' %}
    <li ><a class="page-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>