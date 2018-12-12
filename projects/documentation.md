---
layout: project
title: "Documentation"
description: "Function and Class descrition of Navindoor"
header-img: "img/BG.jpg"
---

<h1> Classes</h1>
{% for post in site.posts %}
{% if post.layout contains 'class' %}
<hr>
<div class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
        <h2 class="post-title"> &#9673; {{ post.title }}</h2>
        <small>
        {{ post.description }}
        </small>

    </a>
</div>
<hr>
{% endif %}
{% endfor %}
