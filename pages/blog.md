---
layout: page
sidebar: right
subheadline: Creative writing, thoughts, and various stuff
title:  "Blog"
breadcrumb: true
tags:
    - post format
header: no
image:
    title: blog-banner.jpg
permalink: "/blog/"
---
{% for post in site.categories.blog %}
<div class="row">
    <div class="small-12 columns b60">
        <h2>
            <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
        </h2>
        <p class="subheadline">
        <span class="subheader">{% for tag in post.tags %}{{ tag }}{% unless forloop.last %} , {% endunless %}{% endfor %}
        </span>
        {{ post.subheadline }}
        </p>
        {% if post.image %}
        <img src="{{ site.url }}{{ site.baseurl }}/images/{{ post.image.title }}" class="alignleft" width="150" height="150">
        {% endif %}
        {{post.teaser}} &nbsp;
        <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}"><strong>Read More&nbsp;></strong></a>
    </div>
</div>
{% endfor %}
