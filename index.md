---
layout: page
title: JAVA Blog!
tagline: Supporting tagline
---
{% include JB/setup %}

{% for post in site.posts limit: 10 %}
  <div id="mainWrapper">
		<div class="post">
			<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
			<h3 class="date">{{ post.date | date:"%Y-%m-%d" }}{% if post.author %} <a href="/pages/about/index.html">{{ post.author }}</a>{% endif %}</h3>
		</div>
		{{ post.content  }}
		<br/>
		<h3 class="tags">Cimkek:</h3>
		<ul class="tag_box inline">
			{% for tag in post.tags %}
				<li><a href="/tags.html#{{tag}}-ref">{{tag}}</a></li>	
			{% endfor %}
		</ul>
  </div>
  {% endfor %}