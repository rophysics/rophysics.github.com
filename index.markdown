---
layout: default
---
{% for post in site.posts limit:3 %}
<div>
	<a href="{{ post.url }}"><h2>{{ post.title }}</h2></a>
	<b>{{ post.date| date_to_string }} by  <a href="/about.html">Liangzhao</a></b>
	
	{{ post.content }}
	
</div>
-------------------------
{% endfor %}
    <div class="pagination">
      <ul>
      {% if page.previous %}
        <li class="prev"><a href="{{ BASE_PATH }}{{ page.previous.url }}" title="{{ page.previous.title }}">&larr; Previous</a></li>
      {% else %}
        <li class="prev disabled"><a>&larr; Previous</a></li>
      {% endif %}
        <li><a href="{{ BASE_PATH }}{{ site.JB.archive_path }}">Archive</a></li>
      {% if page.next %}
        <li class="next"><a href="{{ BASE_PATH }}{{ page.next.url }}" title="{{ page.next.title }}">Next &rarr;</a></li>
      {% else %}
        <li class="next disabled"><a>Next &rarr;</a>
      {% endif %}
      </ul>
    </div>