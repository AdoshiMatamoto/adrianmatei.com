---
layout: archive
author_profile: true
permalink: /blog/
---

{% assign posts = site.posts | sort: date | reverse %}
{% for post in posts %}  
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <a href="{{ post.url }}">
    <img src="{{ site.url }}{{ site.baseurl }}{{ post.thumbnail }}" alt="" class="full">
  </a>  
  <div>{{ post.excerpt }}</div>
{% endfor %}  
