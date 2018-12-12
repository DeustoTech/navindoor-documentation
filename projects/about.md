---
layout: project
title: About
description: "Documentation of PIBA-Project"
header-img: "img/BG.jpg"
---

{% for WP in site.data.chapters %}
<h1>  Chapter {{{WP[1].number}}  <small>  {{WP[1].name}} </small></h1>
<p> {{WP[1].description}}</p>
<div id="wrapper"> 
<div id="content"> 

<ul>
{% assign reversepost = site.posts | reverse %}
{% for post in reversepost %}
{% if post.layout contains 'about' %}
{% if WP[0] == post.chapter %}
<hr>
<li style="list-style-type:none">
<div class="post-preview">
<a href="{{ post.url | prepend: site.baseurl }}" style="display: block">
<p class="post-title"> &#9673; {{ post.title }} 
    <small><p class="post-subtitle">{{ post.subtitle }}</p></small>
</p>
</a>
</div>
</li>
<hr>
{% endif %}
{% endif %}
{% endfor %}
</ul> 
</div>
</div>

{% endfor %}
