---
layout: page
title: photo
permalink: /photo/
headerimage: /assets/img/foodheader.jpg

---
*My own phototgraphy*

***

<ul class="post-list">
  {% for post in site.categories.photo %}
    <li>

      <h2>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </h2>
      <span class="post-meta">
        {{ post.date | date: "%b %-d, %Y" }} •
        <a href="{{ post.categories }}">{{ post.categories }}</a>
      </span><br />

    </li>

    {{ post.photothumb }}
    <div class="post-desc">{{ post.description }}</div>

    <hr />

  {% endfor %}
</ul>
