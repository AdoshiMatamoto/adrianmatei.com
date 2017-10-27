---
layout: archive
title: "Book notes"
permalink: /booknotes/
author_profile: true
---
{% assign booknotes = site.booknotes | sort: date | reverse %}
{% for booknote in booknotes %}  
  <h2><a href="{{ booknote.url }}">{{ booknote.title }}</a></h2>
  <div>{{ booknote.excerpt }}</div>
{% endfor %}  