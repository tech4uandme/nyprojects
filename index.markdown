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
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <p style='font-size=10pt'>{{ post.excerpt }}
        <a href="{{ post.url | relative_url }}">weiter lesen...</a></p>
    </li>
  {% endfor %}
</ul>
  
  {% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul class='post-list'>
    {% for post in category[1] %}
      <li class='post-link'><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

