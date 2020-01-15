---
title: cobalt-github-actions
layout: post.liquid
is_draft: true
---
# Cobalt & GitHub Actions

I have been exploring various DevOps solutions to improve my day job. Manual deployments just haven't been working out. During my research GitHub rolled out their new [GitHub Actions](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/about-github-actions#about-github-actions) feature. 

I have been wanting to automate deployment of this GitHub Pages site since my last post. Testing out Actions is a great excuse to dive in.

Of course it is configured with YAML, the braces optional JSON.

    name: Deploy to GitHub page nathanjent.github.io
    on: [push]
    jobs:
    build:
        runs-on: ubuntu-latest
        steps:
        - name: Checkout source branch
            uses: actions/checkout@v1
            with:
            ref: source


Exploring the documentation I see many integrations with other GitHub features. But most are not that useful for individual contributor projects like mine. I will focus on automating [Cobalt](http://cobalt-org.github.io) to build this site and update pages.
