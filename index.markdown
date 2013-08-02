---
layout: default
---
{% for post in site.posts limit:5 %}
<div>
	<a href="{{ post.url }}"><h2>{{ post.title }}</h2></a>
	<b>{{ post.date| date_to_string }}</b>
	
	{{ post.content }}
	
</div>
-------------------------
{% endfor %}