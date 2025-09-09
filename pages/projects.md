---
layout: page
show_meta: false
title: "Projects"
subheadline: "A collection of works, big and small, over my career."
header: no
permalink: "/projects/"
---
{% for post in site.categories.projects %}
<div class="row">
    <div class="small-12 columns b60">
        <h2>
            <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
        </h2>
        <p class="subheadline">{{ post.subheadline }}</p>
        {% if post.image %}
        <img src="{{ site.url }}{{ site.baseurl }}/images/{{ post.image.title }}" class="alignleft" width="150" height="150">
        {% endif %}
        {{post.teaser}}
        <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}"><strong>Read More&nbsp;></strong></a>
    </div>
</div>
{% endfor %}

