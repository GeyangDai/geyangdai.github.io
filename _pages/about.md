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

### Product formulas

<div class="formula-item" markdown="1">
<span class="formula-label">Sine product formula</span>

$$
\frac{\sin(\pi z)}{\pi z}
=
\prod_{n=1}^{\infty}
\left(1-\frac{z^2}{n^2}\right).
$$
</div>

<div class="formula-item" markdown="1">
<span class="formula-label">Two-dimensional version</span>

$$
q^{-\frac{1}{12}}\frac{\theta_{11}(z,\tau)}{\eta(\tau)}
=
\left(e^{\pi i z}-e^{-\pi i z}\right)
\prod_{m=1}^{\infty}
\left(1-q^m e^{2\pi i z}\right)
\left(1-q^m e^{-2\pi i z}\right).
$$
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
  margin: 1.35rem 0 1.75rem;
  padding: 1.15rem 1.25rem;
  border: 1px solid rgba(127, 127, 127, 0.20);
  border-radius: 20px;
  background:
    linear-gradient(135deg, rgba(245, 238, 220, 0.72), rgba(255, 255, 255, 0.20)),
    var(--global-card-bg-color, #fff);
  box-shadow: 0 12px 34px rgba(0, 0, 0, 0.08);
}

.formula-showcase h3 {
  margin-top: 0;
  margin-bottom: 1rem;
  font-size: 1.15rem;
}

.formula-item {
  padding: 0.95rem 1rem;
  border-radius: 16px;
  background: rgba(255, 255, 255, 0.46);
}

.formula-item + .formula-item {
  margin-top: 1rem;
}

.formula-label {
  display: inline-block;
  margin-bottom: 0.6rem;
  color: var(--global-text-color-light, #666);
  font-size: 0.86rem;
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}

.formula-item mjx-container {
  overflow-x: auto;
  overflow-y: hidden;
  max-width: 100%;
  padding-bottom: 0.2rem;
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
    padding: 1rem;
  }
}
</style>
