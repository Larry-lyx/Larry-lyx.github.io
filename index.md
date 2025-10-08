---
layout: home
title: 我的学习笔记
---

# 欢迎来到我的学习笔记网站

这里记录了我的学习过程和心得。

## 最新笔记

{% for post in site.posts limit:5 %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

## 所有分类

{% for category in site.categories %}
- {{ category[0] }}
  {% for post in category[1] %}
  - [{{ post.title }}]({{ post.url }})
  {% endfor %}
{% endfor %}