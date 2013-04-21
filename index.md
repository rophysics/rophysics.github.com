---
layout: page
title: {{ post.title}}
tagline: {{ post.tagline }}
---
{% include JB/setup %}

{% for post in site.posts limit:1 %}

{{ post.date | date_to_string }}
{{ post.content }}

<a href="{{ post.url }}">comment</a>

{% endfor %}