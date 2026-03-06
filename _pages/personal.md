---
layout: archive
title: "Personal"
permalink: /personal/
author_profile: true
---

<style>
.photo-gallery figure figcaption {
  opacity: 0;
  transition: opacity 0.3s ease;
}
.photo-gallery figure:hover figcaption {
  opacity: 1;
}
</style>

Welcome to my personal photo gallery! Here are some of my nature and travel photography favorites:

<div class="photo-gallery">
  {% assign captions = site.data.personal_captions %}
  {% for image in site.static_files %}
    {% if image.path contains '/assets/img/personal/' %}
      {% assign caption = captions[image.name] | default: (image.name | split:'.' | first) %}
      <figure style="display:inline-block; margin:10px; position:relative;">
        <a href="{{ image.path | relative_url }}" data-lightbox="gallery" data-title="{{ caption }}">
          <img src="{{ image.path | relative_url }}" alt="{{ caption }}" style="width: 200px; border-radius: 8px; cursor: pointer;">
        </a>
        <figcaption style="position:absolute; bottom:8px; left:8px; right:8px; background:rgba(0,0,0,0.85); color:white; padding:6px 8px; border-radius:4px; pointer-events:none; font-size:0.85em;">{{ caption }}</figcaption>
      </figure>
    {% endif %}
  {% endfor %}
</div>
