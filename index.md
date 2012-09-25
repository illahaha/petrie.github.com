---
layout: page  
title: 一个人能控制的只有自己
tagline: 
---
{% include JB/setup %}

<ul>
	<li><span>我的豆瓣</span></li>
	<li><span>我的微博</span></li>
</ul>
-----

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

