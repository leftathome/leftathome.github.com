---
layout: page
title: leftblog
tagline: Adventures in Automation
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts limit: 10 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    </br> <em>{{ post.excerpt }} </em>
  {% endfor %}
</ul>

