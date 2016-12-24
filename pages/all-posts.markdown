---
layout: page
title: All Posts
permalink: /all-posts/
---
<h3>Recent Posts</h3>
<ul>
	{% for post in site.posts %}
		<li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }} | [{{ post.date | date: "%d-%b-%y" }}]</a></li>
	{% endfor %}
</ul>
<br /><br />