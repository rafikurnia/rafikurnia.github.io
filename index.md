---
title: "rafikurnia's journal"
layout: default
---

## Welcome!
My name is Rafi and I created this page to write whatever I want to write!  
It can be something unimportant or (maybe) important..

Well, my original intention is to write [#TIL](https://knowyourmeme.com/memes/today-i-learned-til) posts.  
But sometimes I will probably write some tutorials too.  

Anyway, I want to share anything I have learned and explored through a writing.  
It is wonderful if they can be beneficial for you!  
  
## Check them out:
<ul style="margin: 20px 0 20px 0">
  {% for post in site.posts %}
    <li>
      <h3 style="margin: 5px 0 0 0">
        <a href="{{ post.url }}">{{ post.title }} ({{ post.date | date: "%B %-d, %Y" }})</a>
      </h3>
    </li>
  {% endfor %}
</ul>