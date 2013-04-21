---
layout: default
---
{% for post in site.posts limit:5 %}
<div>
	{{ post.title }}
	{{ post.date }}
	{{ post.content }}
	
</div>
{% endfor %}