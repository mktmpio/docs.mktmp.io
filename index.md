---
title: Docs Home
skip_nav: true
---

# Welcome to the mktmpio docs!

<ul>
{% assign pages = site.html_pages | sort: 'title' %}
{% for p in pages %}
  <li><a href="{{ p.url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>

### Temporary databases that start up faster than you read this tagline.
