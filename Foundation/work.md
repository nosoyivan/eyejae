---
layout: page
title: work
permalink: /work/
headerimage: /assets/img/foodheader.jpg

---
*work, work, work, work, work*

***

<ul class="post-list">
  {% for post in site.categories.work %}
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
