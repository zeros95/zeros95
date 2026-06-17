---
layout: default
title: 首页
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span style="color:#666; font-size:14px; margin-left:10px;">
        {{ post.date | date: "%Y年%m月%d日" }}
      </span>
    </li>
  {% endfor %}
</ul>
