---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}

{% for post in site.posts limit:1 %}
{{ post.title}}
{{ post.tagline }}
{{ post.date | date_to_string }}
{{ post.content }}

<a href="{{ post.url }}">comment</a>

{% endfor %}