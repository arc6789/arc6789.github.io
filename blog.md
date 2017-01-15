---
layout: blogposts
title: "Blog"
crawlertitle: "Anusuya Choudhury | Blog"
permalink: /blog/
summary: "About this blog"
active: blog
published: false
---

<h1> jekyll matter </h1>



<h1 class="o-title text-center">{{ o.title }}</h1>

{% for o in site.posts.old limit: 6 %}
<article class="o">
 <h1 class="o-title text-center">{{ o.title }}</h1>
  <div class="o-content">
    {{ content }}
  </div>
</article>
{% endfor %}