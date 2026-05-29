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
}
</style>
