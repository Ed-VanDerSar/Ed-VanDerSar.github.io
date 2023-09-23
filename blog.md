---
layout: page
title: "Blog"
---

<div style="text-align:center;">
  <img src="/assets/pictures/mapache1.jpeg" alt="mapache">
</div>

This space is devoted to the topics I find worthwhile talking about or simply to the things I like and enjoy exploring. For instance, I will post 
(in Spanish) about mathematics, books, poetry cooking and so on. 


{% if site.show_excerpts %}
  {% include home.html %}
{% else %}
  {% include archive.html title="Posts" %}
{% endif %}
