---
title: "rafikurnia's blog"
layout: default
---

Welcome to my blog where I write random things!<br>
This blog is a bit abandoned, but the contents are still relevant to my life :D

Cheers,<br>
Rafi

## Posts
<ul style="margin: 20px 0 20px 0">
  {% for post in site.posts %}
    <li>
      <h3 style="margin: 5px 0 0 0">
        <a href="{{ post.url }}">({{ post.date | date: "%Y-%m-%d" }}) {{ post.title }}</a>
      </h3>
    </li>
  {% endfor %}
</ul>