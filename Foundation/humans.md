---
layout: page
title: humans
permalink: /humans/
---
*Some simple observations on the human thought process from my point of view. This is pretty much just an excuse for me to be an internet armchair psychologist.*

***

{% for post in site.categories.humans %}
  <a class="post-link blacklink" href="{{ post.url }}">{{ post.title }}</a>
  <span class="post-meta" style="line-height: .5em;">{{ post.date | date: "%b %-d, %Y" }} <a href="/{{ post.author }}">{{ post.author }}</a></span>
  <hr />
{% endfor %}
