---
layout: page
permalink: /life/
title: 我的生活
description: 生活、旅行与随笔
nav: true
nav_order: 6
---

## 影像集

{% assign gallery = site.data.life_gallery %}
{% if gallery and gallery.size > 0 %}
<div class="life-gallery">
  {% for item in gallery %}
    <figure class="life-gallery-card">
      <img src="{{ item.image | relative_url }}" alt="{{ item.alt | default: item.title }}" loading="lazy">
      <figcaption>
        <div class="life-gallery-title">{{ item.title }}</div>
        {% if item.date or item.location %}
          <div class="life-gallery-meta">
            {% if item.date %}{{ item.date }}{% endif %}{% if item.date and item.location %} · {% endif %}{% if item.location %}{{ item.location }}{% endif %}
          </div>
        {% endif %}
        {% if item.caption %}
          <p>{{ item.caption }}</p>
        {% endif %}
      </figcaption>
    </figure>
  {% endfor %}
</div>
{% else %}
<p>影像集还没有照片。把图片放进 <code>assets/img/life/</code>，再编辑 <code>_data/life_gallery.yml</code> 添加条目即可。</p>
{% endif %}

<style>
.life-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.25rem;
  margin-top: 1.25rem;
}

.life-gallery-card {
  margin: 0;
  overflow: hidden;
  border-radius: 18px;
  background: var(--global-card-bg-color, #fff);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.10);
}

.life-gallery-card img {
  display: block;
  width: 100%;
  aspect-ratio: 4 / 5;
  object-fit: cover;
}

.life-gallery-card figcaption {
  padding: 0.9rem 1rem 1rem;
}

.life-gallery-title {
  font-weight: 700;
  font-size: 1rem;
}

.life-gallery-meta {
  margin-top: 0.15rem;
  color: var(--global-text-color-light, #777);
  font-size: 0.85rem;
}

.life-gallery-card p {
  margin: 0.5rem 0 0;
  font-size: 0.92rem;
}
</style>

## 如何更新

1. 把新图片放到 `assets/img/life/` 文件夹。
2. 打开 `_data/life_gallery.yml`，按下面格式新增一段。
3. 提交并推送到 GitHub，网站会自动更新。

```yaml
- image: /assets/img/life/photo-name.jpg
  title: 标题
  date: 2026
  location: 地点
  caption: 这张照片的说明。
  alt: 图片替代文字
```
