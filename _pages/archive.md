---
layout: default
title: Archive.
permalink: /archive
---

<section class="posts">
{% for post in site.posts %}
   {% assign currentDate = post.date | date: "%Y" %}
   {% if currentDate != myDate %}
       {% unless forloop.first %}</ul>{% endunless %}
       <h1>{{ currentDate }}.</h1>
       <ul>
       {% assign myDate = currentDate %}
   {% endif %}
   <li>
    <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
  </li>
  {% if forloop.last %}</ul>{% endif %}
{% endfor %}
</section>