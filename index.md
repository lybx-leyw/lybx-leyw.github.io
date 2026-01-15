---
layout: splash
title: "欢迎来到我的技术空间"
excerpt: "化工专业学生 → 计算机科学探索者"
header:
  overlay_image: /assets/images/header-bg.jpg # 可选头部图片
  overlay_filter: 0.5
  actions:
    - label: "查看我的项目"
      url: "/portfolio/"
    - label: "阅读博客"
      url: "/year-archive/"  # 新增博客链接
    - label: "GitHub"
      url: "https://github.com/lybx-leyw"
---

## 最新博客文章

<div class="feature__wrapper">
  {% for post in site.posts limit:1 %}  <!-- 只显示最新一篇 -->
  <div class="feature__item" style="width: 100%;">
    <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork">
      <h3 class="archive__item-title" itemprop="headline">
        <a href="{{ post.url }}" rel="permalink">{{ post.title }}</a>
      </h3>
      
      <p class="page__meta">
        <i class="far fa-calendar-alt" aria-hidden="true"></i> 
        {{ post.date | date: "%Y年%m月%d日" }}
        &nbsp;&nbsp;
        <a href="{{ post.url }}" class="btn btn--light btn--small">阅读全文</a>
        &nbsp;&nbsp;
        <a href="/year-archive/" class="btn btn--info btn--small">所有文章</a>
      </p>
    </article>
  </div>
  {% endfor %}
</div>

## 我的项目

<div class="feature__wrapper">
  <div class="feature__item">
    <div class="archive__item">
      <div class="archive__item-body">
        <h3 class="archive__item-title">
          <a href="https://github.com/lybx-leyw/Big-integer-arithmetic">大整数运算库</a>
        </h3>
        <div class="archive__item-excerpt">
          <p>C语言实现，包含NTT算法优化，性能提升198.57倍</p>
        </div>
        <p>
          <a href="https://github.com/lybx-leyw/Big-integer-arithmetic" class="btn btn--primary">查看源码</a>
        </p>
      </div>
    </div>
  </div>
  
  <div class="feature__item">
    <div class="archive__item">
      <div class="archive__item-body">
        <h3 class="archive__item-title">
          <a href="https://github.com/lybx-leyw/AlphaGomoku">五子棋AI</a>
        </h3>
        <div class="archive__item-excerpt">
          <p>基于AlphaGo风格的双网络架构，策略网络准确率~50%</p>
        </div>
        <p>
          <a href="https://github.com/lybx-leyw/AlphaGomoku" class="btn btn--primary">查看源码</a>
        </p>
      </div>
    </div>
  </div>
  
  <div class="feature__item">
    <div class="archive__item">
      <div class="archive__item-body">
        <h3 class="archive__item-title">
          <a href="https://github.com/lybx-leyw/Tetris">俄罗斯方块</a>
        </h3>
        <div class="archive__item-excerpt">
          <p>C语言完整实现，模块化设计，线性变换旋转算法</p>
        </div>
        <p>
          <a href="https://github.com/lybx-leyw/Tetris" class="btn btn--primary">查看源码</a>
        </p>
      </div>
    </div>
  </div>
</div>

<div style="text-align: center; margin-top: 3em; padding: 2em; background-color: #f8f9fa; border-radius: 10px;">
  <h3>探索更多</h3>
  <p>
    <a href="/portfolio/" class="btn btn--info">查看所有项目</a>
    &nbsp;&nbsp;&nbsp;
    <a href="/year-archive/" class="btn btn--success">阅读技术博客</a>
    &nbsp;&nbsp;&nbsp;
    <a href="/about/" class="btn btn--warning">关于我</a>
  </p>
</div>

