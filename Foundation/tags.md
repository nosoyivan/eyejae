---
layout: page
title: Tags
permalink: /Tags/
---

{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

<div id="{{ t }}">{{ t | downcase }}</div>
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
    <a class="post-link blacklink" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }} | <a href="/{{ post.author }}">{{ post.author }}</a> | <a href="/{{ post.categories }}">{{ post.categories }}</a></span><hr />

  {% endif %}
{% endfor %}
</ul>
{% endfor %}
