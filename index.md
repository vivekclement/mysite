---
title: Welcome to My Blog
layout: layout.liquid
pagination:
  data: collections.blogs
  size: 1
  alias: blogs
---

<h1> Welcome to my Blog </h1>
 {% for blogs in blogs %}
 
 - [{{blogs.data.title}}]({{blogs.url}})
 
 {% endfor %}
Welcome Folks!

{% if pagination.href.previous %}
<a href="{{pagination.href.previous}}">Previous</a>
{% endif %}

{% if pagination.href.next %}
<a href="{{pagination.href.next}}">Next</a>
{% endif %}
