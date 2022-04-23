---
title: Writing system
layout: index
---

{% for exhibit in site.exhibits %}

  {% assign system = site.data.system | find: "name", exhibit.system %}
  <a href = "{{ exhibit.url | relative_url }}"><img src="{{ exhibit.image-url }}" width = 256></a>
  <p><a href = "{{ exhibit.url | relative_url }}">{{ exhibit.title }}</a>  <a href = "{{ system.homepage }}">{{ exhibit.system }}</a></p>

  <p>Time-Period: {{ exhibit.Time-Period }}</p>
  <p>Features: {{ exhibit.Features }}</p>
  <p>Representative: {{ exhibit.Representative }}</p>
  <p>Image-url: <a href="{{ exhibit.Image-url }}">{{ exhibit.Image-url }}</a></p>



{% endfor %}
