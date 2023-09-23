---
layout: page
title: "Blog"
---

<div style="text-align:center;">
  <img src="/assets/pictures/mapache1.jpeg" alt="mapache">
</div>

{% if site.show_excerpts %}
  {% include home.html %}
{% else %}
  {% include archive.html title="Posts" %}
{% endif %}
