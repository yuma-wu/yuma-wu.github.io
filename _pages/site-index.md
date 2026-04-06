---
layout: page
permalink: "/site-index/"
---
{% for post in site.posts %}
<h3><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h3>
<p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
{% endfor %}