---
title: "rafikurnia's writing"
layout: default
---

## Welcome
Hi! Thanks for visiting...  
Here you can read my writings about things.  
I hope you will find them helpful!


## Writings
<ul style="margin: 20px 0 20px 0">
  {% for post in site.posts %}
    <li>
      <h3 style="margin: 5px 0 0 0">
        <a href="{{ post.url }}">{{ post.title }} ({{ post.date | date: "%B %-d, %Y" }})</a>
      </h3>
    </li>
  {% endfor %}
</ul>