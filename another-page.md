---
layout: default
title: Cats Gallery
---

# 🐱 Cat Gallery

<div style="
  display:grid;
  grid-template-columns:repeat(auto-fit, minmax(220px, 1fr));
  gap:20px;
">

{% assign cat_images = site.static_files | where_exp: "file", "file.path contains '/assets/img/Cat/'" %}

{% for image in cat_images %}
<img src="{{ site.baseurl }}{{ image.path }}", loading="crazy",
style="width:100%; border-radius:14px;">
{% endfor %}

</div>

[back](./)
