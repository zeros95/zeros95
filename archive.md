---
layout: page
title: 归档
permalink: /archive/
---

## 文章归档

{% comment %} ===== 归档粒度切换：取消注释其中一行，注释掉另一行 ===== {% endcomment %}

{% comment %} 按年月归档（精确到月） {% endcomment %}
{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y年%m月'" %}

{% comment %} 按年归档（只到年） {% endcomment %}
{% comment %}
{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y年'" %}
{% endcomment %}

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
