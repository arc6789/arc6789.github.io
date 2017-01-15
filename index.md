---
layout: default
crawlertitle: "Anusuya Choudhury | Portfolio"
title: "Home"
summary: "main page"
---

<h2 class="col-lg-12 text-center page-title">PORTFOLIO</h2>
{% for post in site.posts limit: 6 %}
  <article class="index-page">
  	<div class="article_img col-lg-8">
		  <img class="img-thumbnail img-responsive" style="width:100%; margin:0" src="assets/images/{{post.bg}}">
	  </div>
	  <div class="article_content col-lg-4">
    	<!-- <h2><a href="{{ post.url }}">{{ post.title }}</a></h2> --> <!-- Temp -->
      <h2 class="text-center">{{ post.title }}</h2>
      {% if post.summary %}
    	 <p class="summary">{{ post.summary }}</p>
      {% else %}
        <p class="summary">{{ post.content }}</p>
      {% endif %}
      {% if post.link and post.code %}
        <p><strong><a href="{{ post.link }}" target="_blank">View LIVE</a> | <a href="{{ post.code }}" target="_blank"> View CODE</a></strong></p>
      {% elsif post.link %}
        <p><strong>View live at: <a href="{{post.link}}" target="_blank">{{post.link}}</a></strong></p>
      {% elsif post.code %}
        <p><strong>CODE: <a href="{{post.code}}" target="_blank">{{post.code}}</a></strong></p>
      {% endif %}
    	<p clas="roles"><strong>Roles: {{ post.roles }}</strong></p>
    	<p class="tools"><strong>Tools: {{ post.tools }}</strong></p>
    </div>
  </article>
{% endfor %}


<!--     {% for my_page in site.pages %}
      {% if my_page.active %}
        <a href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a>
      {% endif %}
    {% endfor %} -->
 
