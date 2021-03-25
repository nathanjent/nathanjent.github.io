---
layout: default.liquid

title: Nathan Jent
---
## Posts

{% for post in collections.posts.pages %}
{% unless post.data.archived %}

### {{post.title}}

[{{ post.title }}]({{ post.permalink }})
{% endunless %}
{% endfor %}
