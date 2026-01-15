---
title: "博客归档"
layout: archive
permalink: /year-archive/
---

## 按年份查看文章

{% assign postsByYear = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}

{% for year in postsByYear %}
  <h2 id="{{ year.name }}" class="archive__subtitle">{{ year.name }}</h2>
  
  <div class="entries-{{ entries_layout }}">
    {% for post in year.items %}
      <article class="entry">
        <header>
          <h3 class="entry-title">
            <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
          </h3>
          <time class="entry-time" datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: "%Y年%m月%d日" }}
          </time>
        </header>
        {% if post.excerpt %}
          <div class="entry-excerpt">
            {{ post.excerpt | markdownify }}
          </div>
        {% endif %}
      </article>
    {% endfor %}
  </div>
{% endfor %}
