---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h2>Posts</h2>
<ul class='post-list'>
  {% for post in site.posts %}
    <li class='post-link'><a href="{{ post.url }}">{{ post.title }}</a></li>
    <li class='post-link'><a href="{{ post.url }}">weiter lesen...</a></li>
  {% endfor %}
</ul>
  
  {% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

