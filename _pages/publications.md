---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
<p>You can also find my articles on <a href="{{ site.author.googlescholar }}" target="_blank">Google Scholar</a>.</p>
{% endif %}

{% if author.nasaads %}
<p>My publication list is also available on <a href="{{ site.author.nasaads }}" target="_blank">NASA ADS</a>.</p>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
