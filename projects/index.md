---
layout: page
modified: 2014-07-31T13:23:02.362000-04:00
excerpt: "Instructions on how to install and customize the Jekyll theme Minimal Mistakes."
skip_title: true
nav: projects
title: Projects
image:
  feature: sample-image-3.jpg
  credit: WeGraphics
  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
---

<div markdown="0">
{% for page in site.pages %}
  {% if page.project == true %}
    {% if page.hidden != true %}
      <div class="post post-preview">
      {% if page.link %}
        <h1><a class="post-link" href="{{ page.link }}">
      {% else %}
        <h1><a class="post-link" href="{{ page.url | replace: '/index.html', '' }}">
      {% endif %}
      {{ page.title }}</a></h1>
        <span class="post-date">{{ page.summary }}</span>
      </div>
    {% endif %}
  {% endif %}
{% endfor %}
</div>
