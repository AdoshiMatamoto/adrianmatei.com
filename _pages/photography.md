---
layout: archive
title: "Posts by Collection"
permalink: /photography/
author_profile: true
---
{% for collection in site.collections %}  
  {% for post in collection.photography %}
    {% unless collection.output == false or collection.label == "posts" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
{% endfor %}  