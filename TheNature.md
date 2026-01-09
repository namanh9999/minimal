---
layout: default
title: Cats Gallery
---

# 🌅 Nature Gallery

<div style="
  display:grid;
  grid-template-columns:repeat(auto-fit, minmax(220px, 1fr));
  gap:20px;
">

{% assign cat_images = site.static_files | where_exp: "file", "file.path contains '/assets/img/Nature/'" %}

{% for image in cat_images %}
  <img src="{{ site.baseurl }}{{ image.path }}"
       loading="lazy"
       style="width:100%; border-radius:14px;">
{% endfor %}
</div>
<br>
<br>

[<center>Back to home page</center>](./)--