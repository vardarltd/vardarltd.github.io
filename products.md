---
layout: page
title: Ürünler
permalink: /products/
onMenu: true
order: 1
---

{% for page in site.pages %}
  {% if page.type == 'product' %}
# <a class="page-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
_{{ page.subtitle }}_
  {% endif %}
{% endfor %}
