---
layout: page
title: Hello, World!
---
{% include JB/setup %}

{% for post in site.posts limit:1 %}
<h2>{{ post.title }}</h2>
{{ post.date | date_to_string }}
{{ post.content }}

<p><a href="{{ post.url }}">comment</a></p>

{% endfor %}