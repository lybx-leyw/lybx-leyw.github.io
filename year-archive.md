---
title: "博客归档"
layout: archive
classes: ["page--archive"]
permalink: /year-archive/
---

按年份查看我的所有文章：

{% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != current_year %}
    {% unless forloop.first %}</ul>{% endunless %}
    <h2 id="{{ year }}" class="archive__subtitle">{{ year }}{{ year }}</h2>
    <ul class="archive__list">
    {% assign current_year = year %}
  {% endif %}
  <li>
    <span class="archive__item-date">{{ post.date | date: "%Y年%m月%d日" }}</span>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
  {% if forloop.last %}</ul>{% endif %}
{% endfor %}
