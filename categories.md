---
layout: page
title: 分类
permalink: /categories/
---

## 所有分类

{% for category in site.categories %}
  <h3 id="{{ category[0] | slugify }}">{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span style="color:#888; font-size:0.9em;">（{{ post.date | date: "%Y-%m-%d" }}）</span>
      </li>
    {% endfor %}
  </ul>
{% endfor %}

<p style="margin-top: 2em;"><a href="/">← 返回首页</a></p>
