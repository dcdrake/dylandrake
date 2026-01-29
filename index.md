---
layout: default
---
<p class="intro">
  Thoughts I have when I'm doing my daily ritual of staring at a blank wall like a cat.
</p>

<ul class="post-list">
  {% for post in site.posts %}
  <li class="post-item">
    <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
    <h2 class="post-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    {% if post.excerpt %}
    <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    {% endif %}
  </li>
  {% endfor %}
</ul>
