---
layout: default
title: 首页
---

<div class="posts">
  {% for post in site.posts %}
    <article class="post">
      <h2>
        <a href="{{ post.url | relative_url }}">
          {{ post.title }}
        </a>
      </h2>
      <div class="post-meta">
        {{ post.date | date: "%Y年%m月%d日" }}
      </div>
      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
    </article>
  {% endfor %}
</div>
