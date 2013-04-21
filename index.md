---
layout: page
title: Hello, World!
tagline: liang
---
{% include JB/setup %}

{% for post in site.posts limit:2 %}
{{ post.title }}
{{ post.content }}
{% endfor %}