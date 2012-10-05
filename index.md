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
<script type="text/javascript">
var _bdhmProtocol = (("https:" == document.location.protocol) ? " https://" : " http://");
document.write(unescape("%3Cscript src='" + _bdhmProtocol + "hm.baidu.com/h.js%3Fdb8ac6c44527ed1ea98877a2e6c148e7' type='text/javascript'%3E%3C/script%3E"));
</script>

