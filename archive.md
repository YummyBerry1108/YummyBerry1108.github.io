---
layout: custom_default
title: "Archive"
---

<h1>檔案庫</h1>

<div class="archive-list">

  {% assign current_year = 0 %}
  {% assign current_month = 0 %}

  {% for post in site.posts %}
  
    {% assign post_year = post.date | date: "%Y" %}
    {% assign post_month = post.date | date: "%B" %}  
    {% if post_year != current_year %}
      
      <h2 class="archive-year">{{ post_year }}</h2>
      
      {% assign current_year = post_year %}
      
      <h3 class="archive-month">{{ post_month }}</h3>
      
      {% assign current_month = post_month %}
      
    {% else %}
      
      {% if post_month != current_month %}
        
        <h3 class="archive-month">{{ post_month }}</h3>
        
        {% assign current_month = post_month %}
        
      {% endif %}
      
    {% endif %}
    
    <div class="archive-item" style="margin-bottom: 1rem; margin-left: 1.5rem;">
      <span class="post-date" style="color: #999; margin-right: 15px;">
        {{ post.date | date: "%Y-%m-%d" }}
      </span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </div>

  {% endfor %}

</div>