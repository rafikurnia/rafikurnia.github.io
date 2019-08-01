---
title: "rafikurnia's journal"
layout: default
---

## Welcome!
My name is Rafi and I created this page to share things I have learned and explored.  
It is wonderful if they can be beneficial for you!  

## Check them out:
<ul>
  {% for post in site.posts %}
    <li>
      <h3>
        <a href="{{ post.url }}">{{ post.title }} ({{ post.date | date: "%B %-d, %Y" }})</a>
      </h3>
    </li>
  {% endfor %}
</ul>