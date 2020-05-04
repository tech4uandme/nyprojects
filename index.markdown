---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

Posts

  {% for post in site.posts %}
    
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
      <a href="{{ post.url }}">weiter lesen...</a>
    
  {% endfor %}

