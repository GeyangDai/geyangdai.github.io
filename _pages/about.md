---
layout: about
title: about
permalink: /
subtitle: PhD in Mathematics · Differential Geometry· Index Theory · Mathematical Physics

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Department of Mathematics</p>
    <p>National University of Singapore</p>
    <p>Email: <a href="mailto:geyang.dai@u.nus.edu">geyang.dai@u.nus.edu</a></p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I work on Differential Geometry and Mathematical Physics.
My current projects focus on:

- Loop space and double loop space geometry;
- Index Theorems and Elliptic Cohomology;
- Quantization and Chern-Simons theory.

[Google Scholar](https://scholar.google.com/citations?user=1j_zvZcAAAAJ&hl=zh-CN)

<div class="formula-showcase" markdown="1">

<div class="formula-item" markdown="1">
<div class="formula-equation">
\[
\large
\frac{\sin(\pi z)}{\pi z}
=
\prod_{n=1}^{\infty}
\left(1-\frac{z^2}{n^2}\right).
\]
</div>
</div>

<div class="formula-item" markdown="1">
<div class="formula-equation">
\[
\large
q^{-\frac{1}{12}}\frac{\theta_{11}(z,\tau)}{\eta(\tau)}
=
\left(e^{\pi i z}-e^{-\pi i z}\right)
\prod_{m=1}^{\infty}
\left(1-q^m e^{2\pi i z}\right)
\left(1-q^m e^{-2\pi i z}\right).
\]
</div>
</div>

</div>

<style>
.post-header {
  position: relative;
  padding-right: min(32vw, 220px);
}

.post-header::after {
  content: "中文签名";
  position: absolute;
  top: 0.1rem;
  right: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  width: min(28vw, 190px);
  height: 76px;
  border: 1.5px dashed var(--global-text-color-light, #777);
  border-radius: 14px;
  background-color: var(--global-card-bg-color, rgba(255, 255, 255, 0.72));
  background-image: url("/assets/img/chinese_signature.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
  color: var(--global-text-color-light, #777);
  font-size: 0.9rem;
  letter-spacing: 0.08em;
}

.formula-showcase {
  margin: 1.1rem 0 1.5rem;
  padding: 0;
  background: transparent;
}

.formula-item {
  padding: 0.15rem 0;
  background: transparent;
}

.formula-item + .formula-item {
  margin-top: 0.85rem;
}

.formula-equation {
  overflow-x: auto;
  overflow-y: hidden;
  padding: 0.25rem 0;
}

.formula-item mjx-container {
  overflow-x: auto;
  overflow-y: hidden;
  max-width: 100%;
  padding-bottom: 0.2rem;
  font-size: 118% !important;
}

@media (max-width: 575px) {
  .post-header {
    padding-right: 0;
  }

  .post-header::after {
    position: static;
    width: 180px;
    height: 64px;
    margin-top: 0.7rem;
  }

  .formula-showcase {
    margin-top: 1rem;
  }
}
</style>
