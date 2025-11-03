---
layout: default
title: "Tags"
---

<h1>依標籤分類</h1>

<div class="tag-list">

  {% comment %}
    Jekyll 會自動建立一個 'site.tags' 變數。
    這個變數包含了你所有文章的標籤，並且已經幫你分類好了。

    'site.tags | sort' 會將標籤按照字母順序 (A-Z) 排列。
  {% endcomment %}

  {% for tag in site.tags | sort %}

    {% comment %}
      'tag[0]' 是標籤的名稱 (例如 "Jekyll" 或 "Guide")
      'tag[1]' 是包含該標籤的所有文章 (一個陣列)
    {% endcomment %}

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