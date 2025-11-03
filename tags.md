---
layout: custom_default
title: "Tags"
---

<h1>標籤</h1>

<div class="tag-list">

  {% for tag in site.tags | sort %}

    {% assign tag_name = tag[0] %}
    {% assign posts_with_tag = tag[1] %}

    <h2 id="{{ tag_name | slugify }}">{{ tag_name }}</h2>

    <ul>
      {% for post in posts_with_tag %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <span style="color: #999;">({{ post.date | date: "%Y-%m-%d" }})</span>
        </li>
      {% endfor %}
    </ul>

  {% endfor %}

</div>