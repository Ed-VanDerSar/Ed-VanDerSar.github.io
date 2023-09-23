---
layout: default
title: "Home"
---

<div style="text-align:center;">
<img src="/assets/pictures/mapache1.jpeg" alt="Texto alternativo" height="200">
</div>


{% if site.show_excerpts %}
  {% include home.html %}
{% else %}
  {% include archive.html title="Posts" %}
{% endif %}
