---
layout: page
title: About
---
{% include JB/setup %}

Born in 1980s. Interested in medical images, radiation physics, web technologies. Now located in Beijing, China.

## Recent Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## Contact

liangzhao6{at}gmail.com


