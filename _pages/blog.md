---
layout: archive
author_profile: true
permalink: /blog/
---

{% assign posts = site.posts | sort: date | reverse %}
{% for post in posts %}  
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  
  {% if post.thumbnail.external %}
  <a href="{{ post.url }}">
    <img src="{{ post.thumbnail.external }}" alt="" class="full">
   </a>  
  {% else %}
  <a href="{{ post.url }}">
    <img src="{{ site.url }}{{ site.baseurl }}{{ post.thumbnail }}" alt="" class="full">
    </a> 
  {% endif %}
  
  <div>{{ post.excerpt }}</div>
  
  <hr>
{% endfor %}  
