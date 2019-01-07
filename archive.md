---
permalink: /archive.html
layout: default.liquid

title: Nathan Jent
---
## Archived Posts

{% for post in collections.posts.pages %}
{% if post.data.archived %}
#### {{post.title}}

[{{ post.title }}]({{ post.permalink }})
{% endif %}
{% endfor %}
