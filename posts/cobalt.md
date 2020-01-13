---
title: Cobalt
published_date: "2019-01-10 02:47:06 +0000"
layout: post.liquid
is_draft: false
---
# Cobalt Static Site Generator

I have been building this site using [Cobalt](http://cobalt-org.github.io)

Cobalt allows me to write my posts using Markdown syntax.

```markdown
---
title: Cobalt
layout: post.liquid
is_draft: true
---
# Cobalt Static Site Generator

I have been building this site using [Cobalt](http://cobalt-org.github.io)

```

It then combines my posts with layout files written in [Liquid](https://shopify.github.io/liquid/) templates.


{% raw %}

    {% include "_header.liquid" %}
    {% include "_menu.liquid" %}
    <main class="main-content">
        {{ page.content }}
    </main>
    {% include "_footer.liquid" %}

{% endraw %}

FYI: You can escape the Liquid template syntax with the `{% raw %}{% raw %}{% endraw %}` tag.

I then add some CSS which can be broken up using [SASS](https://sass-lang.com/) and I've got a full site.

I could even add some scripts if I wanted to get fancy. Mostly it avoids all the backend configuration. I just write a post and build. I could even setup a CI that would automatically build whenever I commit an update if I feel inclined.
