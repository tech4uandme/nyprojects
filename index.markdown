---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

Posts

  {% for post in site.posts %}
    [{{ post.title }}]({{ post.url }})
      {{ post.excerpt }}
    [weiter lesen...]({{ post.url }})  
  {% endfor %}
  
  {% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

