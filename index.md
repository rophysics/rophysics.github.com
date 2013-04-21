---
layout: page
title: Hello, World!
tagline: liang
---
{% include JB/setup %}

{% for post in site.posts limit:2 %}
{{ post.date }}
{{ post.content }}

<p><a href="{{ post.url }}">comment</a></p>

{% endfor %}