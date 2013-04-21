---
layout: default
---
{% for post in site.posts limit:5 %}
<div>
	<h2>{{ post.title }}</h2>
	<b>{{ post.date| date_to_string }}</b>
	
	{{ post.content }}
	
</div>
{% endfor %}