Welcome to this page!  
My name is Rafi and I created this page to share anything about things I learned, explored, and thought.  

Check them out:
<ul>
  {% for post in site.posts %}
    <li>
      <h2>
        <a href="{{ post.url }}">{{ post.title }} ({{ post.date | date: "%B %-d, %Y" }})</a>
      </h2>
    </li>
  {% endfor %}
</ul>