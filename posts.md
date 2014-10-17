---
layout: default
title: Zype Developer Portal | Posts
permalink: /blog/
---
<ul>
  {% for post in site.posts %}
    <ol class='blog-posts'>
      <h2>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span class='date'>
          {{ post.date | date: "%b %-d, %Y" }}
        </span>
      </h2>
      <p>
        {{ post.excerpt}}
      </p>
        <a href="{{ post.url }}"> Read More &hellip;</a>
      </p>
    </ol>
  {% endfor %}
</ul>
