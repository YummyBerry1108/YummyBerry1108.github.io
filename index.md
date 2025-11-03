---
layout: custom_default
---

<h1>文章列表</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <h2>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <p class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</p>

      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
    </li>
  {% endfor %}
</ul>