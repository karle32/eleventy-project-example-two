---
layout: base
title: My Web Blog
pagination:
  data: collections.general
  size: 2
  alias: posts
---

## My Blog Posts

{%- for post in posts %}
- [{{ post.data.title }}]({{ post.url }})
{%- endfor %}

{% if pagination.href.previous %}
  <a href="{{pagination.href.previous}}">Previous Page</a>
{% endif %}
{% if pagination.href.next %}
  <a href="{{pagination.href.next}}">Next Page</a>
{% endif %}