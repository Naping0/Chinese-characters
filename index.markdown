---
title: Writing system
layout: index
---

{% for exhibit in site.exhibits %}

  {% assign system = site.data.system | find: "name", exhibit.system %}
  <a href = "{{ exhibit.url | relative_url }}"><img src="{{ exhibit.image-url }}" width = 256></a>
  <p><a href = "{{ exhibit.url | relative_url }}">{{ exhibit.title }}</a>  <a href = "{{ system.homepage }}">{{ exhibit.system }}</a></p>

  <p>Script type: {{ exhibit.Script-type }}</p>
  <p>Time-period: {{ exhibit.Time-period }}</p>
  <p>Direction: {{ exhibit.Direction }}</p>
  <p>Languages: {{ exhibit.Languages }}</p>
  <p>image-url: <a href="{{ exhibit.image-url }}">{{ exhibit.image-url }}</a></p>



{% endfor %}
