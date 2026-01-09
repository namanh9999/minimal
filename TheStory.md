---
layout: default
title: Cats Gallery
---

# 🌅 Cat Gallery

<div style="
  display:grid;
  grid-template-columns:repeat(auto-fit, minmax(220px, 1fr));
  gap:20px;
">

{% assign cat_images = site.static_files
  | where_exp: "file", "file.path contains '/assets/story/'"
%}

{% for image in cat_images %}
  {% assign name = image.name | remove: image.extname %}

  <a href="{{ site.baseurl }}/assets/story/{{ name }}.html"
     style="text-decoration:none;">

    <img src="{{ site.baseurl }}{{ image.path }}"
         loading="lazy"
         style="width:100%; border-radius:14px; cursor:pointer;">

  </a>
{% endfor %}

</div>
