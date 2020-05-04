---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h1>Posts</h1>
<ul class='post-list'>
  {% for post in site.posts %}
    <li class='post-link'>
      <span class='post-meta'>{{ post.date }}</span><br>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <div style='font-size:8pt'>{{ post.excerpt }}
        <a href="{{ post.url | relative_url }}">weiter lesen...</a></div>
    </li>
  {% endfor %}
</ul>
  
<h1>Kategorien</h1>
  {% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul class='post-list'>
    {% for post in category[1] %}
      <li class='post-link'><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

