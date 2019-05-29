---
layout: archive
title: "Book notes"
permalink: /booknotes/
author_profile: true
---
{% assign booknotes = site.booknotes | sort: date | reverse %}
{% for booknote in booknotes %}
  <div class="booknote">
    {% if booknote.bookcover %}
      <img class="fillwidth" style="float: left" alt="{{ booknote.title }}" src="{% if booknote.bookcover contains "://" %}{{ booknote.bookcover }}{% else %}{{ booknote.bookcover | absolute_url }}{% endif %}">
    {% endif %}
    <h2><a href="{{ booknote.url }}">{{ booknote.title }}</a></h2>
    <div>{{ booknote.excerpt }}</div>
  </div>
  <div class="clear"></div>
{% endfor %}  