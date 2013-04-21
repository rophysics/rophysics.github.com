---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}

<h2>Recent 2 posts</h2>

{% for post in site.posts limit:2 %}
<div>
{{ post.content }}
<p>
<a href="{{ post.url }}">read more </a>
</p>
</div>
{% endfor %}