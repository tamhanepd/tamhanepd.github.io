---
layout: archive
title: "Personal"
permalink: /personal/
author_profile: true
---

Welcome to my personal photo gallery! Here are some of my nature and travel photography favorites:

<div class="photo-gallery">
  {% for image in site.static_files %}
    {% if image.path contains '/assets/img/personal/' %}
      <a href="{{ image.path | relative_url }}" data-lightbox="gallery" data-title="Nature photo">
        <img src="{{ image.path | relative_url }}" alt="Nature photo" style="width: 200px; margin: 10px; border-radius: 8px;">
      </a>
    {% endif %}
  {% endfor %}
</div>
