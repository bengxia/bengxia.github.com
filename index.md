---
layout: page
title: 欢迎来到 bengxia@github!
tagline: 
---
{% if site.posts.size > 0 %}
<section style="posts">
  <h1>随笔!</h1>
{% for post in site.posts limit:3 %}
  <article>
    <h2><a href="{{ post.url | replace:'.html','' }}">{{ post.title }}</a></h2>
    {{ post.description | textilize }}
    <p>由 <a href="http://github.com/{{ post.author }}">{{ post.author }}</a> 在 {{ post.date | date_to_string }} 发布.</p>
  </article>
{% endfor %}
  <p><a href="/posts">更多随笔!</a></p>
</section>
{% endif %}