---
layout: page
show_meta: false
title: "Projects"
subheadline: "A collection of works, big and small, over my career."
header: no
permalink: "/projects/"
---
<ul>
    {% for post in site.categories.projects %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }} - {{ post.subheadline }}</a><br/>{{post.teaser}}</li>
    {% endfor %}
</ul>