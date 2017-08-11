---
layout: archive
title: "Photostories"
permalink: /photostories/
author_profile: true
---
{% assign photostories = site.photostories | sort: date | reverse %}
{% for photostory in photostories %}  
  <h2><a href="{{ photostory.url }}">{{ photostory.title }}</a></h2>
  <a href="{{ photostory.url }}">
    <img src="{{ site.url }}{{ site.baseurl }}{{ photostory.header.image }}" alt="" class="full">
  </a>  
  <div>{{ photostory.excerpt }}</div>
{% endfor %}  