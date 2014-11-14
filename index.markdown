---
layout: default
---
{% for post in site.posts limit:5 %}
<div>
	<a href="{{ post.url }}"><h2>{{ post.title }}</h2></a>
	<b>{{ post.date| date_to_string }} by <a href="/about.html">Liangzhao</a></b>
	
	{{ post.content }}
	
</div>
-------------------------
{% endfor %}
<a href="/archive.html"><h2>Archives</h2></a>