---
layout: page
sidebar: right
subheadline: Creative writing, thoughts, and various stuff
title:  "Blog"
breadcrumb: true
tags:
    - post format
image:
    title: blog-banner.jpg
permalink: "/blog/"
---
<ul>
    {% for post in site.categories.blog %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }} - {{ post.subheadline }}</a><br/>{{post.teaser}}</li>
    {% endfor %}
</ul>
