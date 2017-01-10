---
layout: default
crawlertitle: "Jekyll blog"
title: "Home"
summary: "main page"
---

{% for post in site.posts limit: 6 %}
  <article class="index-page row">
  	<div class="article_img col-lg-8">
		  <img class="img-thumbnail img-responsive" style="width:100%; margin:0" src="assets/images/{{post.bg}}">
	  </div>
	  <div class="article_content col-lg-4">
    	<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    	<p class="summary">{{ post.summary }}</p>
    	<p class="link"><strong>View live at: <a href="{{ post.link }}">{{ post.link }}</a></strong></p>
    	<p clas="roles"><strong>Roles: {{ post.roles }}</strong></p>
    	<p class="tools"><strong>Tools: {{ post.tools }}</strong></p>
    </div>
  </article>
{% endfor %}

