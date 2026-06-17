---
layout: page
title: 归档
permalink: /archive/
---

## 文章归档

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y年%m月'" %}

{% for year_month in posts_by_year %}
  <h3>{{ year_month.name }}</h3>
  <ul>
    {% for post in year_month.items %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span style="color:#888; font-size:0.9em;">（{{ post.date | date: "%Y-%m-%d" }}）</span>
      </li>
    {% endfor %}
  </ul>
{% endfor %}

<p style="margin-top: 2em;"><a href="/">← 返回首页</a></p>
