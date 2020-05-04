---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h2>Posts</h2>
<ul class='post-list'>
  {% for post in site.posts %}
    <li class='post-link'>
      <span class='post-meta'>{{ post.date }}</span><br>
      <a href="{{ post.categories }}{{ post.url }}">{{ post.title }}</a>
      <small>{{ post.excerpt }}
        <a href="{{ post.categories }}{{ post.url }}">weiter lesen...</a></small>
    </li>
  {% endfor %}
</ul>
  
  {% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul class='post-list'>
    {% for post in category[1] %}
      <li class='post-link'><a href="{{ post.categories }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

