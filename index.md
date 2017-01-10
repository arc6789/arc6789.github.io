---
layout: default
crawlertitle: "Jekyll blog"
title: "Home"
summary: "main page"
---

{% for post in site.posts limit: 5 %}
  <article class="index-page row">
  	<div class="img-wrap col-lg-8">
		<img style="width:100%; padding: 0 20px" src="assets/images/{{post.bg}}">
	</div>
	<div class="content-wrap col-lg-4">
    	<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    	<p>{{ post.excerpt }}</p>
    	<p>View live at: <a href="{{ post.link }}">{{ post.link }}</a></p>
    	<p>Roles: {{ post.roles }}</p>
    </div>
  </article>
{% endfor %}

