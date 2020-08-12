---
layout: blog.liquid
pageTitle: Blogs Page
pagination:
  data: collections.blog
  size: 2
  alias: blogs
---

# Latest blog posts

<div class="font-bold py-2 px-4">
{% for blog in collections.blog %}

- [{{blog.data.title}}]({{blog.url}})

{% endfor %}

</div>

{% if pagination.href.previous %}
<a href="{{pagination.href.previous}}">Previous Page</a>
{% endif %}
{% if pagination.href.next %}
<a href="{{pagination.href.next}}">Next Page</a>
{% endif %}
