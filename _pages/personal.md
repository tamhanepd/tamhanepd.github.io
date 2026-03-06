---
layout: archive
title: "Personal"
permalink: /personal/
author_profile: true
---

Welcome to my personal photo gallery! Here are some of my nature and travel photography favorites:

<div class="photo-gallery">
  {% assign captions = site.data.personal_captions %}
  {% for image in site.static_files %}
    {% if image.path contains '/assets/img/personal/' %}
      {% assign caption = captions[image.name] | default: (image.name | split:'.' | first) %}
      <figure style="display:inline-block; margin:10px; text-align:center;">
        <a href="{{ image.path | relative_url }}" data-lightbox="gallery" data-title="{{ caption }}">
          <img src="{{ image.path | relative_url }}" alt="{{ caption }}" style="width: 200px; border-radius: 8px;">
        </a>
        <figcaption style="margin-top:4px; font-size:0.9em;">{{ caption }}</figcaption>
      </figure>
    {% endif %}
  {% endfor %}
</div>
