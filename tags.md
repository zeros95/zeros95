---
layout: page
title: 标签
permalink: /tags/
---

## 所有标签

{% assign tags = site.tags | sort %}
{% for tag in tags %}
  <h3 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span style="color:#888; font-size:0.9em;">（{{ post.date | date: "%Y-%m-%d" }}）</span>
      </li>
    {% endfor %}
  </ul>
{% endfor %}

<p style="margin-top: 2em;"><a href="/">← 返回首页</a></p>
